# xinchao.java
java笔记 

一、JVM JDK与jre的区别：
1、包含关系： JDK包含JRE，JRE包含JVM
   JVM：java虚拟机，在不同的系统中，都有不同的JVM，所以也证明java是跨平台的
   JRE：是java运行时环境，是运行已编译java所需的所有内容的集合，包含了JVM，java类库，java命令以及一些基础的架构吗，但不能用于创建新程序
   JDK：拥有JRE所拥有的一切，并且还包含java编译器（javac）和工具（如javadoc和jdb），能够创建和编译程序
 
二、String怎么转换成Integer的？
   String转换成Integer的两种方法：
   Integer.parseInt（String s）
   Integer.valueOf（String s）

三、什么是序列化与反序列化？
   序列化：就是把java对象转换成二进制流，方便进行存储和运输。
   反序列化：就是把二进制流转换回java对象
   
四、反射
   反射核心的四大类：
   Class类：正在运行在内存中的所有类都是该类的对象，每个Class类都包含本类的所有信息
           类内部的主要信息：Field（所有的属性），Method（所有的方法），Constructor（所有的构造方法）
   Field类：通过反射获取到Field对象时，也就获得了某个类起内部包含某个属性的所有信息
           类内部的主要信息：标注的属性上的注解，属性名，属性的数据类型，属性的访问修饰符
   Constructor类：描述Class类中构造方法的一个类，提供了描述某个类中构造方法的所有信息
           类内部的主要信息：构造方法的访问修饰符，构造方法的参数（参数上的注解，参数的类型，参数的名字）
   Method类：描述Class类中的所有方法（不包含构造方法）的类，包含抽象方法
           类内部的主要信息：与Constructor类内部的主要信息相同，返回的数据类型
   
五、ArrayList扩容机制：
   ArrayList是基于数组的一个集合，在开始的时候就确定了数组的容量，当新增数据的时候回判断当前数组长度+1是否超过数组容量，是的话会增加1.5倍数组容量

六、
