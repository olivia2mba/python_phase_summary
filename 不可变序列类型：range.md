# 第十章 range类型

* ## **range\(\)函数的通常用途是：生成一个序列，这个序列通常用于for循环。**

看下面例子：

&gt;&gt;&gt; for i in range\(5\):

```
print\('hello world', str\(i\)\)
```

hello world 0

hello world 1

hello world 2

hello world 3

hello world 4

注意一个细节，序列里不包含5.

* ## **range也是一个类型，是不可变序列，不支持原位改变：**

&gt;&gt;&gt; r = range\(5\)

&gt;&gt;&gt; r

range\(0, 5\)

&gt;&gt;&gt; type\(r\)

&lt;class 'range'&gt;

type\(\) 函数是可以查看一个对象类型的函数。

* ## **对于序列的通用操作也适用于range类型**

&gt;&gt;&gt; r

range\(0, 5\)

&gt;&gt;&gt; r\[0\]

0

&gt;&gt;&gt; r\[-1\]

4

&gt;&gt;&gt; 3 in r

True

&gt;&gt;&gt; 9 in r

False

&gt;&gt;&gt; r\[:\]

range\(0, 5\)

&gt;&gt;&gt; min\(r\)

0

&gt;&gt;&gt; max\(r\)

4

&gt;&gt;&gt; len\(r\)

5

&gt;&gt;&gt; r.index\(3\)

3

&gt;&gt;&gt; r.count\(4\)

1

&gt;&gt;&gt; sum\(r\)

10

&gt;&gt;&gt; r\[0:2\]

range\(0, 2\)

&gt;&gt;&gt; r = r\[0:2\]

&gt;&gt;&gt; r

range\(0, 2\)

&gt;&gt;&gt; r\[4\]

Traceback \(most recent call last\):

  File "&lt;pyshell\#396&gt;", line 1, in &lt;module&gt;

    r\[4\]

IndexError: range object index out of range

&gt;&gt;&gt; r\[2\]

Traceback \(most recent call last\):

  File "&lt;pyshell\#397&gt;", line 1, in &lt;module&gt;

    r\[2\]

IndexError: range object index out of range

&gt;&gt;&gt; r\[0\]

0



* ## **range类型的声明：**

1）参数只有1个，代表终止数值，此数值并不包括在序列里。

3） 参数有2个，代表起始数值和终止数值，序列包括起始数值，不包括终止数值。

后面的for循环只是便于理解range序列里的数值，其本身range\(3, 12\)的含义要理解。

4） 参数如果有3个，第三个参数代表step步长值。

