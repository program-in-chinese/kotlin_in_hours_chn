## 共享协议
本作使用[署名-非商业使用-禁止演绎](https://creativecommons.org/licenses/by-nc-nd/4.0/)协议共享。

# Kotlin编程一天入门 v0.0.1 alpha

## 前言

Kotlin入门代码用中文写更能被新手理解, 可惜没有看到类似教程. 本作纯属抛砖引玉, 希望各位多指出错误, 欢迎批评/意见/建议.

编程语言的语法是最机械的, 在阅读过程中, 请尽量关注于程序做了些什么, 而一些语法细节可以暂时忽略. 入门之后, 在接下去的写和读代码过程中, 语法自然会熟练起来. 推荐用30分钟先迅速浏览一遍全文, 由于代码是中文命名, 可以先对代码内容有个直观的了解. 第二遍再开始动手运行例程以及自行修改尝试.

每一讲建议时间30分钟左右. 如果卡住(比如超过一小时), 请在代码库开issue. 目的是让总时间控制在8小时左右, 让"一天入门"更符合实际.

## 目录
一 [准备编程](#%E4%B8%80-%E5%87%86%E5%A4%87%E7%BC%96%E7%A8%8B)

二 [问个好吧](#%E4%BA%8C-%E9%97%AE%E4%B8%AA%E5%A5%BD%E5%90%A7)

## 一 准备编程

编程就是让计算机做你想让它做的事.

编程语言是工具,就像画笔,应该拿上手找块空白就可以用.

为了编写第一个Kotlin程序, 我安装了Kotlin编译器, 过程参考[官方文档](https://kotlinlang.org/docs/tutorials/command-line.html).
本文的代码足够简单, 任何文本编辑器都可以编写. 写本文时用的是Visual Studio Code.

安装JDK后, 打开命令行窗口,运行kotlinc和java,不报错"command not found",即为成功,可以继续. (待续:常见问题与解决)

## 二 问个好吧

新建文本文件,命名为"问好.kt".输入最简单的一个Kotlin程序:

```
fun main(参数: Array<String>) {
    // 待续: 要让它做的事
}
```

的main是程序入口. 注意所有的大括号都需要配对. 双斜杠"//"之后的是注释,是为读代码的人方便理解写的,不影响编译运行.
"参数"很扎眼吧,不用急,第四讲就知道它做什么了.

这个程序可以编译运行(见"手把手"部分),但运行后没有任何输出.因为这个程序是个空架子,没有任何可以看到的运行结果.下面就让它做点事.

```
fun main(参数: Array<String>) {
    // 要让它做的事
    println("吃了么");
}

```

加上的这行代码将打印一行字,内容是"吃了么".

试试编译运行,将看到命令行下输出:
```
吃了么
```

试试改字符串的内容,再编译运行.恭喜! 你已经可以写出无数个不同的Kotlin程序了.
再试试加一行相同的代码,输出结果变了吗? 恭喜! 你已经可以写出无限长的Kotlin程序了.

### 手把手:
在命令行下编译和运行
#### 编译:
在程序文件的目录下,运行下面的命令
```
$ kotlinc 问好.kt -include-runtime -d 问好.jar
```
此命令将程序文件编译生成.jar,在这个目录下多了一个"问好.jar"文件

(TODO: Windows下测试)
```
#### 运行
下面的命令寻找并运行叫"问好"的类:
```
$ java -jar 问好.jar
```
