# RNN (순환 신경망)

: 순환 신경망(Recurrent Neural Network)은 은닉 계층 안에 하나 이상의 순환 계층을 갖는 신경망

## 순환 계층
- 시계열 데이터 처리에 알맞게 고안된 퍼셉트론 계층입니다.
- 가중치와 편향을 각 시간대 데이터에 반복해서 사용합니다.
- 순환 벡터를 사용하여 정보를 전달합니다.

# RNN 구조

![image](https://user-images.githubusercontent.com/79880336/144062577-3c4b5cfa-8779-4a2e-9c65-44f99503bbb7.png)

- RNN은 되먹임 구조를 가지고 있고, 레이어의 출력을 다시 입력으로 받아서 사용하는 것으로서, 이전의 데이터가 함께 결과에 영향을 미친다
- RNN은 입력과 출력의 길이에 제한이 없다는 특징이 있어서, 구조를 바꾸면 다양한 형태, 스타일의 네트워크를 형성할 수 있습니다.
- 기본적으로 Fully connected 구조


# RNN 파라미터

- units 파라미터는 RNN 신경망에 존재하는 뉴런의 개수입니다.

![image](https://user-images.githubusercontent.com/79880336/144063398-022c924d-d822-47e6-ab61-6392fe473784.png)


- return_sequences
: RNN 계산 과정에 있는 hidden state를 출력할 것인지에 대한 값을 의미
: 해당 값은 다층으로 이루어진 RNN 또는 one-to-many, many-to-many 출력을 위해서 사용된다

![image](https://user-images.githubusercontent.com/79880336/144063541-2c25377f-87ed-4d7d-a3e5-03250d96a8d9.png)

- return_state
: LSTM 레이어에서 주로 사용되는 값으로, cell_state를 출력할 것인지를 결정하는 값입니다.

- activation
: 활성화 함수를 선언하는 변수입니다. tanh, relu 등과 같은 함수를 사용할 수 있습니다.

# RNN 종류

- SimpleRNN 구조
가장 간단한 형태의 RNN 레이어입니다. 구조는 아래의 그림과 같습니다.

![image](https://user-images.githubusercontent.com/79880336/144063922-fd9cb9de-4852-4072-b73a-610819f8c0cb.png)

- SimpleRNN in Tensorflow 2.0
