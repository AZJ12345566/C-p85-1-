# C-p85-1-
C语言的学习笔记 p85 分支和循环（1）
C语言是一门结构化的程序设计语言
1.顺序结构
2.选择结构
3.循环结构


分支语句
if和switch
循环语句
while，for，do while
#include<stdio.h>
int main()
{
    ;//空语句
    return 0;
}

//单分支
int main()
{
    int age=10;
    if(age<18)
        printf("未成年\n");
    return 0;
}

//双分支
int main()
{
    int age=18;
    if(age<18)
        printf("未成年\n");
    else
        printf("成年\n");
    return 0;
}


int main()
{
    int age=100;
    if(age<18)
        printf("未成年\n");
    else if(age>18&&age<28)
        printf("青年\n");
    else if(age>28&&age<50)
        printf("壮年\n");
    else if(age>50&&age<90)
        printf("老年\n");
    else
        printf("老不死\n");
    return 0;
}

int main()
{
    int age=100;
    if(age<18)
        printf("未成年\n");
    else
    {
      if(age>18&&age<28)
        printf("青年\n");
      else if(age>28&&age<50)
        printf("壮年\n");
      else if(age>50&&age<90)
        printf("老年\n");
      else
        printf("老不死\n");
    }
    return 0;
}//与上一个main一个逻辑

//如果条件成立，要执行多条语句，应该使用代码块({})
int main()
{
    int age=100;
    if(age<18)
    {
        printf("未成年\n");
        printf("不能谈恋爱\n");
    }
    else
    {
      if(age>18&&age<28)
        printf("青年\n");
      else if(age>28&&age<50)
        printf("壮年\n");
      else if(age>50&&age<90)
        printf("老年\n");
      else
        printf("老不死\n");
    }
    return 0;
}


//悬空else
int mian()
{
    int a=0;
    int b=2;
    if(a==1)
        if(b==2)
            printf("hehe\n");
        else
            printf("haha\n");
    return 0;
}
//这个代码无效，因为else与第二个if对齐，当第一个if不成立，则无法进入程序
//else与最近的if匹配，非要与第一个if匹配，则需要把第二个if括起来

int main()
{
    int num=4;
    if(num=5)//=赋值==判断相等
    {
        printf("呵呵\n");
    }
    return 0;
}//此写法会打印呵呵
//推荐代码这样写,把常量放在前面（在常量和变量的比较下）
int main()
{
    int num=4;
    if(5==num)
    {
        printf("hehe\n");
    }
    return 0;
}


int main()
{
    int i=0;
    while(i<=100)
    {
        if(i%2==1)
            printf("%d",i);
        i++;
    }
    return 0;
}

//switch 专门实现多分支语句
int main()
{
    int day=0;
    scanf("%d",&day);
    switch(day)
    {
    case 1:
        printf("星期1\n");
        break;
    case 2:
        printf("星期2\n");
        break;
    case 3:
        printf("星期3\n");
        break;
    case 4:
        printf("星期4\n");
        break;
    case 5:
        printf("星期5\n");
        break;
    case 6:
        printf("星期6\n");
        break;
    case 7:
        printf("星期7\n");
        break;
     }
    return 0;
}
//case决定入口，break决定出口
//注：case后面必须是整形常量表达式
int main()
{
    int day=0;
    scanf("%d",&day);
    switch(day)
    {
    case 1:
        if(n==1)
            printf("hehe\n");//if语句也可以出现在case语句中
    case 2:
    case 3:
    case 4：
    case 5:
        printf("工作日\n");
        break;
    case 6:
    case 7:
        printf("休息日\n");
        break;
    default://可有可无，处理非法情况，在switch里位置在哪里都可以
        printf("输入错误\n");
        break;
     }
    return 0;
}



