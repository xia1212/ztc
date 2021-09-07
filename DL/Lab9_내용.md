![image](https://user-images.githubusercontent.com/79880336/132367389-a21f84c6-4d14-494c-a373-22df2556366b.png)


각각은 logistic regression으로 두 개 중에서 하나만 선택할 수 있다. 
logistic regression 한 개만 사용해서는 XOR 문제를 해결할 수 없지만, 
그림처럼 3개를 연결해서 사용한다면 가능하다고 설명하고 있다. 어떻게 보면 이 부분이 Neural Network의 핵심일 수 있다. 기존의 방식을 연결해서 사용하는 거.


![image](https://user-images.githubusercontent.com/79880336/132367523-ef5dc5e4-ea47-439d-af99-5c74c6293f8d.png)
최초의 x1과 x2는 두 개의 logistic regression에 전달되고, 이들의 계산 결과를 마지막 logistic regression의 입력으로 전달
