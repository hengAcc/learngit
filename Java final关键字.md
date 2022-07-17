### final 关键字

#### 一、定义常量

等同于C++的const

```java
final int a = 1;
```

#### 二、修饰类

final 修饰类表示该类不可被继承。

注意： final 类中的所有成员方法都会被隐式地指定为 final 方法。

![image-20210721150533949](java final关键字.assets/bc4e838bb8ca47dba31e344087137a2d~tplv-k3u1fbpfcp-zoom-in-crop-mark:1304:0:0:0.image)

#### 二、修饰成员方法

final 关键字修饰的方法不可被覆盖。

《Java编程思想》中指出类中所有的 private 方法都隐式指定为 final 的，所以对于 private 方法，我们显式的声明 final 并没有什么效果。但是我们创建一个父类，并在父类中声明一个 private 方法，其子类中是能够重写其父类的private 方法的。

```java
// 父类
public class Teacher {
    private void study(){
        System.out.println("teacher");
    }
}
// 子类
public class Student extends Teacher{
    private void study(){
        System.out.println("student");
    }
}
```

私有成员函数不属于子类，所以不算方法的覆盖。

**final修饰的方法不能被子类覆盖，但是可以被子类使用和重载。**

####

