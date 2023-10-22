# 신경망 모델, 파이썬 코드로 살펴보기
### 1. 임계치가 2인 계단 함수가 활성화 함수로 사용될 때, 아래 뉴런의 출력은?

```python
def step_function(z)
  T = 2 #임계치
    if z >= T:
      y = 1
    elif z < T
      y = 0
    
  return y
  x1 = 1
  x2 = 2
  w1 = 0.8
  w2 = 0.5
    
  z = w1 * x1 + w2 * x2
  y = step_fluction(z)
  print(y)
```
실행결과 : 0

### 2. 임계치가 1인 계단 함수가 활성화 함수로 사용될 때, 아래 뉴런의 출력은?

```python
def step_function(z)
  T = 1 #임계치
    if z >= T:
      y = 1
    elif z < T
      y = 0
    
  return y
  x1 = 2
  x2 = 1
  w1 = 0.8
  w2 = -0.5
  b = 0.3 #바이어스(편견)

  z = w1 * x1 + w2 * x2 + b
  y = step_fluction(z)
  print(y)
```
실행결과 : 1
