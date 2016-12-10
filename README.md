# JavaNote

## I/O Stream
> Update: 9/12/2016     

### 1.0 I/O Defn
* Intput Stream: can be read,but not wrote
* class InputStream & Reader for Input stream.

* Outout Stream: can be worte,but not read 
* class OutputStream & Writer for out stream,

* All InputStream & Reader & OutputStream & Writer are abstract base class!!!

* I/O stream 是对于内存来说的。  

#### 1.1 抽象类？
* 抽象类:类里定义了纯虚成员函数的类。纯虚函数只提供了接口，并没有具体实现.
* In Java, you do not need to declare a method as virtual. Dynamic binding is the default behavior. If you do not want a method to be virtual, you tag it as final.
* Java中所有函数都是虚函数。  

#### 1.2 虚函数和纯虚函数和抽象函数？
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

### 2.0 字节流&字符流?    
> update: 10/12/2016

* 操作单位不一样
* 前者操作单位为8bit->byte，对应 InputStream & OutputStream
* 后者操作单位为16bit->char, 对应 Reader & Writer     

#### 2.1 Reader

`read()`: Reads a single character.     
`read(char[] cbuf)`: Reads characters into an array.     
`read(char[] cbuf, int off, int len)`: Reads characters into a portion of an array.     
    

#### 2.2 InputStream     

`read()`: Reads the next byte of data from the input stream.     
`read(byte[] b)`: Reads some number of bytes from the input stream and stores them into the buffer array b.     
`read(byte[] b, int off, int len)`: Reads up to len bytes of data from the input stream into an array of bytes.     
     
example :
```
                        File file = new File(".");
		        File tmpFile = File.createTempFile("aaa", ".txt",file);
			FileInputStream fileInputStream = new FileInputStream(tmpFile);
			byte[] buffer = new byte[1024];
			int hasread = 0;
			while((hasread = fileInputStream.read(buffer))>0) {
				System.out.print(new String(buffer,0,hasread));
			}
			tmpFile.deleteOnExit();
			fileInputStream.close();
```     
     
#### 2.3 OputStream & Writer     

### 3.0 节点流 & 处理流?     
* 节点流： 向特定I/O设备读写数据的流；
* 处理流： 连接或封装已存在的流，用封装后的流实现读写；     

#### 3.1 处理流     

example:     
```
FileOutputStream file = new FileOutputStream("test.txt");
PrintStream ps = new PrintStream(file);
ps.println(new PrinteStreamTest());
```
