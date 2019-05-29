# Java并发编程实战

## 2. 线程安全性

### 2.1无状态的对象是线程安全的（类中无类的域和域的引用）

### 2.2原子性： 不可分割的操作（结果状态不依赖于之前的状态） 

### 2.3 静态条件： 当某个计算的正确性取决于多个线程的交替执行时序性（先检查后执行）

### 2.4 AtomicLong/ AtomicReference

### 2.5 

>  每个操作都是原子性的，但不能保证多个原子性的操作复和后是原子性的 

```java 
if(vector.contains(element))
    vector.add(element);
```

### 2.6 @CuardedBy("this")

### 2.7 程序要在简单性和性能之间平衡

## 对象的共享

### 3.1 重排序

### 3.2非volatile类型的long或double变量的读或写操作分解为两个32位的操作

### 3.3volatile： 不会将变量一起重排序，volatile不会被缓存在寄存器中或者其他处理器不可见的地方

### 3.4 

```java
volatile boolean asleep;
.......
    while(!asleep)
        countSomeSleep();
```

### 3.5 volatile的语义不足以确保递增操作（count++)的原子性

### 3.6 不要在构造过程中用this是对象发生溢出

