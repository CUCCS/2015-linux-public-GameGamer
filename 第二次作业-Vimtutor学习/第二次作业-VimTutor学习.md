# 第二次作业-VimTutor学习

## 实验名称

* VimTutor学习

## 实验过程

#### [第一课](https://asciinema.org/a/SqzLckcpLc7kmB2GDOAM0SIPh)

#### [第二课](https://asciinema.org/a/ujlUtCN7oKzIuH8O55ELkNFXJ)

#### [第三课](https://asciinema.org/a/M0RVQVJbp3PIUMgu6UjXoW0wx)

#### [第四课](https://asciinema.org/a/s1zbazPl4O2DrEJshtSW2PpPp)

#### [第五课](https://asciinema.org/a/mXEFqV2hJ9bT0W0SDxQNPIIJp)

#### [第六课](https://asciinema.org/a/yvVP1k6pt0FB1UEuessaETu5t)

#### [第七课](https://asciinema.org/a/3ZmX0OrYTy8QWgwQmp15gXjOa)

#### [语法高亮](https://asciinema.org/a/AjQZmzJo6uOM43SfT2DzX7yqf)

## 自查清单


* 你了解vim有哪几种工作模式？

  * 正常模式： <ESC>后进入的模式
  
  * 插入模式： ----insert----
  
  * 选择模式：-----visual----
  
  * 命令模式：在编辑状态下左下角可以输入命令
  
* Normal模式下，从当前行开始，一次向下移动光标10行的操作方法？如何快速移动到文件开始行和结束行？如何快速跳转到文件中的第N行？

  * 大写的G代表shift+g，小写代表直接按g，之后的大小写也如此

  * 跳十行：10j
  
  * 开始: gg  0G
  
  * 结束: G
  
  * 第N行： NG
  
* Normal模式下，如何删除单个字符、单个单词、从当前光标位置一直删除到行尾、单行、当前行开始向下数N行？

  * 单个字符： x
  
  * 单个单词： dw
  
  * 删到行尾： d$
  
  * 删除单行：dd
  
  * 删除向下N行： Ndd，dNd
  
* 如何在vim中快速插入N个空行？如何在vim中快速输入80个-？

  * N个空行：100o 
  
  * 80个-：<ESC>80i-<ESC>
  
* 如何撤销最近一次编辑操作？如何重做最近一次被撤销的操作？

  * u
  
  * U
  
* vim中如何实现剪切粘贴单个字符？单个单词？单行？如何实现相似的复制粘贴操作呢？

  * 剪切粘贴：
  
    * 字符：d  p
    
    * 单词：dw p
    
    * 单行：dd p
    
  * 复制粘贴：
  
    * 复制：按v，进入visual模式，用hjkl选中要复制内容，或用$到行尾，w到单词尾部，按y复制
    
    * 粘贴：p
    
* 为了编辑一段文本你能想到哪几种操作方式（按键序列）？

  * 命令行输入vim filename，然后i/o/a/c等键进入编辑模式，或是用剪切/复制/粘贴命令，编辑完成后<ESC>，:wq保存退出
  
  * 用:edit filename命令
  
* 查看当前正在编辑的文件名的方法？查看当前光标所在行的行号的方法？

  * Ctrl+g
  
* 在文件中进行关键词搜索你会哪些方法？如何设置忽略大小写的情况下进行匹配搜索？如何将匹配的搜索结果进行高亮显示？如何对匹配到的关键词进行批量替换？

  * 向前搜索(keyword为要搜索的关键词)：/keyword
  
  * 向后搜索： ？keyword
  
  * 忽略大小写： :ser ic
  
  * 设置高亮： :set hls is
  
  * 批量替换： :s/old/new/g
  
* 在文件中最近编辑过的位置来回快速跳转的方法？

  * Ctrl+i Ctr1+o
  
* 如何把光标定位到各种括号的匹配项？例如：找到(, [, or {对应匹配的),], or }

  * %
  
* 在不退出vim的情况下执行一个外部程序的方法？

  * :!+命令
  
* 如何使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法？如何在两个不同的分屏窗口中移动光标？

  * :help后加想要查的命令，例如： :help g/w
  
  * Ctrl + w

#### 问题

1. 使用apt直接安装的asciicast版本太低不能上传
    * 解决:使用官方文档中提供的方法，安装最新版本

    Ubuntu
    ```
    sudo apt-add-repository ppa:zanchey/asciinema
    
    sudo apt update
    
    sudo apt install asciinema
    ```
2. 第一次上传时卡住，等了很长时间也没有显示上传成功

    * ctrl+c结束，重新录制上传

3. 语法高亮第一次没有成功，重新配置文件后成功，文件和以前相同，不知道原因。