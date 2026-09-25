# Python Unit 2 Assignment

### 1. String to Integer

```python
x = "25"
x = int(x)
print(x, type(x))
```

### 2. String to Float

```python
x = "75.5"
x = float(x)
print(x, type(x))
```

### 3. Integer to Float

```python
x = 50
x = float(x)
print(x, type(x))
```

### 4. Float to Integer

```python
x = 85.9
x = int(x)
print(x, type(x)) # 85, decimal is removed
```

### 5. Integer to String

```python
x = 101
x = str(x)
print(x, type(x))
```

### 6. Multiple Conversions

```python
a=int("18"); b=float("92.5"); c=str(100); d=int(45.8)
print(a,b,c,d)
```

### 7. Predict Output

```python
a=int("20"); c=int(10.8); e=str(25)
print(a,c,e)
# 20 10 25
```

### 8. Debug

```python
x = "19"
print(int(x) + 1) # 20
```

### 9. Bonus

```python
bonus = "85"
print(int(bonus) + 5) # 90
```

### 10. Delivery

```python
price="1499.50"; delivery=99.50
print(float(price)+delivery) # 1599.0
```

### 11. Arithmetic Operators

```python
a=20; b=6
print(a+b,a-b,a*b,a/b,a//b,a%b,a**b)
# 26 14 120 3.3333333333333335 3 2 64000000
```

### 12. Division

```python
print(17/5,17//5,17%5)
# 3.4 3 2
# / = normal division, // = whole number, % = remainder
```

### 13. Precedence

```python
print(10+5*2) # 20
print((10+5)*2) # 30
```

### 14. Precedence

```python
print(20-4*3+2) # 10
print((20-4)*(3+2)) # 80
```

### 15. Power and Square

```python
print(2**3,3**2,10**2)
side=5
print(side**2) # 25
```

### 16. Shopping

```python
print(80+20+10) # 110
```

### 17. Shopping

```python
print(3*50,2*15,1*500)
print(3*50+2*15+500) # 680
```

### 18. Groups

```python
students=47
print(students//5,students%5) # 9, 2
```

### 19. Marks

```python
marks=[85,78,92]
print(sum(marks),sum(marks)/3) # 255, 85
```

### 20. Percentage

```python
marks=[78,85,92,81,74]
total=sum(marks)
print(total,total/5,total/500*100) # 410,82,82
```

### 21. Ones Digit

```python
n=583
print(n%10) # 3
```

### 22. Tens Digit

```python
n=583
print((n//10)%10) # 8
```

### 23. Hundreds Digit

```python
n=583
print(n//100) # 5
```

### 24. Digits of 746

```python
n=746
print(n//100,(n//10)%10,n%10) # 7 4 6
```

### 25. Digits of 5829

```python
n=5829
print(n//1000,(n//100)%10,(n//10)%10,n%10) # 5 8 2 9
```

### 26. Sum of 583

```python
n=583
print(n//100+(n//10)%10+n%10) # 16
```

### 27. Sum of 4726

```python
n=4726
print(n//1000+(n//100)%10+(n//10)%10+n%10) # 19
```

### 28. Product of 234

```python
n=234
print((n//100)*((n//10)%10)*(n%10)) # 24
```

### 29. Reverse 583

```python
n=583
print(n%10*100+(n//10)%10*10+n//100) # 385
```

### 30. Reverse 4726

```python
n=4726
print(n%10*1000+(n//10)%10*100+(n//100)%10*10+n//1000) # 6274
```

### 31. Place Values

```python
n=5834
print(n//1000*1000,(n//100)%10*100,(n//10)%10*10,n%10)
# 5000 800 30 4
```

### 32. First and Last Difference

```python
n=583
print(abs(n//100-n%10)) # 2
```

### 33. Debug Ones Digit

```python
number=583
print(number%10) # 3
```

### 34. Digits of 9365

```python
n=9365
print(n//1000,(n//100)%10,(n//10)%10,n%10) # 9 3 6 5
```

### 35. Build 583

```python
h=5; t=8; o=3
print(h*100+t*10+o) # 583
```

### 36. Simple Interest

```python
P=10000; R=5; T=2
print(P*R*T/100) # 1000
```

### 37. Rectangle

```python
l=15; w=8
print(l*w,2*(l+w)) # 120 46
```

### 38. Circle

```python
r=7
print(3.14*r*r) # 153.86
```

### 39. Celsius to Fahrenheit

```python
C=35
print(C*9/5+32) # 95
```

### 40. Seconds to Minutes

```python
s=367
print(s//60,s%60) # 6 minutes 7 seconds
```

### 41. Seconds to Hours

```python
s=7384
print(s//3600,(s%3600)//60,s%60) # 2 h 3 m 4 s
```

### 42. Salary

```python
basic=25000; hra=5000; travel=2500; tax=3000
gross=basic+hra+travel
print(gross,gross-tax) # 32500 29500
```

### 43. Travel Cost

```python
distance=120; mileage=20; rate=100
fuel=distance/mileage
print(fuel,fuel*rate) # 6 L, 600
```

### 44. Discount

```python
price=float("2500"); discount=float("10")
d=price*discount/100
print(d,price-d) # 250, 2250
```

### 45. Price × Quantity

```python
price=int("1200"); quantity=int("4")
print(price*quantity) # 4800
```

### 46. Marks

```python
a=int("85"); b=int("78"); c=int("91")
print(a+b+c,(a+b+c)/3) # 254, 84.6667
```

### 47. Tax

```python
p=int("1500"); q=int("2"); tax=int("5")
sub=p*q; t=sub*tax/100
print(sub,t,sub+t) # 3000 150 3150
```

### 48. Discount + GST

```python
p=2000; d=15; gst=18
after=p-p*d/100
print(after,after*gst/100,after+after*gst/100) # 1700 306 2006
```

### 49. Debug Price

```python
price="500"; quantity=3
print(int(price)*quantity) # 1500
```

### 50. Debug Marks

```python
a="80"; b="75"; c="90"
print(int(a)+int(b)+int(c)) # 245
```

### 51. Type Casting

```python
a="50"; b=int(a)
print(a,b,type(a),type(b))
# 50 50 <class 'str'> <class 'int'>
```

### 52. Float to Integer

```python
x=99.99
print(x,int(x)) # 99.99 99
# int() removes the decimal part
```

### 53. Arithmetic

```python
a=12; b=5
print(a+b,a-b,a*b,a/b,a//b,a%b)
# 17 7 60 2.4 2 2
```

### 54. Parentheses

```python
print(10+5*2) # 20
print((10+5)*2) # 30
print(14/2+0) # 7.0
print(5*(2+3)/10) # 2.5
```

### 55. Digit Extraction

```python
n=684
a=n%10; b=n//10; c=b%10; d=n//100
print(a,c,d) # 4 8 6
```

### 56. Debug Student Code

```python
student_name="Ravi"
marks=int("85")
print(student_name,marks)
# Fix: use correct variable name, int(), and close brackets
```

### 57. Digits of 746

```python
n=746
hundreds=n//100
tens=(n//10)%10
ones=n%10
print(hundreds,tens,ones) # 7 4 6
```

### 58. Discount

```python
price=float("2500")
discount=float("10")
amount=price*discount/100
print(amount,price-amount) # 250 2250
```

### 59. Rahul's Marks

```python
a=int("85"); b=int("90"); c=int("78")
total=a+b+c
print(total,total/3,type(total))
# 253, 84.3333, <class 'int'>
# Fix: correct case, type casting, and brackets.
```

### 60. Final Question

```python
n=5836
print(n//1000,(n//100)%10,(n//10)%10,n%10) # 5 8 3 6
print(5+8+3+6) # 22
print(6*1000+3*100+8*10+5) # 6385

price=int("1250"); quantity=int("4"); discount=int("10")
subtotal=price*quantity
d=subtotal*discount/100
print(subtotal,d,subtotal-d) # 5000 500 4500
```
