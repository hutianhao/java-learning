## java类与对象
>类的定义
>>1. class 类名{成员变量;}<br/>
>>2. class 类名{成员变量;成员方法;}
>>3. 一个类中可以没有成员变量和成员方法

```
//hasNext()不可以识别空格
//hasNextLine()可以识别空格
import java.util.Scanner;

public class Test{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        System.out.println(“请输入: ”);
        if(scan.hasNext()){
            String str = scan.Next();
            System.out.println(“输入的是: ”+str);
        }
    }
}
```

```
public class Person{
    public static void main(String[] args){
       
    
    }
    int age;
    String name;
    public Person(int age,String name){
        age = age;
        name = name;
        
    }
}
```
>类的成员方法-声明
```
//访问修饰符 数据类型 函数名(参数列表);
public int test(int a);/*方法的声明没有函数体*/
```

```
//把表达式里的值返回给主调方法
return 表达式
```

```
例：计算两个数的和，并把结果返回给调用他的函数
注意：返回类型和返回的结果的类型要一样，在调用某个成员方法的时候，给出的具体数值的个数和类型要跟形参相互匹配

1.返回为int整形
public int add1(int num1,int num2){
    return num1+num2;
}

2.float单精度
public float add2(float num1,num2){
    return num1+num2;
}

3.方法可以没有返回值
public void add(int num1,int num2){
    int result = num1 + num2;
    System.out.println("结果是:" + result);
}
```

>编写一个函数将二维数组进行转置
```
import java.util.Scanner;
import java.lang.String;

public class TranformMatrix{
    public static void main(String[] args){
        Scanner scan = new Scanner(System.in);
        System.out.println("请输入矩阵的行:");
        int row = scan.nextInt();
        System.out.println("请输入矩阵的列:");
        int column = scan.nextInt();
        System.out.println("转置前的矩阵:");
        int[][]a = inputMatrix(row,column);
        transform(a);
        System.out.println("转置后的矩阵:");
        display(a);
    }
    //输入矩阵
    public static int[][] inputMatrix(int row,int column){
        Scanner scan = new Scanner(System.in);
        System.out.println("请输入矩阵的值:");
        int[][] a = new int[row][column];
        for(int i=0;i<a.length;i++){
            for(int j=0;j<a[0].length;j++){
                a[i][j] = scan.nextInt();
            }
        }
        return a; //返回整个matrix
    }
    //转置矩阵
    public static void transform(int[][] a){
        int result = new int[a[0].length][a.length];
        for(int i=0;i<a[0].length;i++){
            for(int j=0;j<a.length;j++){
                result[i][j] = a[j][i];
                System.out.println("result[i][j]"+" ");
            }
            System.out.println();
        }
    }
    //输出矩阵
    public static void display(int[][] a){
        for(i=0;i<a.length;i++){
            for(j=0;j<a[0].length;j++){
                System.out.println(a[i][j]+" ");
            }
            System.out.println();
        }
    }
}
```








