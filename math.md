
+ [Base 7](#base-7)
+ [Palindrome Number](#palindrome-number)
+ [Fibonacci Number](#)
+ [Fizz Buzz](#)
+ [Largest Perimeter Triangle](#)
+ [Sqrt(x)](#)
+ [Reverse Integer](#)
<!-----solution----->

## Reverse Integer



```python

def reverse(self, x: int) -> int:
    x_str = str(x)
    if x >= 0:
        x_reverse = x_str[::-1]
    else:
        x_no_sign = x_str[1::]
        x_reverse = "-" + x_no_sign[::-1]
    if int(x_reverse) <= -2**31 or int(x_reverse) >= 2**31-1:
        return 0
    else:
        return int(x_reverse)
```

## Sqrt(x)



```python
    def mySqrt(self, x: int) -> int:
        l = 1
        r = x
        while l <= r:
            mid = (l + r) // 2
            if mid * mid <= x:
                l = mid + 1
            else:
                r = mid - 1
                
        return l - 1
```

## Largest Perimeter Triangle



```python

def largestPerimeter(self, A: List[int]) -> int:
    A.sort()
    for i in range(len(A) - 2):
        if A[i+1] + A[i+2] > A[i]:
            return A[i] + A[i+1] + A[i+2]
return 0
```

## Fizz Buzz



```python

def fizzBuzz(self, n: int) -> List[str]:
    list = []
    for i in range(1, n+1):
        if i % 3 == 0 and i % 5 != 0:
            list.append('Fizz')
        elif i % 5 == 0 and i % 3 != 0:
            list.append('Buzz')
        elif i % 3 == 0 and i % 5 == 0:
            list.append('FizzBuzz')
        else:
            list.append(str(i))
return list
```

## Fibonacci Number



```python

def fib(self, N: int) -> int:
    if N <= 1:
        return N
return self.fib(N - 1) + self.fib(N - 2)
```


## Palindrome Number

https://leetcode.com/problems/palindrome-number/

```python
s = input()
i, j = 0, len(s) - 1
for i in range(len(s)):
  if s[i] != s[j]:
    print("No")
    break
  else:
    j -= 1
else:
  print("Yes")
```

## Base 7

https://leetcode.com/problems/base-7/

```python
def convertToBase7(self, n: int) -> str:
base_seven = []
min_sign = False
if n == 0:
    return '0'
if n < 0:
    min_sign = True
    n = -n
while n > 0:
    base_seven.append(str(n % 7))
    n //= 7
if min_sign:
    return '-' + ''.join(base_seven[::-1])
return ''.join(base_seven[::-1])
```


```