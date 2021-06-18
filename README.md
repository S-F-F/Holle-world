# Day 01—Java

```java
public class HelloWord{
	public static void main(String[] arge){
		System.out.println("环境是HelloWorld");
		//println("ssss");
}
}
/*
	public static void main(String[] arge)入口函数
	一个文件只能包含一个public class
	class文件可以通过反编译jd-gui
*/
/**
*文档注释
*/

```

### 数据类型

```java



/*
	java数据类型
		基本数据类型
			整数（不同长度）：byte(一个字节-128~127)
            	 short(俩个字节-32768~32767) 
            	 int(四个字节政府21亿) 
            	 long(八个字节，默认类型是in t。需要int转long在后面加L)
			浮点：float(小数点后七位)
				 double(默认类型是double,使用float时候后面加f)
				 浮点类型并不能确保一个精确的值，会损失精度
			字符：char(表示一个字符''，对应Unicode表里面的字符,""表示一个字符转String)
			布尔：boolean
		引用数据类型
			接口
			类
			String
*/

puclic calss DataType{
    public static void main(String args[]){
        
    }
}
```

### 常量变量

```java
/*
常量:在执行过程中，不会发生改变 final
变量:在执行过程中，会发生改变

在类内定义的成员变量会存在默认值，在方法内不会
*/
```

### 运算符

```java
/*
	运算符
		%取余
		/取商 
		+=赋值运算符
		逻辑运算符：&&and ||or ！取反
		位运算符：&,|,^,~,>>,<<,>>>
*/

public class OperatorDome{
    public static void mian(Sting args[]){
        
    }
}
```



# Day 02

```java
import java.util.Scanner;
/*
	Scanner
	Math.random()随机数
	switch：一般用于等值判断
*/
public class AddCust{
    public static void main(String args[]){
        //创建Scanner对象
        Scanner sc = new Scanner(System.in);
        System.out.println("");
        String strText = sc.nextLine();
    }
}
```

![image-20210616162415729](C:\Users\lancet\AppData\Roaming\Typora\typora-user-images\image-20210616162415729.png)



### 循环

```java
/*
while :先判断后执行
do while :先执行后判断
for :定义变量初始化的时候，for循环的作用域仅仅是限制与当前for循环
*/
public class WhileDome{
    public static void main(String args[]){
        int i = 1;
        int sum = 0;
        while(i<=100){
            sum+=i;
           	i++;
		}
        System.out.println(sum);
        
        do{
            if(i == 50){
                System.out.println(i);
            }
            i++;
        }while(i>=100);
        for(int range=1;range<=100;range++){
            System.out.println(range);
        }
    }
}
```

# Day 03

### System.exit(0)

``` java
/*
直接退出方法，return、
System.exit(0):可以根据退出参数进行不同处理
*/
```

### 递归算法

![image-20210617154130678](C:\Users\lancet\AppData\Roaming\Typora\typora-user-images\image-20210617154130678.png)

### 数组

``` java
/*
数据是引用类型，是有默认值的
*/

public class ArrageDome{
    public static void main(Strint args[]){
        int[] array;
        array = new int[5];
        //声明并创建
        int [] arr = new int[5];
        int [] arr2 = new int[]{1,2,3,4,5};
        int[] arr5 = {1,2,3,4};
        //长度表示申请空间的大小
        int listLength = arr5.length;
    }
}
```

### 二维数组

``` java
 /*
 
 */
public class TowArray{
    public static void main(String args[]){
        int[] arr = new int[6];
        int[][] arr2 = new int[5][]
    }
}
```

### 特殊传参

![image-20210617182042574](C:\Users\lancet\AppData\Roaming\Typora\typora-user-images\image-20210617182042574.png)

# Day 04

## 面向对象

``` java
/*
	java文件中可以定义多个cliass，只能有一个public cliass、
	在字符转比较的时候使用equals
	void 表示没有返回值
*/


public class Student{
    //属性的定义
    int stuNumber;
    String name;
    int age = 20;

    //方法的定义
    void study(){
        System.out.println("sss");
    }

    void eat(String food){
        System.out.println(food);
    }
    public static void main(String args[]){
//        创建对象
        Student student = new Student();
//        调用属性
        student.name = "史飞飞";
        student.age = 29;
        student.stuNumber = 164351027;
        System.out.println(student.stuNumber);
        System.out.println(student.name);
        System.out.println(student.age);
//        调用方法
        student.study();
        student.eat("sss");

    }

}

```

### Srting 比较

```java
/*
字符转在比较的时候
==：比较的是地址,Scanner是存在池，String是存在堆
equals比较的是值
*/
import java.util.Scanner
public class StringDome{
    public static void main(String args[]){
        String str = "sss";
        Scanner sc = new Scanner(String.in);
        System.out.print("input");
        String str2 = sc.nextLine();
        System.out.print(str == str2);
        String str3 = "sss"
        System.out.print(str.equals(str3));
    }
}
```

### 内存

​	**栈 stake**

```text
	存放局部变量

	先进后出
```

​	**堆 heap**

``` text
	存放new出来的对象

	需要垃圾回收器定期回收System.gc()
```

**方法区**

```tetx
	存放：类的信息代码，static(静态变量)，字符串常量
```

### 构造函数

```java
/*
	系统自动补充无参构造方法
	无返回值
*/

public class Teacher{
    String name;
    int age;
    public Teacher(){
        System.out.println();
    }
    public Teacher(String name,int age){
        
    }
}
```

### 重载

```java
public class Teacher{
   
    public teach(String a,int b){
        
    }
    public teach(int b,String a){
        
    }
}

```

### 构造函数重载

```java
public class Teacher{
    String name;
    int age;
    public Teacher(){
        System.out.println();
    }
    public Teacher(String xname,int xage){
        name=xname;
        age=xage;
    }  
    public Teacher(int xage,String xname){
        name=xname;
        age=xage;
    }
    public static void main(String args[]){
        Teacher tea = new Teacher("lisi",11);
        Teacher tea = new Teacher(11,"11");
        
    }
}
```



