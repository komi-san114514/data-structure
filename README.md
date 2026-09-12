# data-structure
关于数据结构学习的心得与体会
## 1. scanf 的宽度数字含义（宽度限制）

scanf("%13s %60s %lf", book.number_book, book.name_book, &book.price) != EOF（注：这里的book.number_book, book.name_book均为char类型的数组，且前者大小为14，后者大小为61）
>>而%13s则表示scanf只读number前13个字符，%60s同理

## 2. EOF
EOF是stdio.h中的宏，可以当成输出的结束（即无输入）常用在不知总数的前提下输入部分数量。例如下：

<img width="1115" height="506" alt="image" src="https://github.com/user-attachments/assets/c618cd26-12a6-4b59-b1c1-a01d85bc031d" />

