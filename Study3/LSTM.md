# RNN의 문제점 : 장기 의존성

## 
기존의 RNN은 단점이 있습니다. 
입력 데이터가 커지면, 학습 능력이 저하되고, 데이터의 뒤쪽으로 갈수록, 앞쪽의 입력 데이터를 까먹게 된다.
입력 데이터와 출력 데이터 사이의 길이가 멀어질수록 연관 관계가 줄어들어서 이를 장기 의존성(Long-Term Dependency)문제 라고 한다.

![image](https://user-images.githubusercontent.com/79880336/144055686-d2060890-e758-465c-adc1-4efda1f52db6.png)


# 장기 의존성 문제를 해결하기위해서 제안된 RNN의 변형 구조가 바로 LSTM

![image](https://user-images.githubusercontent.com/79880336/144056699-24942275-f727-4d99-b0ad-003f9edb51e3.png)


![image](https://user-images.githubusercontent.com/79880336/144056827-a2ba978f-2925-4bec-bfa2-1d7f8b00c1e6.png)


## 활성화 함수 종류
- tanh: 기존의 RNN에서 사용되는 활성화 함수, 해당 함수는 relu로 대체될 수 있습니다.
- sigmoid: 정보가 0과 1 사이에서 얼마나 통과할지를 결정하는 함수입니다.

![image](https://user-images.githubusercontent.com/79880336/144057642-b7f4db78-144d-4210-a18c-8eb11c203ea2.png)


위의 그림처럼 LSTM 레이어는 Forget Gate, Input Gate, Output Gate라는 c(cell state)의 값을 제어하는 게이트들이 존재한다.

각 게이트들은 sigmoid layer와 pointwise곱 연산을 통해서 값을 제어합니다.

각각의 게이트들은 cell state를 보호하고 제어하는 역할을 합니다.

- Forget gate layer
: 얼마나 잊어버릴지에 대한 가중치를 사용하여 잊어버리기로 정한 것을 실제로 잊는 게이트
이전 state c에 forget gate 출력 값을 곱해서 state를 업데이트합니다. 또한 input 게이트를 통해 나온 출력 값들을 곱하여 state에 더합니다.

- Input gate layer
: sigmoid layer가 새로운 정보 중에 어떤 것을 cell state에 담을 것인지를 결정하는 게이트
그 다음으로 tanh layer에서 새로운 데이터의 후보 값을 만들어냅니다. 이것을 cell layer에 합칠 준비를 합니다.

- Output gate layer
: 어떤 값을 출력할지를 결정하는 게이트
cell state의 어떤 부분을 출력할 지를 정하는 것이 바로 게이트의 sigmoid layer입니다.
cell state를 tanh 하여 나온 -1과 1 사이의 값을 sigmoid 출력 값과 곱하여 최종 출력 값을 연산합니다.
