# 1. Bag of words

![image](https://user-images.githubusercontent.com/79880336/149944938-e0f3fe9b-a737-450f-88fa-fbc7eb90251d.png)

![image](https://user-images.githubusercontent.com/79880336/149944980-be6a7c12-058e-4829-a56e-cb3d3b26f98f.png)

- 문장의 유사도 (Sentence similarity)

![image](https://user-images.githubusercontent.com/79880336/149945011-5868a680-1533-4a19-b181-bdfa61b8c5a5.png)

![image](https://user-images.githubusercontent.com/79880336/149945101-b937f5da-d535-4f53-a08a-5d143e4ebb84.png)

- Limitation (단점)
1. Sparsity (학습량이 많아진다)
2. Frequent words has more power (많이 나오던 단어에 힘이 커진다)
3. ignoring word orders (순서 무시하고, 문맥이 무시된다)
4. out of vocabulary (오타)


# 2. n-그램

- What is n-gram? 
: contiguous sequence of N tokens (words, characters,...)

2-1. 1-gram (unigram)

![image](https://user-images.githubusercontent.com/79880336/149945416-1cbccca7-d5ef-4bef-8670-5f8f3e87db01.png)

2-2. 2-gram (bigram)
- 2개의 단어가 하나의 묶음

![image](https://user-images.githubusercontent.com/79880336/149945460-7d94cd9a-77fe-468e-8c53-40b2cbd121b8.png)

2-3. 3-gram (trigram)

![image](https://user-images.githubusercontent.com/79880336/149945526-2b64d890-c88d-43b8-b6c2-c435e3f11bfb.png)

- Why n-gram?
1. Bag of words 의 단점을 극복
2. 다음 단어 예측 (Naive Next word prediction)
3. 오타 발견

![image](https://user-images.githubusercontent.com/79880336/149945613-301a6bca-d11e-4dc8-9ccd-d76496c326d5.png)

- bag of words 단점
: bag of words ignore word sequence

![image](https://user-images.githubusercontent.com/79880336/149945836-05e4abc0-d98a-4154-bb58-e6d03c29f041.png)

- bigram 사용

![image](https://user-images.githubusercontent.com/79880336/149945977-2351f8c0-07d0-4c07-8c72-7348d9667a7e.png)

- Naive Next word prediction
- Navie Spell checker

# 3.TF-IDF

- What is TF-IDF?
: Term Frequency * Inverse Document Frequency

- Why TF-IDF?
: To find how relevant a term is in a document (문서의 연관성을 알아보고 싶을 때 사용)

- What is Term Frequency?
: 문서에 몇번 출현했는지
![image](https://user-images.githubusercontent.com/79880336/149947313-649fa461-e097-4028-b8ef-5c8617954954.png)
 
![image](https://user-images.githubusercontent.com/79880336/149947509-3ba7a84e-b474-44df-b329-9aa6fd52ce52.png)

- TF 단점
: 자주 출현하는 단어에 연관성 높아짐

- What is IDF?

![image](https://user-images.githubusercontent.com/79880336/149948010-ebbbcf90-2047-4819-8af0-c65c1211950e.png)

- IDF score

![image](https://user-images.githubusercontent.com/79880336/149948266-cf4cb446-0017-46b6-929b-2e14607fc954.png)


- TF-IDF score

![image](https://user-images.githubusercontent.com/79880336/149948167-f980db22-57b1-428f-9e6a-14552e4de1a7.png)

: 문서나 문장이 주어졌을 때 연관성 분석

# 4. 자연어처리의 유사도 측정 방법(거리측정,코사인 유사도)

- How to check similarity in vector space?
1. Euclidean Distance (유클리디안 거리)
2. Cosine Similarity

- Euclidean Distance
: 거리가 짧을수록 유사도가 높다 

![image](https://user-images.githubusercontent.com/79880336/149948575-74f32399-1491-492a-9bc3-f16fa976d87f.png)

 - cosine similarity
: 각도가 좁을수록 유사도가 높다

![image](https://user-images.githubusercontent.com/79880336/149948957-804973de-cffe-4420-8770-319cea91ba2b.png)

- Can angle be greater than 90?
: 코사인 유사도는 90보다 높을 수 없다. (마이너스로 갈 수 없다)

![image](https://user-images.githubusercontent.com/79880336/149949257-1410e799-5dd1-4f71-a686-2cc103e98f2f.png)


# 5. TF-IDF 문서유사도 측정

- 유사도 측정방법에는 두가지 방법이 있음

![image](https://user-images.githubusercontent.com/79880336/149949333-638a0faf-3594-41b3-8fb0-227bd55014b2.png)

- Advantage of TF-IDF bag of words (장점)
1. Easy to get document similarity (구현하기 쉽다)
2. Keep relevant words score (중요한 단어에 점수 유지)
3. lower just frequent words score 

- Drawback of TF-IDF bag of words (단점)
1. Only based on Terms(words) (단어만 보고, 속에 있는 유사도는 안봄)
2. Weak on capturing document topic (단어 파악이 안됨)
3. Weak handling synonym (different words but same meaning)

- How to overcome Drawbacks of TF-IDF?
1. LSA (Latent Semantic Analysis)
2. Word Embeddings (Word2Vec, Glove)
3. conceptNet

# 6. 잠재 의미분석(LSA, Latent Semantic Analysis)

- TF-IDF or Bag of Words : 피자 / 햄버거 유사도 0 

- 유사도가 0 , Why? 
TF-IDF or Bag of Words similarity is based on word 
(= TF-IDF or Bag of Words similarity is not based on topic)

- LSA similatiy is based on topic

![image](https://user-images.githubusercontent.com/79880336/149950214-9f7e9e4a-dbfa-4d6d-800a-4d35a7e1f3c1.png)

![image](https://user-images.githubusercontent.com/79880336/149950247-6119020e-3d34-4468-8880-fcf5310f3a6c.png)

![image](https://user-images.githubusercontent.com/79880336/149949992-ff373ac9-b272-4a63-9a73-1a61e09b2443.png)

![image](https://user-images.githubusercontent.com/79880336/149950945-840bc10b-a931-4b73-a825-e414021fd655.png)

![image](https://user-images.githubusercontent.com/79880336/149950986-4ae7707f-8846-4c88-adf3-735a5d0da8da.png)

![image](https://user-images.githubusercontent.com/79880336/149951067-d6db335e-c376-4cac-a0de-cb1f717a6f5a.png)



