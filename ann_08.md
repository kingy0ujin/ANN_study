# 활성화 함수
## 1. 단극성 시그모이드 함수(파이썬 코드로 살펴보기)

```python
import numpy as np
import matplotlib.pyplot as plt

def sigmoid_function(lamda, z):
  y = 1 / (1 + np.exp(-lamda * z))
  return y
z_range = np.arange(-6, 6, 0.1) #-6이상 6미만의 수, 0.1 간격으로

plt.figure()
plt.plot(z_range, sigmoid_function(1,z_range), label='lamda=1')
plt.plot(z_range, sigmoid_function(2,z_range), label='lamda=2')
plt.plot(z_range, sigmoid_function(5,z_range), label='lamda=5')
plt.xlabel('z')
plt.ylabel('f(z)')
plt.grid(True)
plt.legend()
plt.show()
```
## 2. 양극성 시그모이드 함수(파이썬 코드로 살펴보기)

```python
import numpy as np
import matplotlib.pyplot as plt

def sigmoid_function(z):
  y = (1 - np.exp(-z)) / (1 + np.exp(-z))
  return y

z_range = np.arange(-6, 6, 0.1) #-6이상 6미만의 수, 0.1 간격으로

plt.figure()
plt.plot(z_range, sigmoid_function(z_range))
plt.xlabel('z')
plt.ylabel('f(z)')
plt.grid(True)
plt.show()
```
