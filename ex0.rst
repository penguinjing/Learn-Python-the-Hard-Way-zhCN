习题 0: 准备工作
*********************

这道习题并没有代码内容，它的主要目的是让你在计算机上安装好 Python。你应该尽量\
照着说明进行操作，例如 Mac OSX 默认已经安装了 Python 2，所以就不要在上面安装\
Python 3 或者别的 Python 版本了。

.. warning::

    如果你不知道怎样使用 Windows 下的 PowerShell，或者 OSX 下的 Terminal，\
    或者 Linux 下的“bash”，那你就需要学习了。我有一个免费的快速入门教程放在
    http://cli.learncodethehardway.org/，你可以快速学到 PowerShell 和
    Terminal 的基本用法。学完后再回来看这本书吧。

Mac OSX
=======

你需要做下列任务来完成这个练习：

1. 用浏览器打开 http://www.barebones.com/products/textwrangler/ 找到并安装 ``TextWrangler`` 文本编辑器。
2. 把 TextWrangler (也就是你的编辑器) 放到 Dock 中，以方便日后使用。
3. 找到系统中的 “命令行终端(Terminal)” 程序。到处找找，你会找到的。
4. 把 Terminal 也放到 Dock 里面。
5. 运行 Terminal 程序，这个程序看上去不怎么地。
6. 在 Terminal 程序里边运行 ``python``\。运行的方法是输入程序的名字再敲一下回车。
7. 敲击 CTRL-D (^D) 退出 python。
8. 这样你就应该退回到敲 ``python`` 前的提示界面了。如果没有的话自己研究一下为什么。
9. 学着使用 Terminal 创建一个目录，你可以上网搜索怎样做。
10. 学着使用 Terminal 进入一个目录，同样你可以上网搜索。
11. 使用你的编辑器在你进入的目录下建立一个文件。你将建立一个文件。使用 “Save” 或者 “Save As...” 选项，然后选择这个目录。
12. 使用键盘切换回到 Terminal 窗口，如果不知道怎样使用键盘切换，你一样可以上网搜索。
13. 回到 Terminal，看看你能不能使用命令看到你新建的文件，上网搜索如何将文件夹中的内容列出来。


OSX: 你应该看到的结果
------------------------

以下是我在自己电脑的 Terminal 中执行上述练习时看到的内容。和你做的结果会有一些不同，所以看看你能不能找出两者不同点来。

.. code-block:: console
    
    Last login: Sat Apr 24 00:56:54 on ttys001
    ~ $ python
    Python 2.5.1 (r251:54863, Feb  6 2009, 19:02:12) 
    [GCC 4.0.1 (Apple Inc. build 5465)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> ^D
    ~ $ mkdir mystuff
    ~ $ cd mystuff
    mystuff $ ls
    # ... 使用 TextWrangler 编辑 test.txt ...
    mystuff $ ls
    test.txt
    mystuff $ 

Windows
=======

.. note:: 感谢 zhmark 的贡献。

1. 用浏览器打开 http://notepad-plus-plus.org/ 下载并安装 ``Notepad++`` 文本编辑器。这个操作无需管理员权限。
2. 把 ``Notepad++`` 放到桌面或者快速启动栏，这样你就可以方便地访问到该程序了。这两条在安装选项中可以看到。
3. 从开始菜单运行“PowerShell”程序。你可以使用开始菜单的搜索功能，输入名称后敲回车即可打开。
4. 为它创建一个快捷方式，放到桌面或者快速启动栏中以方便使用。
5. 运行命令行终端程序(也就是 PowerShell)，这个程序看上去不怎么地。
6. 在命令行终端里边运行 ``python``\。运行的方法是输入程序的名字再敲一下回车。
    a. 如果你运行 ``python`` 发现它不存在(``python 不是可执行命令，或者系统找不到python云云``)。你需要访问 http://python.org/download 并且安装 Python。
    b. 确认你安装的是 **Python 2** 而不是 Python 3。
    c. 你也可以试试 ActiveState Python，尤其是你没有管理员权限的时候。
    d. 如果你安装好了但是 ``python`` 还是不能被识别，那你需要在 powershell 下输入并执行以下命令：
   
        ``[Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\Python27", "User")``
   
    e. 关闭并重启 powershell，确认 python 现在可以运行。如果不行的话你可能需要重启电脑。
7. 键入 CTRL-Z (^Z)，再敲回车以退出 ``python``\。
8. 这样你就应该退回到敲 ``python`` 前的提示界面了。如果没有的话自己研究一下为什么。
9. 学着使用 Terminal 创建一个目录，你可以上网搜索怎样做。
10. 学着使用 Terminal 进入一个目录。同样你可以上网搜索。
11. 使用你的编辑器在你进入的目录下建立一个文件。你将建立一个文件，使用 "Save" 或者 "Save As..." 选项，然后选择这个目录。
12. 使用键盘切换回到 Terminal 窗口，如果不知道怎样使用键盘切换，你一样可以上网搜索。
13. 回到 Terminal，看看你能不能使用命令看到你新建的文件，上网搜索如何将文件夹中的内容列出来。


.. warning::

    有时这一步你会漏掉：Windows 下装了 Python 但是没有正确配置路径。
    确认你在 ``powershell`` 下输入了 ``[Environment]::SetEnvironmentVariable("Path", "$env:Path;C:\Python27", "User")``\。你也许需要重启 powershell 或者计算机来让路径设置生效。

Windows: 你应该看到的结果
--------------------------


.. code-block:: console

    > python
    ActivePython 2.6.5.12 (ActiveState Software Inc.) based on
    Python 2.6.5 (r265:79063, Mar 20 2010, 14:22:52) [MSC v.1500 32 bit (Intel)] on win32
    Type "help", "copyright", "credits" or "license" for more information.
    >>> ^Z


    > mkdir mystuff

    > cd mystuff

    ... 使用 Notepad++ 编辑 mystuff 目录下的 test.txt ...

    >
       <如果你没有使用管理员权限安装，你会看到一堆错误。忽略它们，按回车即可。>
    > dir
     Volume in drive C is
     Volume Serial Number is 085C-7E02

     Directory of C:\Documents and Settings\you\mystuff

    04.05.2010  23:32    <DIR>          .
    04.05.2010  23:32    <DIR>          ..
    04.05.2010  23:32                 6 test.txt
                   1 File(s)              6 bytes
                   2 Dir(s)  14 804 623 360 bytes free

    > 

你看到的命令行信息，Python 信息，以及其它一些东西可能会非常不一样，不过应该大致不差。你可以通过 http://learnpythonthehardway.org 把你找到的错处告诉我们，我们会修正过来。


Linux
=====

Linux 系统可谓五花八门，安装软件的方式也各有不同。我们假设作为 Linux 用户的你已经知道如何安装软件包了，以下是给你的操作说明：

1. 1. 用浏览器打开 http://learnpythonthehardway.org/exercise0.html 下载并安装 ``gedit`` 文本编辑器。
2. 把 gedit (也就是你的编辑器) 放到窗口管理器显见的位置，以方便日后使用。
    a. 运行 gedit，我们要先改掉一些愚蠢的默认设定。
    b. 从 ``gedit menu`` 中打开 ``Preferences``\，选择 ``Editor`` 页面。
    c. 将 ``Tab width:`` 改为 4。
    d. 选择 (确认有勾选到该选项) ``Insert spaces instead of tabs``\。
    e. 然后打开 “Automatic indentation” 选项。
    f. 转到 ``View`` 页面，打开 "Display line numbers" 选项。
3. 找到 "Terminal" 程序。它的名字可能是 ``GNOME Terminal``\、\ ``Konsole``\、或者 ``xterm``\。
4. 把 Terminal 也放到 Dock 里面。
5. 运行 Terminal 程序，这个程序看上去不怎么地。
6. 在 Terminal 程序里边运行 ``python``\。运行的方法是输入程序的名字再敲一下回车。
   a. 如果你运行 ``python`` 发现它不存在的话，你需要安装它，而且要确认你安装的是 Python 2 而非 Python 3。
7. 敲击 CTRL-D (^D) 以退出 ``python``\。
8. 这样你就应该退回到敲 ``python`` 前的提示界面了。如果没有的话自己研究一下为什么。
9. 学着使用 Terminal 创建一个目录。你可以上网搜索怎样做。
10. 学着使用 Terminal 进入一个目录。同样你可以上网搜索。
11. 使用你的编辑器在你进入的目录下建立一个文件。你将建立一个文件，使用 “Save” 或者 “Save As...” 选项，然后选择这个目录。
12. 使用键盘切换回到 Terminal 窗口，如果不知道怎样使用键盘切换，你一样可以上网搜索。
13. 回到 Terminal，看看你能不能使用命令看到你新建的文件，上网搜索如何将文件夹中的内容列出来。


Linux: 你应该看到的结果
--------------------------


.. code-block:: console

    [~]$ python
    Python 2.6.5 (r265:79063, Apr  1 2010, 05:28:39)
    [GCC 4.4.3 20100316 (prerelease)] on linux2
    Type "help", "copyright", "credits" or "license" for more information.
    >>>
    [~]$ mkdir mystuff
    [~]$ cd mystuff
    # ... 使用gedit编辑text.txt ...
    [mystuff]$ ls
    test.txt
    [mystuff]$ 

你看到的命令行信息，Python 信息，以及其它一些东西可能会非常不一样。不过应该大致不差就是了。


给新手的告诫
======================

你已经完成了这节练习，取决于你对计算机的熟悉程度，这个练习对你而言可能会有些难。\
如果你觉得有难度的话，你要自己克服困难，多花点时间学习一下。因为如果你不会这些\
基础操作的话，编程对你来说将会更难学习。

如果有程序员告诉你让你使用 ``vim`` 或者 ``emacs``\，那你应该拒绝他们。当你成为\
一个更好的程序员的时候，这些编辑器才会适合你使用。你现在需要的只是一个可以编辑\
文字的编辑器。我们使用 ``gedit`` 是因为它很简单，而且在不同的系统上面使用起来\
是一样的。就连专业程序员也会使用 ``gedit``\，所以对于初学而言它已经足够了。

也许有程序员会告诉你让你安装和学习 Python 3。你应该告诉他们“等你电脑里的所有\
python 代码都支持 Python 3 了，我再试着学学吧。”你这句话足够他们忙活个十来年的了。

总有一天你会听到有程序员建议你使用 Mac OSX 或者 Linux。如果他喜欢字体美观，他\
会告诉你让你弄台 Mac OSX 计算机，如果他们喜欢操作控制而且留了一部大胡子，他会\
让你安装 Linux。这里再次向你说明，只要是一台手上能用的电脑就可以了。你需要的只\
有三样东西: ``gedit``\、一个命令行终端、还有 ``python``\。

最后要说的是这节练习的准备工作的目的，也就是让你可以在以后的练习中顺利地做到下面的这些事情：

1. **写出**\习题的代码，在 Linux 下用 ``gedit``\，OSX 下用 ``TextWrangler``\，Windows
下用 ``Notepad++``\。
2. **运行**\你写的习题。
3. **修改**\错误的地方。
4. 重复上述步骤。

其他的事情只会让你更困惑，所以还是坚持按计划进行吧。

