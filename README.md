# JavaNote

## I/O Stream

### I/O Defn
* Intput Stream: can be read,but not wrote
* class InputStream & Reader for Input stream.

* Outout Stream: can be worte,but not read 
* class OutputStream & Writer for out stream,

* All InputStream & Reader & OutputStream & Writer are abstract base class!!!

* I/O stream 是对于内存来说的。  

#### 抽象类？
* 抽象类:类里定义了纯虚成员函数的类。纯虚函数只提供了接口，并没有具体实现.
* In Java, you do not need to declare a method as virtual. Dynamic binding is the default behavior. If you do not want a method to be virtual, you tag it as final.
* Java中所有函数都是虚函数。  

#### 虚函数和纯虚函数和抽象函数？
* java中没有虚函数的概念，但是有抽象函数的概念，用abstract关键字表示，java中抽象函数必须在抽象类中，而且抽象 函数不能有函数体，抽象类不能被实例化，只能由其子类实现抽象函数，如果某个抽象类的子类仍是抽象类，那么该子类不需要实现其父类的抽象函数。
```
                                   C++               Java
　                                 虚函数-------------普通函数
　　                               纯虚函数-----------抽象函数
　　                               抽象类-------------抽象类
　　                               虚基类--------------接口
  
 ```
* Java中，如果函数不是抽象函数，而是一个普通函数，它是默认实现类似C++中虚函数功能的，也就是说，调用某个函数，是根据当前指针所指向对象的类型来判断的，而不是根据指针类型判断
* 抽象函数没有函数体，与空函数有区别。     

### 字节流&字符流?
* 操作单位不一样
* 前者操作单位为8bit，对应 InputStream & OutputStream
* 后者操作单位为16bit, 对应 Reader & Writer

###  
