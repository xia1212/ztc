Lab 12-1. RNN

![image](https://user-images.githubusercontent.com/79880336/136020909-82e0ecf0-393f-43f9-a65e-3bf77533b45b.png)


연속적인 데이터들의 의미를 파악하기 위해 기존의 NN/CNN 구조를 사용하는 것은 어려워서

따라서 이전의 연산 결과가 현재의 연산 결과에 영향을 미치는 신경망 구조를 만들게 되었는데, 

이를 RNN 이라고 한다.


![image](https://user-images.githubusercontent.com/79880336/136033269-bee77058-2d10-47db-b3b1-fe40ee2e557f.png)

RNN의 구조는 위의 그림과 같이 나타낼 수 있다.

연속적인 데이터들이 입력으로 들어가게 되고, 현재의 입력값에 대한 출력이 과거의 연산값에 영향을 받는 구조


![image](https://user-images.githubusercontent.com/79880336/136033458-ec1cb8ad-1ef4-4ff9-a22d-71b05071b8c3.png)


![image](https://user-images.githubusercontent.com/79880336/136033537-f6ce49a0-f65d-45b6-b396-e65f6cfb4c85.png)

위 그림은 RNN의 연산식을 나타낸 것이다.


현재의 입력값과 과거의 상태가 현재의 상태에 영향을 미치는 것을 알 수 있다.
 

계산 과정에서 쓰이는 fw(함수)와 파라미터들은 매 time step 마다 동일하다.
 
 
 ![image](https://user-images.githubusercontent.com/79880336/136033705-5fcbc468-7405-4ff9-ad1d-7682d3a190b8.png)


다양한 RNN
- one to one: 기본 RNN 구조
- one to many: ex) 이미지 설명 (이미지를 통해 문장을 만들어냄)
- many to one: ex) 감정 분석 (문장을 통해 감정을 분석)
- many to many 1: ex) 자동 번역 (문장을 다른 언어로 번역)
- many to many 2: ex) 비디오를 프레임 단위로 설명

# 모델 만들기

![image](https://user-images.githubusercontent.com/79880336/136398011-c7cf6435-9535-4321-b52d-ec5f510f607f.png)

language 모델 만들기

![image](https://user-images.githubusercontent.com/79880336/136398106-c0d359e4-ba42-48c8-b1c1-4ed501a3adc7.png)

RNN cell을 생성할때 원하는 종류를 선택할 수 있음

![image](https://user-images.githubusercontent.com/79880336/136398303-6cd539ae-8572-4251-aa61-25b820e3326b.png)

cell을 생성하였으면 cell을 동작시키는 코드가 필요

![image](https://user-images.githubusercontent.com/79880336/136398529-486275f4-6430-489b-bb69-e7491b74199f.png)

5개의 문자로 이루어진 단어이므로 hidden size는 5로 설정하고, 

input_dimension 또한 5로 설정한다.

하나의 단어만 학습해서 batch = 1 로 설정한다.

단어에서 마지막 부분은 들어갈 필요가 없으므로 6으로 설정한다.

## 최종

![image](https://user-images.githubusercontent.com/79880336/136398836-b6c779e6-02f7-4abd-b607-e3a6549b70ef.png)

