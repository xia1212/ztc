11-1. CNN introduction

고양이 실험에서 시작되었고,
하나의 이미지를 여러개의 컨볼루션 필터를 통해 서로 다른 특징점들을 뽑아내는 방법을 이용하였고,
ReLU와 Pooling 레이어를 조합한다.
마지막 부분에서는 분류를 위해 FC레이어를 붙여 사용한다.

컨볼루션 필터의 수는 Input 채널의 수와 동일해야 한다.
컨볼루션 연산을 통해 하나의 값을 만들어내게 된다.

Padding 기능을 사용하면 Input과 Output의 크기를 동일하게 유지할 수 있다.
Padding은 가장자리를 0으로 채워 컨볼루션 계산에 의한 크기 손실을 막는 역할을 한다.

11-2. CNN introduction: Max pooling and others

Pooling layer는 컨볼루션 레이어의 출력 값을 Sampling하는 레이어이다. (resize)

![image](https://user-images.githubusercontent.com/79880336/135083552-2131bd4b-73c3-497a-ac1d-58a6983ef9d6.png)

 2x2필터를 적용한 최대 풀 처리과정이다.

상단부터 하단까지 2만큼 이동하며 최대값을 뽑아낸다.

 이때 생성되는 출력의 크기는 필터의 크기와 stride에 따라 달라진다.

11-3. CNN case study

1. LeNET-5
2. AlexNet
3. GooleLeNet
4. NesNet
 
