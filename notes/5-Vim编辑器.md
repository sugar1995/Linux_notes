# 5-Vim编辑器

## 1. vim主要模式介绍

* 查询命令安装位置：rpm -qf `which vim` ； rpm -qf `which vi`。vim是vi的增加版，最明显的区别就是vim可以语法加亮，它完全兼容vi

* 主要模式有4种
1. 命令模式  默认
2. 扩展命令行模式 ':'进入，'enter'退出
3. 编辑模式，文件底部会出现Insert字样 'a/i/o/A/I/O'进入，'esc'退出
4. 虚拟编辑(可视块)模式 ，文件底部会出现Visual字样 'vV^v'切换进出

## 2. 编辑模式

* 进入编辑模式的方法:
1. i 当前字符之前插入 (光标前)
2. I 行首插入  (行首)
3. a 当前字符之后插入 (光标后)
4. A 行尾插入(行尾)
5. o下一行插入 (另起一行)
6. O上一行插入(上一行插入)
7. x 向后删除一个字符，等同于delete
8. X 向前删除一个字符，等同于backspace
9. u 撤销一步   每按一次就撤销一次
10. r 替换

## 3. 命令模式

* 光标定位：
1. HJKL(上左右下)
2. 0 和 home键表示切换到行首， $和end键表示切换到行尾
3. gg 快速定位到文档的首行 ,  G定位到未行
4. 3gg 或者 3G  快速定位到第3行
5. /string(字符串)   ----找到或定位要找的单词或内容，如果相符内容比较多，可以通过N、n来进行向上向下查找，取消高亮显示 :noh
6. /^d  ----^意思表示以什么开头 ，，查找以字母d开头的内容
7. /t$  ----$意思表示以什么结尾，，查找以字母t结尾的内容
8. vim + a.txt  打开文件后，光标会自动位于文件的最后一行

* 文本编辑 删除、剪切、复制、粘贴、撤销
1. y 复制（以字符为单位） :表示对单个字符进行复制，如果要复制整行，用yy（以行为单位）,复制N行： Nyy  ，比如： 2yy ，表示复制2行
2. dd（删除，以行为单位，删除当前光标所在行）,删除N行： Ndd  ，比如： 2dd ，表示删除2行
3. p ： P粘贴,剪切： dd
4. x 删除光标所在位置的字符
5. D 从光标处删除到行尾
6. u 撤销操作
7. ctrl+r  还原撤销过的操作，将做过的撤销操作再还原回去，也就是说撤销前是什么样，再还原成什么样
8. r 替换，或者说用来修改一个字符


