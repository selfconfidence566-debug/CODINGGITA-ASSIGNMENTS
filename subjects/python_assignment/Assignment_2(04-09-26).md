# 1. String to Integer

# Convert "25" into an integer and print its value and type.

x="25"
x=int(x)
print(x,type(x))

# 2. String to Float

# Convert "75.5" into a float.

x="75.5"
x=float(x)
print(x,type(x))

# 3. Integer to Float

# Convert 50 into a float.

x=50
x=float(x)
print(x,type(x))

# 4. Float to Integer

# Convert 85.9 into an integer. Decimal part is removed.

x=85.9
x=int(x)
print(x,type(x))

# 5. Integer to String

# Convert 101 into a string.

x=101
x=str(x)
print(x,type(x))

# 6. Multiple Conversions

# Convert 18 to int, 92.5 to float, 100 to string, and 45.8 to int.

a=int("18"); b=float("92.5"); c=str(100); d=int(45.8)
print(a,b,c,d)

# 7. Predict the Output

# a=int("20"), c=int(10.8), e=str(25)

a=int("20"); c=int(10.8); e=str(25)
print(a,c,e)

# Output: 20 10 25

# 8. Debug

# "19" is text, so convert it to int before adding 1.

x="19"
print(int(x)+1)

# Output: 20

# 9. Bonus

# Convert "85" to int and add 5.

bonus="85"
print(int(bonus)+5)

# Output: 90

# 10. Delivery

# Price is "1499.50" and delivery is 99.50. Find total.

price="1499.50"; delivery=99.50
print(float(price)+delivery)

# Output: 1599.0

# 11. Arithmetic Operators

# Find +, -, *, /, //, %, and ** for 20 and 6.

a=20; b=6
print(a+b,a-b,a*b,a/b,a//b,a%b,a**b)

# Output: 26 14 120 3.3333333333333335 3 2 64000000

# 12. Division

# Find 17/5, 17//5 and 17%5.

print(17/5,17//5,17%5)

# Output: 3.4 3 2

# / means normal division, // gives whole number, % gives remainder.

# 13. Operator Precedence

# Find 10+5*2, then make addition happen first.

print(10+5*2)

# Output: 20

print((10+5)*2)

# Output: 30

# 14. Operator Precedence

# Find 20-4*3+2, then use brackets to change the order.

print(20-4*3+2)

# Output: 10

print((20-4)*(3+2))

# Output: 80

# 15. Power and Square

# Find 2^3, 3^2, 10^2 and area of a square with side 5.

print(2**3,3**2,10**2)
side=5
print(side**2)

# Output: 8 9 100 and 25

# 16. Shopping

# Find total cost of 80, 20 and 10.

print(80+20+10)

# Output: 110

# 17. Shopping

# Find cost of 3 items at 50, 2 items at 15 and 1 item at 500.

print(3*50,2*15,1*500)
print(3*50+2*15+500)

# Output: 150 30 500 and total 680

# 18. Groups

# Put 47 students into groups of 5. Find full groups and students left.

students=47
print(students//5,students%5)

# Output: 9 groups and 2 students left

# 19. Marks

# Find total and average of 85, 78 and 92.

marks=[85,78,92]
print(sum(marks),sum(marks)/3)

# Output: 255 and 85

# 20. Percentage

# Find total, average and percentage of 78,85,92,81,74.

marks=[78,85,92,81,74]
total=sum(marks)
print(total,total/5,total/500*100)

# Output: 410, 82 and 82%

# 21. Ones Digit

# Find the ones digit of 583.

n=583
print(n%10)

# Output: 3

# 22. Tens Digit

# Find the tens digit of 583.

n=583
print((n//10)%10)

# Output: 8

# 23. Hundreds Digit

# Find the hundreds digit of 583.

n=583
print(n//100)

# Output: 5

# 24. Digits of 746

# Print hundreds, tens and ones digits.

n=746
print(n//100,(n//10)%10,n%10)

# Output: 7 4 6

# 25. Digits of 5829

# Print thousands, hundreds, tens and ones digits.

n=5829
print(n//1000,(n//100)%10,(n//10)%10,n%10)

# Output: 5 8 2 9

# 26. Sum of Digits

# Find the sum of digits of 583.

n=583
print(n//100+(n//10)%10+n%10)

# Output: 16

# 27. Sum of Digits

# Find the sum of digits of 4726.

n=4726
print(n//1000+(n//100)%10+(n//10)%10+n%10)

# Output: 19

# 28. Product of Digits

# Find the product of digits of 234.

n=234
print((n//100)*((n//10)%10)*(n%10))

# Output: 24

# 29. Reverse Number

# Reverse 583.

n=583
print(n%10*100+(n//10)%10*10+n//100)

# Output: 385

# 30. Reverse Number

# Reverse 4726.

n=4726
print(n%10*1000+(n//10)%10*100+(n//100)%10*10+n//1000)

# Output: 6274

# 31. Place Values

# Find place values of 5834.

n=5834
print(n//1000*1000,(n//100)%10*100,(n//10)%10*10,n%10)

# Output: 5000 800 30 4

# 32. First and Last Digit

# Find the difference between first and last digit of 583.

n=583
print(abs(n//100-n%10))

# Output: 2

# 33. Debug Ones Digit

# /10 is wrong for finding the ones digit. Use %10.

number=583
print(number%10)

# Output: 3

# 34. Digits of 9365

# Extract all digits using % and //.

n=9365
print(n//1000,(n//100)%10,(n//10)%10,n%10)

# Output: 9 3 6 5

# 35. Build Number

# Build 583 using hundreds=5, tens=8 and ones=3.

h=5; t=8; o=3
print(h*100+t*10+o)

# Output: 583

# 36. Simple Interest

# Find simple interest for P=10000, R=5 and T=2.

P=10000; R=5; T=2
print(P*R*T/100)

# Output: 1000

# 37. Rectangle

# Find area and perimeter of a rectangle with length 15 and width 8.

l=15; w=8
print(l*w,2*(l+w))

# Output: 120 and 46

# 38. Circle

# Find area of a circle with radius 7 and pi=3.14.

r=7
print(3.14*r*r)

# Output: 153.86

# 39. Celsius to Fahrenheit

# Convert 35 Celsius to Fahrenheit.

C=35
print(C*9/5+32)

# Output: 95

# 40. Seconds to Minutes

# Convert 367 seconds into minutes and seconds.

s=367
print(s//60,s%60)

# Output: 6 minutes 7 seconds

# 41. Seconds to Hours

# Convert 7384 seconds into hours, minutes and seconds.

s=7384
print(s//3600,(s%3600)//60,s%60)

# Output: 2 hours 3 minutes 4 seconds

# 42. Salary

# Find gross salary and salary after tax.

basic=25000; hra=5000; travel=2500; tax=3000
gross=basic+hra+travel
print(gross,gross-tax)

# Output: Gross=32500, Net=29500

# 43. Travel Cost

# Travel 120 km, mileage is 20 km/L and fuel costs 100/L.

distance=120; mileage=20; rate=100
fuel=distance/mileage
print(fuel,fuel*rate)

# Output: 6 L and Rs.600

# 44. Discount

# Price=2500 and discount=10%. Find discount and final price.

price=float("2500"); discount=float("10")
d=price*discount/100
print(d,price-d)

# Output: 250 and 2250

# 45. Price and Quantity

# Price is "1200" and quantity is "4". Find total.

price=int("1200"); quantity=int("4")
print(price*quantity)

# Output: 4800

# 46. Marks

# Find total and average of marks "85", "78" and "91".

a=int("85"); b=int("78"); c=int("91")
print(a+b+c,(a+b+c)/3)

# Output: 254 and 84.6667

# 47. Tax

# Price=1500, quantity=2 and tax=5%. Find subtotal, tax and final.

p=int("1500"); q=int("2"); tax=int("5")
sub=p*q; t=sub*tax/100
print(sub,t,sub+t)

# Output: 3000, 150 and 3150

# 48. Discount and GST

# Price=2000, discount=15%, GST=18%. Apply discount first.

p=2000; d=15; gst=18
after=p-p*d/100
print(after,after*gst/100,after+after*gst/100)

# Output: 1700, 306 and 2006

# 49. Debug Price

# "500" is text, so convert it before multiplying by 3.

price="500"; quantity=3
print(int(price)*quantity)

# Output: 1500

# 50. Debug Marks

# Convert string marks before adding them.

a="80"; b="75"; c="90"
print(int(a)+int(b)+int(c))

# Output: 245

# 51. Type Casting

# Show the value and type before and after converting "50".

a="50"; b=int(a)
print(a,b,type(a),type(b))

# Output: 50 50 <class 'str'> <class 'int'>

# 52. Float to Integer

# Convert 99.99 to int. The decimal part is removed.

x=99.99
print(x,int(x))

# Output: 99.99 99

# 53. Arithmetic

# Find +, -, *, /, // and % for 12 and 5.

a=12; b=5
print(a+b,a-b,a*b,a/b,a//b,a%b)

# Output: 17 7 60 2.4 2 2

# 54. Parentheses

# Show how parentheses change the answer.

print(10+5*2)
print((10+5)*2)
print(14/2+0)
print(5*(2+3)/10)

# Output: 20, 30, 7.0, 2.5

# 55. Digit Extraction

# For 684, find ones, tens and hundreds digits.

n=684
a=n%10; b=n//10; c=b%10; d=n//100
print(a,c,d)

# Output: 4 8 6

# 56. Debug Student Code

# Fix variable name, type conversion and missing bracket.

student_name="Ravi"
marks=int("85")
print(student_name,marks)

# Output: Ravi 85

# 57. Digits of 746

# Extract hundreds, tens and ones digits.

n=746
hundreds=n//100
tens=(n//10)%10
ones=n%10
print(hundreds,tens,ones)

# Output: 7 4 6

# 58. Discount

# Price="2500", discount="10". Find discount amount and final price.

price=float("2500"); discount=float("10")
amount=price*discount/100
print(amount,price-amount)

# Output: 250 2250

# 59. Rahul's Marks

# Find total, average and type for 85, 90 and 78.

a=int("85"); b=int("90"); c=int("78")
total=a+b+c
print(total,total/3,type(total))

# Output: 253, 84.3333 and <class 'int'>

# 60. Final Question

# Part A: Extract digits, find sum and reverse 5836.

n=5836
print(n//1000,(n//100)%10,(n//10)%10,n%10)
print(5+8+3+6)
print(6*1000+3*100+8*10+5)

# Output: digits=5 8 3 6, sum=22, reverse=6385

# Part B: Price=1250, quantity=4, discount=10%.

price=int("1250"); quantity=int("4"); discount=int("10")
subtotal=price*quantity
d=subtotal*discount/100
print(subtotal,d,subtotal-d)

# Output: subtotal=5000, discount=500, final=4500
