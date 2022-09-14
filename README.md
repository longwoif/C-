# C-
C语言输出一句话
#include<stdio.h> 头文件
int main() 定义为整数值
{
printf("Welcome to Minjiang College!\n"); 输出内容  “\n”换行
return 0; 程序完成时关闭
}
C语言输入两个整数,计算两数之和
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
