# GRU 개요
: GRU 는 LSTM 구조와 비슷하지만, 더 간단한 구조여서 계산상 이점이 있음

![image](https://user-images.githubusercontent.com/79880336/145045070-ef0907a4-faa3-4998-a3ed-1ffe7b48873e.png)

: LSTM 는 Cell state 가 있지만 GRU에는 Cell state 가 없음 (H가 Cell state 를 대신함)
: GRU는 활성화 함수가 5개 -> 3개로 줄어서 연상량을 줄일 수 있음

# GRU 구조

## Reset Gate
: 과거의 정보를 얼마나 잊을지(또는 기억할지) 결정하는 게이트
: 현 시점의 데이터 x와 과거의 은닉층 값 H 에 각각의 가중치 W,U 곱하여 더한 후에 시그모이드 함수 적용

![image](https://user-images.githubusercontent.com/79880336/145046040-59e4e2e3-b300-4b30-b611-1f923235227b.png)


## Update Gate
: 과거와 현재의 정보가운데 어떤 정보를 더 많이 업데이트 할지를 결정하는 게이트
: Update Gate 는 LSTM 의 Input Gate 와 Forget Gate를 합쳐놓은 개념 

![image](https://user-images.githubusercontent.com/79880336/145046473-10cfe71c-6531-41ea-b64f-fe62de945432.png)


## Candidate (데이터 선정)
: 다음 시점으로 전달해줄 데이터 Ht를 만들기 위해, 현재 시점의 데이터를 선정하는 단계

![image](https://user-images.githubusercontent.com/79880336/145046929-d978bb61-4cbe-4110-b398-3efa5e82dad4.png)


## Output (출력 값 계산)
 : 수식의 Ut 부분은 현재 시점의 데이터 중 얼마나 가져갈 것인지를 나타내며, 1-Ut 부분은 얼마나 잊을지를 나타냄
 
  
 # GRU summary
 
 ![image](https://user-images.githubusercontent.com/79880336/145048141-b74072a2-945e-4363-9bb7-72c71521e628.png)

