- [x] 已掌握：Java程序基本格式，编写注释，变量与常量,整数类型，二进制，浮点类型，字符类型,布尔类型
- [x] (java10)局部变量类型判断,赋值运算符，算术运算符
# 基本格式，注释
```java
/**
 * 这是文档注释
 * @author Melon 
 * @since 1999
 */
public class Main {
    //这是普通注释
    ///这是新版注释md.
    public static void main (String[] args ) {
        System.out.println();
        /*多行注释
          这是多行注释
         */
    }
}
//新版简化版
void main () {
    System.out.println();
}

```
# 整数类型
byte <short <int <long
```java
        byte a ;
        a = -128 ;
        int b = a + 1 , c = 2 ;
        int x = a ;
        final int p = 567 ; //永久不变
        System.out.println(x) ;
        System.out.println(b) ;
        System.out.println(c) ;
        System.out.println(p) ;
        long l = 763698271637892192L;  //右侧默认int,需要加L表示long类型
        int o = 0xa ;  //0x开头16进制
        int oo = 010 ;   //0开头是8进制
        System.out.println(o);
        System.out.println(oo);
        int max = 2147483647;
        max = max + 1 ;
        System.out.println(max);   //补码的原因导致最大变最小
```
# 浮点类型
byte < short(char) <int <long <float <double
```java
        double a = 1.53 , b = 33;
        float c = 10.9f;   //默认double,所以声明单精度时需要加f/F
        System.out.println(a) ;
        System.out.print(b);
        System.out.println(c);
        double z = c ;
        System.out.println(z);  //float转double会出现偏差(0.9时
        long l = 782814670000098082l;
        System.out.println(l);
        float ll = l ;       //float可以损失精度但是转化long
        System.out.println(ll);
```
# 字符类型
```java
        int c = '的';              //char只能单引号 单字符
        char a = '\'' ;             // 反斜杠表转义字符
        System.out.println(a);
        System.out.println(c);     //用int可以直接查看此字符的编码
        String X = "aaaa\nbbbb\"" ;        //String双引号 0-n个字符
        System.out.println(X);
```
# 布尔类型
```java
    boolean b = true ;      //布尔类型只有真或假
```
# (java10)局部变量类型判断
```java
        var i = 1.5 ;        //var关键字自动识别变量类型,但少用
        System.out.println(i);
```
# 赋值运算符
```java
    int a =  666 ;     //等号用来赋值
    int b = a =777 ;     //a = 777 的结果就是777(赋值运算有结果)
        System.out.println(a);
        System.out.println(b);
```
# 算术运算符
```java
 int a = 1 + 1 , c = 30 ;    //和平常计算一样
    int b = a + 20 - c ;
    System.out.println(a) ;
    System.out.println(b);
    //不同类型
        int d = 10 ;   //小类型会自动转化为大类型进行运算
        short o = 90 ;
        int p = d + o ;
        System.out.println(p);
        char ch = 'c' ;    //char会转化为编码来进行运算
        int ch2 = ch ;
        System.out.println(ch2);
        System.out.println(ch + a);
        float f1 = 9.9f;    //float和double不要直接加
        double f2 = 0.9;
        System.out.println(f2+a );
        String str1 = "abc" ,str2 = "cdf" ;
        System.out.println(a + 1.5 + str1 + str2 + a  + true);    //字符串可以用加法拼接，其他类型会自动变为字符串
        double i = 1d*8/5 ;      //运算中小数部分会被消除，需要专门声明double(坑点)
        System.out.println(i);
        /*其他运算符：%取余数
        优先级:正负号>乘除取模>加减>赋值
        赋值=从右往左,其余从按优先级从左往右
         */
```
