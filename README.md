# Age-calculator2

print("Enter the date in formats of dd-mm-yyyy")
date1=[int(s) for s in input("Date1: ").split("-")]
date2=[int(s) for s in input("Date2: ").split("-")]
days=[31,28,31,30,31,30,31,31,30,31,30,31]
d1=date1[0]
d2=date2[0]
m1=date1[1]
m2=date2[1]
y1=date1[2]
y2=date2[2]
a=0
b=0
count=0
x=(y2-y1-1)*365
#print("x",x)
for i in range(y1+1,y2):
    if (i%4==0 and i%100!=0) or (i%400==0):
        count=count+1
        #print(count,"c")
for i in range(m1-1,12):
    a=a+days[i]
    #print(a,"a")
for i in range(m2-1):
    b=b+days[i]
    #print(b,"b")
n1=-d1+a+x+count+d2+b
#print(n1)
if  (y1%4==0 and y1%100!=0) or (y1%400==0):
    if m1<=2:
        n1=n1+1
if  (y2%4==0 and y2%100!=0) or (y2%400==0):
    if m2>2:
        n1=n1+1
print("no.of days:",n1)
