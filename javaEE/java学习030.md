# 昨日回顾

## IO流：

### 	流的分类：

​		单位 ： 流向：

​				输入		输出

​			字节	InputStream	OutputStream

​			字符	Reader	Writer

​	以上4个类时候IO流的四个抽象基类，其他的流都是基于以上流衍生而来——装饰者设计模式

​	节点流：	FileInputStream		FileOutputStream

​	处理流	：

​		缓冲流 	BufferedInputStream		BufferedOutputStream

​				BufferedReader			BufferedWriter

​			特点：内部自动创建以一个8K的缓冲区，因此在使用缓冲输出流的时候，需要进行flush /  close。

​		转换流：InputStreamRead		字节——>字符	编码

​				OutputStreamWriter	字符——>字节	解码

​		字符集

​		标准流：System.in(InputStream)	键盘

​				System.out(PrintStream)	屏幕

​				标准流重定向：setIn / setOut

​				System.err	错误流

​		打印流：PrintStream

# 数据流：DataInputStream/DataOutputStream





问题：使用数据输入流





# 对象流：





## 序列化和反序列化：

​	为了方便数据或对象在网络中进行传送。以序列化机制来保证数据传送的正确性。

- 只能
- Seri









​				