- Ссылка на статью: [arXiv](https://arxiv.org/abs/1802.05365)
- Paper Dissected: “Deep Contextualized Word Representations” Explained: http://mlexplained.com/2018/06/15/paper-dissected-deep-contextualized-word-representations-explained/
- The Current Best of Universal Word Embeddings and Sentence Embeddings: https://medium.com/huggingface/universal-word-sentence-embeddings-ce48ddc8fc3a

### Идея

Используем посимвольные CNN + 2xLSTM (biLM) для обучения языковой модели.
Затем во время решения своей supervised задачи обучаем коэффициенты векторных представлений слов (замораживая при этом веса biLM сети).

Преимуществом таких векторных представлений является то, что они используют все предложение и символы для его построения.
В статье утверждается, что разные слои biLM отображают разную лингвистическую информацию после обучения.

### Шаги

1. Обучаем языковую модель CNN + 2xLSTM (biLM). Уже есть предобученные, в т.ч. для русского (http://docs.deeppavlov.ai/en/master/apiref/models/embedders.html#deeppavlov.models.embedders.elmo_embedder.ELMoEmbedder).

2. Дообучаем (fine-tuning) biLM на своей supervised задаче, отсекая при этом метки (labels) в supervised датасете.
Можно и не дообучать, но тогда будет меньший рост качества.

3. Замораживаем веса biLM. Встраиваем biLM в свою сеть для решения supervised задачи.
Конкатенируем вход [X_k, ELMo(task, k)] и подаем на вход своей сети решающую supervised задачу.
Также ELMo можно одновременно или раздельно подавать на выход сети: [H_k, ELMo(task, k)]. Иногда это улучшает качество.

X_k - объект k из размеченной выборки.
H_k - веса последнего слоя из сети решающую задачу.

ELMo(task, k ) - это подтюненные векторные представления под решение задачи. Причем тюнятся не веса biLM сети, а
специальные коэффициенты.
ELMo(task, k) считается так: g_task*H_biLM_k.
H_biLM_k - заморожен, обновляется только g_task.

Функцию ELMo можно считать используя все слои biLM для улучшения качества. В статье утверждается, что разные слои
отображают разную лингвистическую информацию после обучения.
