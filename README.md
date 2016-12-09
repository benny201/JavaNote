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
* In Java, you do not need to declare a method as virtual. Dynamic binding is the default behavior. If you do not want a method to be virtual, you tag it as final.Java中所有函数都是虚函数。
