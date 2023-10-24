# 다층 신경망을 이용한 패턴 분류기, 파이썬 언어로 살펴보기

### 4개의 패턴을 2가지 클래스로 분류하는 신경망 분류기 설계하기
* 판단면을 2개 이상 사용하는 경우, 다층 신경망으로 해결


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
x = np.array([[1,1,1], [1,0,1], [0,1,1],[0,0,1]])
w1 = np.array([-1, 1, -0.5]).reshape([3,1])
w2 = np.array([-1,1,0.5]).reshape([3,1])
w3 = np.array([1,-1,1]).reshape([3,1])

for i in range(4):
    h1 = step_function(x[i].dot(w1))
    h2 = step_function(x[i].dot(w2))
    
    y = step_function(np.dot([h1,h2,1],w3))
    print(y)
```
