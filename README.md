# data-structure
关于数据结构学习的心得与体会
## 1. scanf 的宽度数字含义（宽度限制）

scanf("%13s %60s %lf", book.number_book, book.name_book, &book.price) != EOF（注：这里的book.number_book, book.name_book均为char类型的数组，且前者大小为14，后者大小为61）
>>而%13s则表示scanf只读number前13个字符，%60s同理

## 2.1 EOF
EOF是stdio.h中的宏，可以当成输出的结束（即无输入）常用在不知总数的前提下输入部分数量。例如下：

<img width="1115" height="506" alt="image" src="https://github.com/user-attachments/assets/c618cd26-12a6-4b59-b1c1-a01d85bc031d" />

## 2.2 EOF与scanf返回值判断
当写scanf（“”）之类时要注意输入值是否残缺,有时候题目给的样例或者测试后台给的样例成分是残缺的，这个时候循环该结束了。

>>## 但是 如果你写scanf（“”）！=EOF,假设你需要输入三个参数，你只输入了两个，那么它会沿用上一次的第三个数据，导致循环卡死，而scanf（“”）==n(n为需要输入的参数个数）这种写法就能规避脏数据，可使循环结束
>>## ==n(n为需要输入的参数个数）用来防范输入残缺，避免脏数据；本地控制台两种写法都会阻塞，需要手动发送 EOF；OJ 读取文件，读到末尾自动生成 EOF。（主要还是为了预防文件没读完但是缺数据的情况）


## 3.减少重复输入
对于一个变量在判断时输入即可。
例子如下；
对于 int pos我在输入时一般采用scanf（%d，&pos）；
>>但是如果你写if（scanf（%d，&pos）！=1）类似这种判断语句中已经涵盖了输入语句就无需再重复写输入了。


## 4.字符串的输入与输出
对于char类型的数组，会在结尾处自动添加\0表示结束，而对于char类型数组的输入与输出则用一个%s即可搞定
>> 输入 scanf（“%s”， ）
>> 输出 printf（“%s” ，）
