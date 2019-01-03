# first_test
text for python
题目：定义一个函数‘quadratic(a,b,c)’,接收三个参数，返回一元二次方程：
ax² + bx + c = 0 的两个解。
import math
def quadratic(a,b,c):
	d=b*b-4*a*c
	if a==0:
		if b==0:
     		 if c==0:
      			return '方程根为全体实数'
    	 	 else:
       			return'方程无根'
		else:
			x1=-c/b
			x2=x1
			return x1,x2
	else:
   		 if d<0:
   		 	return'方程无根'
   		 else:
   		 	x1=(-b+math.sqrt(d))/2/a
   		 	x2=(-b-math.sqrt(d))/2/a
   		 	return x1,x2
print(quadratic(2,3,1))
print(quadratic(1,3,-4))
if quadratic(2,3,1)!=(-0.5,-1.0):
   print('测试失败')
elif quadratic(1,3,-4)!=(1.0,-4.0):
   print('测试失败')
else:
   print('测试成功')
