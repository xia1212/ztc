# 1. Bag of words

- 문장의 유사도 (Sentence similarity)


- 단점 (Limitation)
- Sparsity (학습량이 많아진다)
- Frequent words has more power (많이 나오던 단어에 힘이 커진다)
- ignoring word orders (순서 무시하고, 문맥이 무시된다)
- out of vocabulary (오타)


# 2. n-그램

- What is n-gram? 
: contiguous sequence of N tokens (words, characters,...)

2-1. 1-gram (unigram)

2-2. 2-gram (bigram)
- 2개의 단어가 하나의 묶음

2-3. 3-gram (trigram)

Why n-gram?
Bag of words 의 단점을 극복
다음 단어 예측 (Naive Next word prediction)

# 3.TF-IDF

- What is TF-IDF?
: Term Frequency * Inverse Document Frequency

- Why TF-IDF?
: To find how relevant a term is in a document (문서의 연관성을 알아보고 싶을 때 사용)

- TF 단점
: 자주 출현하는 단어에 연관성 높아짐

# 4. 자연어처리의 유사도 측정 방법(거리측정,코사인 유사도)



