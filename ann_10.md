# 단층 신경망을 이용한 패턴 분류기, 파이썬 코드로 살펴보기 🖥️

### 단층신경망을 활용하여 두 패턴을 분류할 수 있는 분류기 설계하기
 1. 양극성 데이터로 표현 -> 활성화 함수는 양극성 계단함수 사용
 2. 패턴 공간에 점으로 표현
 3. 패턴 1,2를 분류할 판단면(판단경계선) 구하기
 4. 판단면으로 가중치 구하기????
 5. 단층 신경망 설계 후 검증

 ```python
import numpy as np

def step_function(z):
    T = 0
    if z > T:
        y = 1
    elif z == T:
        y = 0
    elif z < T:
        y = -1
        
    return y

x = np.array([[1,1,1],[-1,-1,1]])
w = np.array([1,1,0]).reshape([3,1])

print(step_function(x[0].dot(w)))
print(step_function(x[1].dot(w)))
```

실행결과 : 1  -1 
<hr>

### 단층신경망을 활용하여 4개의 패턴을 2가지 클래스로 분류할 수 있는 신경망 분류기 설계하기

```python

import numpy as np

def step_function(z): #단극성 계단함수임
    T = 0
    if z >= T:
        y = 1
    elif z < T:
        y = 0
        
    return y

x = np.array([[1,1,1],[1,0,1],[0,1,1],[0,0,1]])
w = np.array([1,1,-1.5]).reshape([3,1])

print(step_function(x[0].dot(w)))
print(step_function(x[1].dot(w)))
print(step_function(np.dot(x[2],w)))
print(step_function(np.dot(x[3],w)))
```
실행결과 : 1 0 0 0
