### The rook assignment  

#### It is possible to move if 
- **Two cells are on the same row**
- **Two cells are on the same column**  
#### So we can go with:  
```python
# Firstly, lets input the cordinates
a = int(input("the column number of the first cell"))
b = int(input("the row number of the first cell"))
c = int(input("the column number of the second cell"))
d = int(input("the row number of the second cell"))

# Checks the same row or column:
if 1 <= c <= 8 and d == b:
    print("The rook can go to this coordinate")
elif 1 <= d <= 8 and c == a:
    print("The rook can go to this coordinate.")
else:
    print("The rook can't go to this coordinate")
```  

### The queen assignment  
#### There is the same idea that we had with the rook, but we also should handle the horizontal movements and to check it we go with `abs(a - c) == abs(b - d)`, where `abs() function gives you an absolute value of the number`  

```python
# Firstly, lets input the cordinates
a = int(input("the column number of the first cell"))
b = int(input("the row number of the first cell"))
c = int(input("the column number of the second cell"))
d = int(input("the row number of the second cell"))
# Checks the same row or column or diagonal:
if abs(a-c) == abs(b-d) or a == c or b == d:
    print("The queen can go to this coordinate.")
else:
    print("The queen can't go to this coordinate")
```