# SVM 모델 (Support Vector Machines)

- 신경망에 비해 간결함

-분류나 회귀 분석에 사용가능하지만 주로 분류에 사용

-기본적으로 Hyperplane을 이용해서 분류

### Separating Hyperplane
 
![image](https://user-images.githubusercontent.com/79880336/112723318-2755f600-8f51-11eb-835e-157f90508427.png)

![image](https://user-images.githubusercontent.com/79880336/112723342-481e4b80-8f51-11eb-9d0a-c51d826e2f4b.png)

![image](https://user-images.githubusercontent.com/79880336/112723375-7bf97100-8f51-11eb-8d0c-3360c8768837.png)

- Hyperplane 을 찾는게 목적
- w, b 를 찾자
- Margin 을 최대한 하는 것을 찾자

#### Geometric Margin

![image](https://user-images.githubusercontent.com/79880336/112723416-b105c380-8f51-11eb-9aa8-642cb2e43487.png)

- 식으로 표현

![image](https://user-images.githubusercontent.com/79880336/112723475-0641d500-8f52-11eb-88c9-4cef6123a4cc.png)

![image](https://user-images.githubusercontent.com/79880336/112723493-25d8fd80-8f52-11eb-90e3-9bb8beabdda7.png)

- 최적화 (Convex Optimization Problem)

![image](https://user-images.githubusercontent.com/79880336/112723565-9aac3780-8f52-11eb-9dcd-1e29801edb36.png)

- Lagrangina Formulation

![image](https://user-images.githubusercontent.com/79880336/112723658-0b535400-8f53-11eb-8c7e-d5a7d9284ebe.png)

- Lagrangina Dual
(목적식과 제약식을 하나로 만들기)

![image](https://user-images.githubusercontent.com/79880336/112724019-aef13400-8f54-11eb-9358-19d85bbde821.png)
 
![image](https://user-images.githubusercontent.com/79880336/112723736-62f1bf80-8f53-11eb-8fb6-2cb2887f13d7.png)

![image](https://user-images.githubusercontent.com/79880336/112723748-7735bc80-8f53-11eb-95eb-77e527630c74.png)

### Classifying New Data Points

![image](https://user-images.githubusercontent.com/79880336/112723864-f6c38b80-8f53-11eb-96de-08c3fb86ed16.png)

![image](https://user-images.githubusercontent.com/79880336/112723884-093dc500-8f54-11eb-9a17-4df597f332c5.png)



