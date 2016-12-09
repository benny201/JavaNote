# JavaNote

## I/O Stream

### I/O Defn
* Intput Stream: can be read,but not wrote
* class InputStream & Reader for Input stream.

* Outout Stream: can be worte,but not read 
* class OutputStream & Writer for out stream,

* Both InputStream & Reader & OutputStream & Writer are abstract base class!!!

* I/O stream 是对于内存来说的。

### 抽象类？
* 抽象类:类里定义了纯虚成员函数的类。纯虚函数只提供了接口，并没有具体实现.
* In Java, you do not need to declare a method as virtual. Dynamic binding is the default behavior. If you do not want a method to be virtual, you tag it as final.
* Java中所有函数都是虚函数。

### 虚函数和纯虚函数和抽象函数？
* java中没有虚函数的概念，但是有抽象函数的概念，用abstract关键字表示，java中抽象函数必须在抽象类中，而且抽象 函数不能有函数体，抽象类不能被实例化，只能由其子类实现抽象函数，如果某个抽象类的子类仍是抽象类，那么该子类不需要实现其父类的抽象函数。
```
    C++               Java
　　虚函数------------普通函数
　　纯虚函数----------抽象函数
　　抽象类-------------抽象类
　　虚基类--------------接口
  
 ```
