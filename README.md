# C-


2022-9-14第一课
C语言输出一句话
例1
#include<stdio.h> 头文件
int main() 定义为整数值
{
printf("Welcome to Minjiang College!\n"); 输出内容  “\n”换行
return 0; 程序完成时关闭
}
例2
#include<stdio.h> 
int main() 
{
printf("花好还须戴\n周诗念忠嘉\n天闲畜神骏\n遥题应未的\n赵子有新作\n他年恢远业\n"); 
return 0; 
}

C语言输入两个整数,计算两数之和
例1
#include <stdio.h>
int main()
{
int a,b,sum;//一、定义变量,int代表数据类型——整数,sum求和;
printf("请输入两个整数：");
scanf("%d %d",&a,&b);//二、输入数据,%d对输入类型的限制代表——整数，并把这俩个数分别给&a和&b两个变量，&取地址运算符;
sum=a+b;//三、数据处理,把a、b的和赋值给sum;
printf("这两个数的和是：%d\n",sum);//四、输出结果,%d输出一个整形数这个数就是sum;
printf("计算完成，谢谢使用！");
return 0;//返回;
}
例2
#include <stdio.h>
int main()
{
int a,b,sum;
scanf("%d %d",&a,&b);
sum=a+b;
printf("这两个数的和是：%d\n",sum);
return 0;
}

额外习题？函数调用？
#include <stdio.h> 
int sum_f(int x,int y)
{
	int s;
	s=x+y;
	return s;
}

int main()
{
	int a,b,sum;
	scanf("%d%d",&a,&b);
	sum=sum_f(a,b);
	printf("sum=%d",sum);
	return 0; 
}


2022-9-15第二课
//程序排错案例一
#include <stdio.h>
int main( )
{
int a=20,b=10;
x=a;
a=b;
b=x;
printf("a=%d，b=%d",a,b);
}
正确答案
#include <stdio.h>
int main()
{
int a=20,b=10,x;
x=a;
a=b;
b=x;
printf("a=%d,b=%d",a,b);
}

//程序拍错案例二
#include <stdio.h>
int main( )
{
int a=20,b=c=10,sum;
sum=a+b+c;
printf("sum=%d",sum);
}
正确答案
#include <stdio.h>
int main()
{
int a=20,c,b=c=10,sum;
sum=a+b+c;
printf("sum=%d",sum);
}

// 程序填空 设有整型变量a=33,字符型变量b='B',单精度实训变量C=33.5，
//双精度实型变量d=33.5,编程输出变量a、b、c、d以及a与b的和、差、积、商。
#include <stdio.h>
int main( )
{
int a;
char b;
——
——
a=33;
b='B';
——
——
printf("a=%d\nb=%c\nc=%f\nd=%f\n",a,b,c,d);
printf("a+b=%d\n",a+b);
printf("a-b=%d\n",a-b);
printf("a*b=%d\n",a*b);
——————
return 0;
}
正确答案？
#include <stdio.h>
int main( )
{
int a;
char b;
float c;
double d;
a=33;
b='B';
c=33.5;
d=33.5;
printf("a=%d\nb=%c\nc=%f\nd=%f\n",a,b,c,d);
printf("a+b=%d\n",a+b);
printf("a-b=%d\n",a-b);
printf("a*b=%d\n",a*b);
printf("a/b=%0.2fn",a/b);
return 0;
}

//程序设计：输出下列表达式的值：x+a%3*(int)(x+y)%2/4  (其中：a=8,x=3.5,y=5.9)
正确答案
# include <stdio.h>
# include <math.h>
main()
{
float x,y,t;
int a;
a=8;x=3.5;y=5.9;
t=x+a%3*int(x+y)%2/4;
printf("%f",t);
}
