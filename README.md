#### 2018-08

-  NIPS Conversational Intelligence Challenge 2017 Winner System: Skill-based Conversational Agent with Supervised Dialog Manager [[ACL](http://aclweb.org/anthology/C18-1312), [Github](https://github.com/sld/convai-bot-1337)]

#### 2018-01

- How People Negotiate? From the Analysis of a Dialogue Corpus to a Dialogue System [[Paper](http://itnas.civil.duth.gr/inista2018/proceedings/inista2018_NHP1.pdf)]

-
    A Survey of Available Corpora For Building Data-Driven Dialogue Systems: The Journal Version [[arXiv](https://arxiv.org/pdf/1512.05742)]
    <details><summary>+</summary>
    <p>
    Большая статья, хороший обзор. Из интересного указаны датасеты к которым есть юзер
    симуляторы и обозначены проблемы диалоговых систем.
    </p>
    </details>

- [Personalizing Dialogue Agents: I have a dog, do you have pets too?](notes/personalizing-da.md) [[arXiv](https://arxiv.org/abs/1801.07243)]

#### 2017-12

- Avoiding Echo-Responses in a Retrieval-Based Conversation System [[arXiv](https://arxiv.org/abs/1712.05626)]
- Conversational AI: The Science Behind the Alexa Prize [[Amazon](https://s3.amazonaws.com/alexaprize/2017/technical-article/alexaprize.pdf)]
- Sounding Board – University of Washington’s Alexa Prize Submission [[Amazon](https://s3.amazonaws.com/alexaprize/2017/technical-article/soundingboard.pdf)]
- Alquist: The Alexa Prize Socialbot [[Amazon](https://s3.amazonaws.com/alexaprize/2017/technical-article/alquist.pdf)]
- Superhuman AI for heads-up no-limit poker: Libratus beats top professionals [[Science](http://science.sciencemag.org/content/sci/early/2017/12/15/science.aao1733.full.pdf)]

#### 2017-11

- A Survey on Dialogue Systems: Recent Advances and New Frontiers [[arXiv](https://arxiv.org/abs/1711.01731)]

#### 2017-09

- A Deep Reinforcement Learning Chatbot [[arXiv](https://arxiv.org/abs/1709.02349)]
- Seq2SQL: Generating Structured Queries from Natural Language using Reinforcement Learning [[arXiv](https://arxiv.org/pdf/1709.00103.pdf)]
- Generating Sentences by Editing Prototypes [[arXiv](https://arxiv.org/abs/1709.08878)]

#### 2017-08

- Towards an Automatic Turing Test: Learning to Evaluate Dialogue Responses [[arXiv](https://arxiv.org/abs/1708.07149)]
- Referenceless Quality Estimation for Natural Language Generation [[arXiv](https://arxiv.org/abs/1708.01759)]
- [Speech and Language Processing (3rd ed. draft). Dialog Systems and Chatbots and Advanced Dialog Systems chapters](notes/speech-and-text-book.md) [[Stanford](https://web.stanford.edu/~jurafsky/slp3/)]
- Machine Teaching: A New Paradigm for Building Machine Learning Systems [[arXiv](https://arxiv.org/abs/1707.06742v3)]

#### 2017-07

- [Learning Multilingual Joint Sentence Embeddings with Neural Machine Translation](notes/multilingual-sentence-embeddings.md) [[ACL](https://research.fb.com/wp-content/uploads/2017/08/multiling_repl4nlp17_fair.pdf)]

#### 2017-06

- [Deal or no deal? Training AI bots to negotiate](notes/negotiate.md) [[facebook blog](https://code.facebook.com/posts/1686672014972296/deal-or-no-deal-training-ai-bots-to-negotiate/)]

#### 2017-05

- Machine Comprehension by Text-to-Text Neural Question Generation [[arXiv](https://arxiv.org/abs/1705.02012)]
- TriviaQA: A Large Scale Dataset for Reading Comprehension and Question Answering [[Resource](http://nlp.cs.washington.edu/triviaqa/)]
- A Survey of Deep Learning Methods for Relation Extraction [[arXiv](https://arxiv.org/abs/1705.03645)]
- A Deep Reinforced Model for Abstractive Summarization [[arXiv](https://arxiv.org/abs/1705.04304)]
- Ask the Right Questions: Active Question Reformulation with Reinforcement Learning [[arXiv](https://arxiv.org/abs/1705.07830)]

#### 2017-04

-
    Composite task-completion dialogue policy learning via hierarchical deep reinforcement learning [[arXiv](https://arxiv.org/pdf/1704.03084)]
    <details><summary>+</summary>
    <p>
    Те же чуваки делали, примерно также как и в прошлой статье.
    Тоже goal oriented, но тут подробнее описали как тренировали стейт трекер.
    Причем его разделили на low-level, где на каждом ходу награда дается и на high-level
    где награда дается уже достижение большой цели.
    Ну и цель на подзадачи как-то разбили.
    </p>
    </details>

- Neural Question Generation from Text: A Preliminary Study [[arXiv](https://arxiv.org/abs/1704.01792)]
- Reading Wikipedia to Answer Open-Domain Questions [[arXiv](https://arxiv.org/abs/1704.00051)]
- SearchQA: A New Q&A Dataset Augmented with Context from a Search Engine [[arXiv](https://arxiv.org/abs/1704.05179)]

#### 2017-03

-
    Learning Conversational Systems that Interleave Task and Non-Task Content [[arXiv](https://arxiv.org/abs/1703.00099)]
    <details><summary>+</summary>
    <p>
    Тут в task-oriented систему примешивают chit-chat модуль, берут длинный контекст диалога и это дает им прирост как в user engagement так и в достижении цели.
    Мерили людьми по 50 диалогов (без chit-chat модуля, с ним, длинный и короткий контексты).
    В качестве симулятора использовали Alice (рестартили беседу, когда Алиса начинала повторяться).
    В качестве награды для RL использовали линейную комбинацию длины диалога, информативности и пары других эвристик.
    </p>
    </details>

-
    End-to-end task-completion neural dialogue systems [[arXiv](https://arxiv.org/pdf/1703.01008)]
    <details><summary>+</summary>
    <p>
    Тут разбирается task oriented система. Надо заполнить фрейм.
    Решают через end2end систему с RL. Для обучения использовали юзер симулятор.
    Также награду сразу давали, т.к. есть симулятор и это позволило решить проблему
    с отложенной наградой в диалогах.
    </p>
    </details>

- Massive Exploration of Neural Machine Translation Architectures [[arXiv](https://arxiv.org/abs/1703.03906), [github](https://github.com/google/seq2seq)]

#### 2017-01

- Cluster-Based Graphs for Conceiving Dialog Systems [[Paper](http://ceur-ws.org/Vol-1880/paper2.pdf)]

- Building machines that learn and think like people [[arXiv](https://arxiv.org/pdf/1604.00289)]
    <details><summary>+</summary>
    <p>
    Тут с точки зрения психологии и смежных наук сравнивается текущее состояние ИИ и интеллект человека.
    Как обычно пишут, что человек намного быстрее и эффективнее обучается.
    Говорят что это может быть связано с тем что у человека есть врожденные особенности.
    Типа уже к году человек примерно представляет физику (инерция скорость и тд),
    язык тоже очень быстро осваивает и тд.
    </p>
    </details>

-
    User involvement in collaborative decision-making dialog systems [[Springer](https://pdfs.semanticscholar.org/655a/)]
    <details><summary>+</summary>
    <p>
    Тут рассмотрен диалоговый агент как помощник и компаньон юзера.
    Такой collaborive-decision making process.
    Тут был использован классический подход, отдельная база знаний,
    planning framework, decision model (всякие эвристики).
    </p>
    </details>

- [Learning End-to-End Goal-Oriented Dialog](notes/end-to-end-goal.md) [[arXiv](https://arxiv.org/abs/1605.07683v3)]
- История развития ИИ. Проблемы этики искусственного интеллекта [[GitHub](notes/referat-yusupov.pdf)]

#### 2016-11

- Generative Deep Neural Networks for Dialogue: A Short Review [[arXiv](https://arxiv.org/abs/1611.06216)]

#### 2016-09

- [SQuAD: 100,000+ Questions for Machine Comprehension of Text](notes/squad.md) [[arXiv](https://arxiv.org/abs/1606.05250), [github](https://rajpurkar.github.io/SQuAD-explorer/), [review presentation](http://www.slideshare.net/sld7700/ss-75349426)]
- [Google's Neural Machine Translation System: Bridging the Gap between Human and Machine Translation](notes/gntm.md) [[arXiv]](https://arxiv.org/abs/1609.08144)

#### 2016-07

- [Representation learning for very short texts using weighted word embedding aggregation](notes/very-short-texts.md) [[arXiv](http://arxiv.org/abs/1607.00570)]

#### 2016-06

- Named Entity Recognition Using Syntactic and Semantic Features and Neural Networks [[Dialogue-21](http://www.dialog-21.ru/media/3475/yusupov.pdf)]
- [Dialog State Tracking Challenge 5 Handbook v3.1](notes/dstc5-hand.md) [[DSTC5](https://github.com/seokhwankim/dstc5/raw/master/docs/handbook_DSTC5.pdf)]
- Neural Belief Tracker: Data-Driven Dialogue State Tracking [[arXiv](https://arxiv.org/abs/1606.03777)]

#### 2016-05

- [Sentence Pair Scoring: Towards Unified Framework for Text Comprehension](notes/sentence-pair-scoring.md) [[arXiv](http://arxiv.org/abs/1603.06127)]
- [End-to-end Sequence Labeling via Bi-directional LSTM-CNNs-CRF](notes/seq-labeling.md) [[arXiv](https://arxiv.org/abs/1603.01354)]

#### 2016-03

- Generating Factoid Questions With Recurrent Neural Networks: The 30M Factoid Question-Answer Corpus [[arXiv](https://arxiv.org/abs/1603.06807), [corpora](http://agarciaduran.org), [review presentation](http://www.slideshare.net/sld7700/ss-75349426)]

#### 2016-02

- [A Roadmap towards Machine Intelligence](notes/a-roadmap-towards-mi.md) [[arXiv](http://arxiv.org/abs/1511.08130)]
  - [CommAI-env](notes/comm-ai.md) [[github](https://github.com/facebookresearch/CommAI-env)]

#### 2016

- [The Dialog State Tracking Challenge Series: A Review](notes/dstc-review.md) [[Dialogue & Discourse](http://dad.uni-bielefeld.de/index.php/dad/article/view/3685)]
- The Fourth Dialog State Tracking Challenge [[ResearchGate](https://www.researchgate.net/profile/Seokhwan_Kim4/publication/296223502_The_Fourth_Dialog_State_Tracking_Challenge/links/56d3b9ea08ae059e37612d24.pdf)]


#### 2015-12

- [A Survey of Available Corpora for Building Data-Driven Dialogue Systems](notes/corporas-for-ds-survey.md) [[arXiv](https://arxiv.org/abs/1512.05742)]
- [Towards AI-Complete Question Answering: A Set of Prerequisite Toy Tasks](notes/towards-ai-complete-question-answering.md)  [[arXiv](https://arxiv.org/abs/1502.05698)]


#### 2012

- Hierarchical Conversation Structure Prediction in Multi-Party Chat [[ACL](http://www.aclweb.org/anthology/W12-1607)]

#### 2001

- Разработка диалоговой системы с применением корпуса [[Dialog-21](http://www.dialog-21.ru/digest/2001/articles/koit/)]


#### 2003

- Основы теории дискурса [[Book](http://yanko.lib.ru/books/cultur/makarov-osnovu_teorii_diskursa-8l.pdf)]
- Corpus-based, Statistical Goal Recognition [[Paper](https://www.cs.rochester.edu/research/cisd/pubs/2003/blaylock-allen-ijcai2003.pdf)]

#### 2002

-
    Dialogue systems and planning [[Paper - ftp://ftp.irit.fr/pub/IRIT/CSC/tsd02.pdf]]
    <details><summary>+</summary>
    <p>
    Предложили вместо интентов и использовать план.
    Есть задача. Задача решается через достижение цели.
    Цель достигается посредством плана. План - это такой граф, где каждый узел это какое-то действие.
    План есть у юзера, у доменной области и у агента.
    </p>
    </details>



#### 2000

-
    A Plan Based Agent Architecture for Interpreting Natural Language Dialogue [[Paper](http://www.di.unito.it/~guido/articoli/98-ijhcs00.pdf)]
    <details><summary>+</summary>
    <p>
    Рассмотрен диалоговый агент построенный на базе дискурсного анализа и планирования.
    Речевые акты, модель агента и модель доменной области и т.д.
    </p>
    </details>


#### 1999

- Speech acts for dialogue agents [[Paper](http://www.math-info.univ-paris5.fr/~moraitis/webpapers/SpeechActs-Dialogues.pdf)]

#### 1994

- Chatterbots, tinymuds, and the turing test: Entering the loebner prize competition [[AAAI](http://www.aaai.org/Papers/AAAI/1994/AAAI94-003.pdf)]

#### Ссылки

- https://github.com/dennybritz/deeplearning-papernotes
- https://github.com/songrotek/Deep-Learning-Papers-Reading-Roadmap
- http://www.shortscience.org
- https://blog.openai.com
