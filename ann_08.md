# 시그모이드 함수, 파이썬 코드로 살펴보기
## 1. 단극성 시그모이드 함수

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
<img width="445" alt="20231023_175542" src="https://github.com/kingy0ujin/ANN_study/assets/127166629/a882e7a5-785c-4429-b808-2686c841edb8">

## 2. 양극성 시그모이드 함수

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
<img width="448" alt="20231023_180934" src="https://github.com/kingy0ujin/ANN_study/assets/127166629/b105dd2b-9b7e-4d2a-a419-cd2246ba3cff">
