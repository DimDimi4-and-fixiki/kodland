## Home Task for `functions`  

### 1. Make a function to check whether the number is prime  
```python
def isPrime(N):
    # We go from 2 to N - 1
    for i in range(2, N):
        # N divides by i with no remainder
        if N % i == 0:
            # Number is not prime
            return 0
            break
    # Number is not prime after we checked all the numbers
    return 1
```  

### 2. Function for making a circle  
```python
def circle():
    t = Turtle()
    for i in range(0,20,1):
        t.forward(5)
        t.left(18)
```  

### 3. Function for finding the maximum element in the list  
```python
def printMax(list):
    
    # we will start with the first element in the list
    maximum = list[0]
    for element in list:
        # If we found the elemnt which is bigger than a current maximum
        if element > maximum:
            maximum = element
    print(maximum)
```