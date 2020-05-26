## Homework_#5

| 20171621 민대인 |
| --------------: |
|                 |

| 문번 |                             문번                             |
| :--: | :----------------------------------------------------------: |
|  1   | 수치해석 수업시간 때 문제를 풀던 철수는 이분법을 복습해보고자, 번지점프 예제를 짜보았다.  다음,  (A) 와 (B)에 들어갈 것으로 알맞은 것을 고르시오. |

```python
import matplotlib.pyplot as plt
import numpy as np

def bisect(func, xl, xu):
    maxit=100
    es=1.0e-4
    test=func(xl)*func(xu)
    
    if(test>0):
        print('No sign change')
        return [], [], [], []
    
    iter=0
    xr=xl
    
    ea=100
    
    while(1):
        xrold=xr
        xr= [                          (A)                          ]
        iter=iter+1
        
        if xr != 0:
            ea=np.float(np.abs(np.float(xr)-np.float(xrold))/np.float(xr))*100
            test= [                        (B)                          ]
            if test > 0:
                xl=xr
            elif test < 0:
                xu=xr
            else:
                ea=0
            if np.int(ea<es) | np.int(iter >= maxit):
                break
        root=xr
        fx=func(xr)
        
    return root, fx, ea, iter

if __name__== '__main__':
    fm=lambda m: x**3 +
    root, fx, ea, iter=bisect(fm, 40, 200)
    print('root = ', root, '(Bisection)')
    print('f(root) = ', fx, '(must be zero, Bisection)')
    print('estimated error= ', ea, '(must be zero error, Bisection)')
    print('iterated number to find root =', iter, '(Bisection)')
    m=np.linspace(40,200)
    k=m*0
    plt.ylim(-6,6)
    plt.xlim(40,200)
    fm = np.sqrt(9.81*m/0.25)*np.tanh( np.sqrt(9.81*0.25/m)*4 )-36
    plt.plot(m, fm, m, k, 'black')
    
    plt.grid()
    plt.show()
```

1.   (A) np.float((xl+xu)/2)    ,      (B) func(xl)*func(xr)
2.   (A) np.float((xl+xu)/2)    ,      (B) func(xrold)*func(xr)
3.   (A) np.float((xl+xu)/2)    ,      (B) func(xl)*func(xrold)
4.   (A) np.float((xl+xr)/2)    ,      (B) func(xrold)*func(xr)
5.   (A) np.float((xr+xu)/2)    ,      (B) func(xl)*func(xr)



|      |      |
| ---- | ---- |
| 2    |      |

$$
x = {2v^2sin 45 * cos 45\over g}
$$

$$
x = 수평 도달거리
$$

$$
g =9.8
$$

$$
v= 최적의 속도
$$

