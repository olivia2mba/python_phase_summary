语句与流程控制

Pycharm：对于专业python开发者的python IDE

语句与语法

语句

1）赋值语句

2）运行函数

&gt;&gt;&gt; import math

&gt;&gt;&gt; x = 5

&gt;&gt;&gt; y = math.pow\(x\)

&gt;&gt;&gt; y

25

3）选择执行

&gt;&gt;&gt; if x &gt; 3:

    print \('x 大于 3'\)

'x 大于 3'

4）迭代语句

&gt;&gt;&gt; for i in range\(1, 6\):

        i = i \*\*2

        print\(i\)

1

4

9

14

25

5）循环

6）函数

7）模块与命名空间

8）类

9）异常处理



语法 

1）强制缩进 4个空格，非tab键

2）PEP8标准，感兴趣的朋友可以去看一下

&gt;&gt;&gt; while True:

    txt = input\('请输入一个数字：'\)

    if txt == 'stop':

        break

    elif not txt.isdigit\(\):

        print\('您输入的不是数字！'\)

    else:

        num = int\(txt\)

        if num &lt; 20:

        	print\('您输入的数字太小了。'\)

        elif num &gt; 20:

        	print\('您输入的数字太大了'\)

        else:

        	print\('恭喜您，猜对啦。'\)



赋值语句

赋值语句机制：

1）赋值创建对象引用

2）名称创建于首次赋值

3）名称引用前必须赋值

4）某些操作会执行隐形赋值



元组/列表赋值

例子1.

&gt;&gt;&gt; a,b = 5, 3

&gt;&gt;&gt; a

5

&gt;&gt;&gt; b

3

\#这个例子形式python默认其是元组实质



例子2.

&gt;&gt;&gt; a,b = 'jerry', 30

&gt;&gt;&gt; a,b = b,a

&gt;&gt;&gt; a

30

&gt;&gt;&gt; b

'jerry'



序列赋值

例子3.

&gt;&gt;&gt; org = '优品课堂'

&gt;&gt;&gt; org

'优品课堂'

&gt;&gt;&gt; a,b,c,d = '优品课堂'

&gt;&gt;&gt; a

'优'

&gt;&gt;&gt; b

'品'

&gt;&gt;&gt; c

'课'

&gt;&gt;&gt; d

'堂'



\#这里注意，如果赋值字符串，左边变量个数要与右边字符串元素个数一致



例子4.

&gt;&gt;&gt; a,\*b = '优品课堂'

&gt;&gt;&gt; a

'优'

&gt;&gt;&gt; b

\['品', '课', '堂'\]



\# \*b这种形式python认为是打包解码后面字符串



例子5.

&gt;&gt;&gt; a,\*b,c = '优品课堂'

&gt;&gt;&gt; a

'优'

&gt;&gt;&gt; c

'堂'

&gt;&gt;&gt; b

\['品', '课'\]



多目标赋值

例子6.

&gt;&gt;&gt; a = 5

&gt;&gt;&gt; b = 5

&gt;&gt;&gt; a,b = 5,5



&gt;&gt;&gt; a = b = 5

&gt;&gt;&gt; a

5

&gt;&gt;&gt; b

5



顺序执行输入输出

输入：input\(\),接受的是一个字符串类型数据，输出的也是一个字符串类型数据；

特别当输入的是数值的时候，这个数值又要参与计算的时候，注意要对input输出的数字字符串进行处理



&gt;&gt;&gt; name = input\('请输入员工姓名：\n'\)

&gt;&gt;&gt; dep = input\('请输入员工部门：\n'\)

&gt;&gt;&gt; salary = input\('请输入员工工资：\n'\)



print\('员工姓名：{}'.format\(name\)\)

print\('员工部门：{}'.format\(dep\)\)

print\('员工工资：{}'.format\(salary\)\)



\#这里要注意，salary变量接受input输入的是一个字符串类型的数字，若要将salary用于计算的话，要进行适当的处理



输出：print\(\) 



例子1.

name = 'Jerry'

job = 'test'

salary = '8600.333333'



print\('员工姓名：{}'.format\(name\)\)

print\('员工工作：{}'.format\(job\)\)

print\('员工薪资：{}'.format\(salary\)\)



print\(name, job, salary, seq =' \| '\)



\#注意print在打印的时候，字符串尾部默认有一个终止符号end = '\n'

print\(name, end =','\)

print\(job, end =','\)

print\(salary, end=','\)

print\('=' \* 30\) \#分隔符



print\('薪资：{:12,.2f}'.format\(salary\)\)



 其中12代表，salary打印出来的一共有12位，不指定补位符的情况下用空格补位。

 ，代表千位显示用，识别



 打印结果为：

 薪资:     8,600.33





 

