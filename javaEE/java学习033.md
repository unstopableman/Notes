[TOC]

------

# 昨日回顾：

## 反射机制：

​	主要是在程序运行时，来动态获取类的结构及类的内部属性和方法，还可以动态创建对象，为属性赋值，调用方法。

### Class 对象：

​	一个类只能有一个Class	class对象位于方法区的Class区

### 获取class对象的三种方式：

1. 使用Object类继承而来的getClass方法	通过类的对象去获取（基本不用）
2. **通过Class类提供的forName(String className)   使用全类名**
3. 通过Class的class属性来获取

### 类加载器：

1. Bootstap ClassLoader
2. Extention ClassLoader
3. System ClassLoader
4. 自定义类加载器

### 类加载的过程：





