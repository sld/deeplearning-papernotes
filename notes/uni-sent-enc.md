- Ссылка на статью: [[arXiv](https://arxiv.org/abs/1803.11175)]

1. 
	Обучаем multi-task сетку. 

	```
	The supported tasks include: a Skip- Thought like task (Kiros et al., 2015) for the un- supervised learning from arbitrary running text; a conversational input-response task for the in- clusion of parsed conversational data (Henderson et al., 2017); and classification tasks for train- ing on supervised data. The Skip-Thought task replaces the LSTM (Hochreiter and Schmidhu- ber, 1997) used in the original formulation with a model based on the Transformer architecture.
	```

	Обучающие данные:

	```
	Unsupervised training data for the sentence en- coding models are drawn from a variety of web sources. The sources are Wikipedia, web news, web question-answer pages and discussion fo- rums. We augment unsupervised learning with training on supervised data from the Stanford Nat- ural Language Inference (SNLI) corpus (Bowman et al., 2015). Similar to the findings of Conneau et al. (2017), we observe that training to SNLI im- proves transfer performance.
	```

2. 
	Используем hidden-state обученной multi-task сетки как энкодер предложений. 
	В результате можно считать близость между предожениями используя косинусную или angular distance. 
3. 
	Также можно использовать эмбеддинги полученные от нее для transfer learning.
	Заметно улучшает качество на целевой задаче.
4. Энкодер доступен на tfhub.