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

- Why n-gram?
: Bag of words 의 단점을 극복
: 다음 단어 예측 (Naive Next word prediction)

# 3.TF-IDF

- What is TF-IDF?
: Term Frequency * Inverse Document Frequency

- Why TF-IDF?
: To find how relevant a term is in a document (문서의 연관성을 알아보고 싶을 때 사용)

- TF 단점
: 자주 출현하는 단어에 연관성 높아짐

# 4. 자연어처리의 유사도 측정 방법(거리측정,코사인 유사도)

- How to check similarity in vector space?
: Euclidean Distance (유클리디안 거리)
: Cosine Similarity


- cosine similarity
: 각도가 좁을수록 유사도가 높다

- Can angle be greater than 90?
: 코사인 유사도는 90보다 높을 수 없다. (마이너스로 갈 수 없다)

# 5. TF-IDF 문서유사도 측정

- 유사도 측정방법에는 두가지 방법이 있음

- Advantage of TF-IDF bag of words (장점)
: Easy to get document similarity (구현하기 쉽다)
: Keep relevant words score (중요한 단어에 점수 유지)
: lower just frequent words score 

- Drawback of TF-IDF bag of words (단점)
: Only based on Terms(words) (단어만 보고, 속에 있는 유사도는 안봄)
: Weak on capturing document topic (단어 파악이 안됨)
: Weak handling synonym (different words but same meaning)

- How to overcome Drawbacks of TF-IDF?
: LSA (Latent Semantic Analysis)
: Word Embeddings (Word2Vec, Glove)
: conceptNet

# 6. 잠재 의미분석(LSA, Latent Semantic Analysis)

- TF-IDF or Bag of Words : 피자 / 햄버거 유사도 0 
-> TF-IDF or Bag of Words similarity is based on word 
(= TF-IDF or Bag of Words similarity is not based on topic)

- LSA similatiy is based on topic
