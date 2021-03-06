---
title: git修改最后一次提交的内容的具体步骤
abbrlink: 344f746d
date: 2017-05-20 09:50:54
tags:
---
**只是针对第一次提交**

如果发现最后一次的提交出现了错误，需要重新提交，就可以用`git commit --amend`。

比如已经提交了README.md，但是发现还有创建一个新文件一块提交

![已提交未暂存](https://cdn.ru23.com/img/2017/git修改最后一次提交的内容的具体步骤/Jietu20170520-093718.jpg)

这是就要先把新文件放到暂存区，用`git add test.html`

![已提交已暂存](https://cdn.ru23.com/img/2017/git修改最后一次提交的内容的具体步骤/Jietu20170520-093835.jpg)

再使用命令`git commit --amend`，如果出现了一种编辑的模式

![编辑状态](https://cdn.ru23.com/img/2017/git修改最后一次提交的内容的具体步骤/Jietu20170520-094641.jpg)

直接输入`:wq`然后按回车，这里需要注意的是**直接输入**，直接输入的意思就是不是先按esc或者其他的什么键，直接`shift`加L右边的键输入冒号，紧接着加上wq，也就是写入并退出。

![输入:wq](https://cdn.ru23.com/img/2017/git修改最后一次提交的内容的具体步骤/Jietu20170520-094700.jpg)

新添加到暂存区的文件就被放到同一次提交里面了。

![输入:wq](https://cdn.ru23.com/img/2017/git修改最后一次提交的内容的具体步骤/Jietu20170520-094821.jpg)

如果是不是添加新的文件，只是觉得在最后一次提交的时候有的文件没有修改完全，那就在修改完了之后，把修改的文件用`git add`加到暂存区，其他的步骤跟上面是一模一样的。

如果仅仅是想修改一下最后一次提交的提交信息，那就输入这样的命令

~~~
git commit --amend -m "新的提交信息"
~~~

就可以了，之后没有任何其他的操作
