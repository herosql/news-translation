> -  原文地址：[The Go Handbook – Learn Golang for Beginners](https://www.freecodecamp.org/news/go-beginners-handbook/)
> -  原文作者：[Flavio Copes](https://www.freecodecamp.org/news/author/flavio/)
> -  译者：herosql
> -  校对者：

![Go语言手册-面对go语言的初学者](https://www.freecodecamp.org/news/content/images/size/w2000/2022/10/pexels-christina-morillo-1181290.jpg)

Go语言是一门非常棒的,简单的,现代化的,性能特别高的编程语言.

它是编译类型,开源的,强类型语言.

Golang – 也可以称为 Go – 谷歌工程师创造这门语言的主要目标:

-   让他们的项目编译(和运行)快
-   是简单的,这样人们可以很短的时间就能用起来
-   足够低的水平,但也要避免一些水平过低的陷阱
-   具有可移植(经过编译的GO程序不需要其他文件的支持,就可以跨平台运行,因此它们很容易分发)
-   具有简单,稳定的,可以预测性,从而减少犯错的机会
-   使得利用多处理器系统变得容易

Go是基于C和C++.它做一些东西特别简单像并发和内存的管理,和垃圾回收.

当然,它是基于C和C++构建的,它具有很多C语言的特性.

你可以用GO做很多不一样的任务,它既可以解决简单的问题也可以解决复杂的问题.

你可以用Go做命令行的工具和网络服务器,它还可以跨多个不同的学科使用.

举个例子,Docker和K8s是用Go编写的.

我最喜欢的静态网站生成工具Hugo是用Go编写的.

Caddy,一个非常流行的web服务器是用GO编写的.

这些形色各异,广泛使用的工具都是用这门编程语言作为基础创建.

这本手册将向你介绍Go编程语言,使得你开始使用Go编写程序.

[你可以点击链接获得pdf版本和ePub版本的GO初学者手册](https://thevalleyofcode.com/download/go/).

## 目录内容

1.  [怎么获得Go](#how-to-get-started-with-go)
2.  [怎么安装Go语言环境](#how-to-install-go)
3.  [怎么选择你的编辑器](#how-to-setup-your-editor)
4.  [怎么用Go编写Hello,World!](#how-to-write-hello-world-in-go)
5.  [怎么编译和运行Go程序](#how-to-compile-and-run-a-go-program)
6.  [Go的工作空间](#the-go-workspace)
7.  [深入Go语言](#diving-into-the-go-language)
8.  [Go中的变量](#variables-in-go)
9.  [Go的基础类型](#basic-types-in-go)
10.  [Go中的字符串](#strings-in-go)
11.  [Go中的数组](#arrays-in-go)
12.  [Go中的切片](#slices-in-go)
13.  [Go中的哈希表](#maps-in-go)
14.  [Go中的循环](#loops-in-go)
15.  [Go中的条件运算符](#conditionals-in-go)
16.  [Go中的运算符](#operators-in-go)
17.  [Go中的结构体](#structs-in-go)
18.  [Go中的函数](#functions-in-go)
19.  [Go中的指针](#pointers-in-go)
20.  [Go中的方法](#methods-in-go)
21.  [Go中的接口](#interfaces-in-go)
22.  [以后的路](#where-to-go-from-here)

## 怎样开始获得Go

在我们深入语言特性之前,我们首先得知道一些东西

首先, [https://go.dev](https://go.dev/) 这是语言的官网. 在官网你可以获得的资料:

-   下载Go的二进制包 (是 `go` 命令和发行的工具)  [https://go.dev/doc/install](https://go.dev/doc/install)
-   Go的官方文档 [https://go.dev/doc/](https://go.dev/doc/)
-   看到Go的所有第三方库 [https://pkg.go.dev/](https://pkg.go.dev/)
-   Go的在线游乐园 [https://go.dev/play/](https://go.dev/play/)

…待续.

## 怎么安装Go语言环境

到 [https://go.dev/doc/install](https://go.dev/doc/install) 下载你电脑使用的操作系统的Go程序包.

运行并安装,在最后一个步骤你需要在命令行设置`go`命令:

![Screen Shot 2022-07-28 at 10.19.21.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_10.19.21.png)

欢迎进行Go的安装

![Screen Shot 2022-07-28 at 10.20.54.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_10.20.54.png)

安装成功

打开命令行并运行 `go version` 你会看到以下内容:

![Screen Shot 2022-07-28 at 10.21.32.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_10.21.32.png)

展示你当前的Go版本

说明: 你如果在你允许Go的安装程序之前打开的命令行窗口,你可能看不到以上效果.

执行本地的Go安装文件会依赖于你的操作系统.

在mac系统中,它在`/usr/local/go`, 运行文件在`/usr/local/go/bin`.

在Windows系统中,它在`C:\Program Files\go`.

在Windows和Mac安装中Go执行文件路径都是自动设定的.

在Mac你可以在Homebrew中使用`brew install golang`命令安装. 这样方式更容易升级最新版本.

在Linux上你在运行`go`命令之前需要配置环境变量,配置Linux环境变量的路径`/usr/local/go`的命令:

```bash
echo 'export PATH=$PATH:/usr/local/go/bin' >> $HOME/.profile
source $HOME/.profile
```

## 怎么选择你的编辑器

我推荐使用 [**Visual Studio Code**](https://code.visualstudio.com/) (也叫 VS Code) 作为你的编辑器.

阅读 [在 Visual Studio Code 编写Go](https://code.visualstudio.com/docs/languages/go) 查看 “up and running” 安装. 在最小版,  安装[Go的扩展](https://marketplace.visualstudio.com/items?itemName=golang.go).

![Screen Shot 2022-07-28 at 10.54.06.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_10.54.06.png)

在VSCode中的Go扩展

这个扩展可以让你的生活更加轻松.在生产产品(符号高亮,自动编译,动态信息提示,高亮...)和其他的功能如自动格式化,可以选择性的安装其他包,测试,还有更多.

## 怎么用Go编写Hello,World!

现在我们准备创建我们第一个Go程序!

它是一个程序员创建第一个程序,它会在运行的时候在命令行输入“Hello, World!” 字符串.在我们做第一个程序的同时,我们解释一下我们为什么这样做.

或许你可以在你的目录下创建一个文件夹保存你所有编写的项目和测试.

在这,创建一个新的文件夹,比如取名叫`hello`.

在这,创建一个叫`hello.go` 的文件 (你可以用任何想要用的名字).

文件内容如下:

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

![Screen Shot 2022-07-28 at 12.17.14.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_12.17.14.png)

Go "Hello, World!" 代码

这是你编写的第一个Go程序!

开始一行行的解析.

```go
package main
```

我们通过包的形式组织Go程序.

每一个`.go` 文件首先声明包的部分.

一个包可以放多个文件,或者一个文件.

一个程序可以由多个包组成.

这个 `main` 是程序识别可执行程序用的.

```go
import "fmt"
```

我们可以使用 `import` 关键字导入一个包.

`fmt` 是Go提供的输入/输出工具函数包.

我们有[第三方包仓库](https://pkg.go.dev/std) 可以通过网络使用我们想要用的任何包,如数据计算库,加密库,图片处理库,文件系统操作库等更多.

你可以阅读关于`fmt` 包提供的全部功能 [在介绍文档中](https://pkg.go.dev/fmt).

```go
func main() {
	
}
```

这里我们声明名为 `main()` 的函数.

什么是函数?我们待会再看,但是在实际含义中一个函数是一段代码块,包括名字,内部的一些结构.

这个`main`函数是特殊的因为这也是程序启动的地方. 

在这个简单的案例中我们只是有一个函数-这个程序启动和结束在一起.

```go
fmt.Println("Hello, World!")
```

这是我们在函数中的定义.

我们调用了我们引入的`fmt`包中`Println()` 函数,会输出一个字符串.

这个函数的描述在[文档中](https://pkg.go.dev/fmt#Printf) "_formats according to a format specifier and writes to standard output_”.

看一下他们伟大的源码,他们有提供示例,你可以试着运行:

![Screen Shot 2022-07-28 at 14.18.46.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_14.18.46.png)

Go基础的函数模板

我们可以用 “dot” 符号 `fmt.Println()` 获得包中提供的函数的特性.

在执行代码`main`函数之后,它没有做其他的事就结束了执行.

## 怎么编译和运行Go程序

现在在`hello`文件夹下打开命令行,用以下命令运行程序:

```bash
go run hello.go
```

![Screen Shot 2022-07-28 at 12.18.23.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_12.18.23.png)

Go 输出 Hello world 

我们的程序运行成功,它会在命令行输出“Hello, World!” .

这个`go run`会先编译并运行程序.

你可以用`go build`创建一个**可执行文件**:

```bash
go build hello.go
```

这里会创建一个名为`hello`的可执行文件,你可以执行:

![Screen Shot 2022-07-28 at 12.19.50.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_12.19.50.png)

执行Go的可执行文件

在引言部分我提到过Go是轻便的.

现在你可以分发这个可执行文件到每一个可以运行程序的地方,但是这个可执行文件是可以执行的.

这个程序可以运行这和我们的编译有关系.

我们可以创建不一样的可执行文件,通过环境变量`GOOS` 和 `GOARCH`如:

```go
GOOS=windows GOARCH=amd64 go build hello.go
```

 这将会创建`hello.exe`文件,可以在64位的Windows机器上运行:

![Screen Shot 2022-07-28 at 15.36.55.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_15.36.55.png)

Hello.exe 执行

设置64位的Mac的环境变量为`GOOS=darwin GOARCH=amd64` ,Linux的环境变量是`GOOS=linux GOARCH=amd64`.

这个Go最好的特性之一.

## Go的工作空间

关于Go中的一个特殊的点,我们称为 **工作区**.

这个工作区是 Go中的 “家目录”.

Go默认的路径在`$HOME/go`下,所以你可以在你的家目录中看到`go`文件夹.

它会在你安装包(待会我们看一下)进行创建.

在示例中我在VS Code中加载`hello.go`文件, 它会安装`[gopls](https://pkg.go.dev/golang.org/x/tools/gopls)` 命令, 开发调试工具(`dlv`), 和[`静态检查`行](https://staticcheck.io/).

他们会自动安装到`$HOME/go`路径下:

![Screen Shot 2022-07-28 at 12.27.27.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_12.27.27.png)

`$HOME/go`

当你使用`go install`安装库时, 他们会出现在这里.

这就是我们讲的**GOPATH**.

你可以修改环境变量`GOPATH`来决定库文件的位置.

同在在不同项目工作的时候你可以按你想要库的方式来设置.

## 深入Go语言

现在我们编写了一个部分,我们运行了第一个Hello, World! 程序, 我们可以深入Go语言了.

这门语言不是在白板上凭空产生的,它像 C, C++, Rust, Java, JavaScript, 但是不像Python,在白板上定义了语言的特性.

分号结束符是可选的, 像 JavaScript (不像 C, C++, Rust 和 Java).

Go对动态缩进和视觉次序很重视.

在我们安装Go程序的时候自带了`gofmt`命令,我们可以用它对Go程序进行格式化. 在VS Code中可以对Go源码文件进行格式化. 

这是非常重要的,因为格式和问题像tab符和空格符或者是“我是否应该将循环体放在下一行”这些问题浪费很多时间 .

语言在创建的时候就定义了规则,每个人都使用这些规则.

这对于拥有大型团队的项目非常有用.

我推荐你在VS Code中设置 “**保存时格式化**” 和 “**粘贴时格式化**”:

![Screen Shot 2022-07-28 at 14.39.42.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_14.39.42.png)

在VS Code 中设置Go的粘贴时格式化和保存时格式化

你可以使用常用的 C / C++ / JavaScript / Java 语法在Go中写注释:

```go
// this is a line comment

/*
multi
line
comment
*/
```

## Go中的变量

你在使用编程语言时第一件做的事就是定义一个变量.

在Go中我们用`var`关键字声明变量:

```go
var age = 20
```

你可以定义包作用域的变量:

```go
package main

import "fmt"

var age = 20

func main() {
	fmt.Println("Hello, World!")
}
```

或是在函数中:

```go
package main

import "fmt"

func main() {
	var age = 20

	fmt.Println("Hello, World!")
}
```

定义在包中,一个变量可以在包中的所有文件中进行使用.多个文件可以放在一个包里面,你只需要在创建另一个文件并在同样的包名写在文件顶部.

定义在函数中,一个变量只能在函数内使用.它会在调用函数时进行初始化,函数执行结束时销毁.

我们使用以下示例:

```go
var age = 20
```

我们设置变量`age`的值为`20`.

Go使用默认定义这里变量 `age` 的**类型**是 `int`.

我们待会看到更多其他的类型,但你应该知道各种的类型的不同之处,比如`int`, `string`, 和 `bool`.

我们可以不给变量设置值,但是必须设置它们的类型如下:

```go
var age int
var name string
var done bool
```

当你知道值时,你可以直接用短的变量声明如 `:=` 运算符:

```go
age := 10
name := "Roger"
```

变量名你可以使用小写字母,数字和`_`或者可以使用类似于`_`的其他字符.

名字是**区分大小写**的.

如果名字太长,通常可使用驼峰命名法,例如我们想表现车的名字就用`carName`.

你可以使用赋值运算符`=`给一个变量赋予新的值.

```go
var age int
age = 10
age = 11
```

如果你有一个变量在编程过程中永远都不会变,你可以使用`const`关键字来声明这个变量:

```go
const age = 10
```

你可以一行代码中声明多个变量:

```go
var age, name
```

将它们全部都初始化:

```go
var age, name = 10, "Roger"

//or

age, name := 10, "Roger"
```

在程序中使用未声明的变量,程序会报错,而且无法通过编译.

在VS Code中你可以看到警告如下:

![Screen Shot 2022-07-28 at 15.45.31.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_15.45.31.png)

使用未声明变量的警告

以下是编译的报错:

![Screen Shot 2022-07-28 at 15.45.44.png](https://www.freecodecamp.org/news/content/images/2022/10/Screen_Shot_2022-07-28_at_15.45.44.png)

使用未声明变量的编译期报错

如果你声明了一个变量且没有给这个变量一个初始值,它会自动初始化一个对应类型的初始值,例如integer类型的值为`0`而字符串的值是一个空的字符串.

## Go的基础类型

Go是一门强类型语言.

我们可以看到你怎么定义一个变量,指定它的类型:

```go
var age int
```

或者你可以直接给变量赋予初始值,让Go来推断它的类型:

```go
var age = 10
```

这些是Go中的基础类型:

-   整型 (`int`, `int8`, `int16`, `int32`, `rune`, `int64`, `uint`, `uintptr`, `uint8`, `uint16`, `uint64`)
-   浮点型 (`float32`, `float64`), 用于表示带小数点的数
-   复数类型 (`complex64`, `complex128`),常用于科学计算中
-   字符型 (`byte`), 表示一个ASCII字符
-   字符串 (`string`), 一个`byte`的集合
-   布尔型 (`bool`)表示true或false

我们有很多不同类型的整数类型,在大多数情况下你只会用到`int`,在你需要进行很多特殊的优化的时候(你可以在需要考虑使用的时候再学习)

在你使用64位系统的时候`int`类型默认为64位, 使用32位系统的时候`int`类型默认为32位,其他的与此类似.

`uint` 类型是无符号的`int`类型,如果你知道这个数字不是负数,你可以用这个类型存储比现在大两倍的数字.

所有的基础类型都是**值类型**, 这意味着当它们作为参数传递或从函数返回时,它们通过**值传递**给函数.

## Go中的字符串

Go中的字符串是一系列`byte`值.

像我们所看到的一样,你可以定义字符串如下:

```go
var name = "test"
```

其中很重要一点是不像其他语言,字符串定义只能使用双引号表示,而不是单引号.

获得字符串的长度,可以使用内置函数`len()`:

```go
len(name) //4
```

你可以用方括号访问单独字符,使用索引来取得你想要的字符:

```go
name[0] //"t" (indexes start at 0)
name[1] //"e"
```

你可以使用切片获取到字符串:

```go
name[0:2] //"te"
name[:2]  //"te"
name[2:]  //"st"
```

你可以创建一个字符串的副本:

```go
var newstring = name[:]
```

你可以将字符串赋值给一个新的变量,如下:

```go
var first = "test"
var second = first
```

字符串是**不可变**的, 所以你无法修改字符串的值.

如果你给`first`赋予一个新值,`second`的值依然是`"test"`:

```go
var first = "test"
var second = first

first = "another test"

first  //"another test"
second //"test"
```

字符串是类型,意味着如果你将一个字符串传递给一个方法,字符串**引用**会被复制,而不是它的值,但是字符串是不可变的,所在在实践过程中它和`int`类型并没有很大的区别,例如.

你可以通过`+`运算符连接两个字符串:

```go
var first = "first"
var second = "second"

var word = first + " " + second  //"first second"
```

Go提供了`strings`库来进行字符串的操作.

我们已经知道怎么在“Hello, World!”的案例中引入一个包.

这里你可以引入`strings`:

```go
package main

import (
    "strings"
)
```

你可以使用它了.

在例子中我们使用`HasPrefix()`函数来判断一个字符串的开头是否是以另一个子串开头的:

```go
package main

import (
    "strings"
)

func main() {
    strings.HasPrefix("test", "te") // true
}
```

你可以在这找到所有的函数列表: [https://pkg.go.dev/strings](https://pkg.go.dev/strings).

以下是你经常会用到的函数列表:

-   `strings.ToUpper()` 返回一个新的字符串, 大写
-   `strings.ToLower()` 返回一个新的字符串, 小写
-   `strings.HasSuffix()` 检查是否以某子串结尾
-   `strings.HasPrefix()` 检查是否以某子串开头
-   `strings.Contains()` 检查是否包含某字串
-   `strings.Count()` 计算一个某子串在当前字符串出现的次数
-   `strings.Join()` 创建一个新的字符串并连接多个字符串
-   `strings.Split()` 创建一个数组来保存通过特殊字符串对字符串进行分割的结果,例如通常使用空格
-   `strings.ReplaceAll()` 使用替换,可以使用一个新的字符串替换掉原字符中的字符串

## Arrays in Go

Arrays are a sequence of items of a single type.

We define an array in this way:

```go
var myArray [3]string //an array of 3 strings
```

and you can initialize the array with values using:

```go
var myArray = [3]string{"First", "Second", "Third"}
```

In this case you can also let Go do some work and count the items for you:

```go
var myArray = [...]string{"First", "Second", "Third"}
```

An array can only contain values of the same type.

The array cannot be resized – you have to explicitly define the length of an array in Go. That’s part of the _type_ of an array. Also, you cannot use a variable to set the length of the array.

Due to this limitation, arrays are rarely used directly in Go. Instead we use **slices** (more on them later). Slices use arrays under the hood, so it’s still necessary to know how they work.

You can access an item in the array with the square brackets notation we already used in strings to access a single character:

```go
myArray[0] //indexes start at 0
myArray[1]
```

You can set a new value for a specific position in the array:

```go
myArray[2] = "Another"
```

And you can get the length of an array using the `len()` function:

```go
len(myArray)
```

Arrays are **value types**. This means copying an array:

```go
anotherArray := myArray
```

or passing an array to a function, or returning it from a function, creates a copy of the original array.

This is different from other programming languages out there.

Let’s make a simple example where we assign a new value to an array item after copying it. See, the copy doesn't change:

```go
var myArray = [3]string{"First", "Second", "Third"}
myArrayCopy := myArray
myArray[2] = "Another"

myArray[2]     //"Another"
myArrayCopy[2] //"Third"
```

Remember you can only add a single type of items in an array, so setting the `myArray[2] = 2` for example will raise an error.

Low-level elements are stored continuously in memory.

## Slices in Go

A slice is a data structure similar to an array, but it can change in size.

Under the hood, slices use an array and they are an abstraction built on top of them that makes them more flexible and useful (think about arrays as lower level).

You will use slices in a way that’s very similar to how you use arrays in higher level languages.

You define a slice similarly to an array, omitting the length:

```go
var mySlice []string //a slice of strings
```

You can initialize the slice with values:

```go
var mySlice = []string{"First", "Second", "Third"}

//or

mySlice := []string{"First", "Second", "Third"}
```

You can create an empty slice of a specific length using the `make()` function:

```go
mySlice := make([]string, 3) //a slice of 3 empty strings
```

You can create a new slice from an existing slice, appending one or more items to it:

```go
mySlice := []string{"First", "Second", "Third"}

newSlice := append(mySlice, "Fourth", "Fifth")
```

Note that we need to assign the result of `append()` to a new slice, otherwise we’ll get a compiler error. The original slice is not modified – we’ll get a brand new one.

You can also use the `copy()` function to duplicate a slice so it does not share the same memory of the other one and is independent:

```go
mySlice := []string{"First", "Second", "Third"}

newSlice := make([]string, 3)

copy(newSlice, mySlice)
```

If the slice you’re copying to does not have enough space (is shorter than the original) only the first items (until there’s space) will be copied.

You can initialize a slice from an array:

```go
myArray := [3]string{"First", "Second", "Third"}

mySlice = myArray[:]
```

Multiple slices can use the same array as the underlying array:

```go
myArray := [3]string{"First", "Second", "Third"}

mySlice := myArray[:]
mySlice2 := myArray[:]

mySlice[0] = "test"

fmt.Println(mySlice2[0]) //"test"
```

Those 2 slices now share the same memory. Modifying one slice modifies the underlying array and causes the other slice generated from the array to be modified, too.

As with arrays, each item in a slice is stored in memory in consecutive memory locations.

If you know you need to perform operations on the slice, you can request it to have more capacity than initially needed. This way, when you need more space, the space will be readily available (instead of finding and moving the slice to a new memory location with more space to grow and dispose via garbage collection of the old location).

We can specify the **capacity** by adding a third parameter to `make()`:

```go
newSlice := make([]string, 0, 10)
//an empty slice with capacity 10
```

As with strings, you can get a portion of a slice using this syntax:

```go
mySlice := []string{"First", "Second", "Third"}

newSlice := mySlice[:2] //get the first 2 items
newSlice2 := mySlice[2:] //ignore the first 2 items
newSlice3 := mySlice[1:3] //new slice with items in position 1-2
```

## Maps in Go

A map is a very useful data type in Go.

In other language it’s also called a _dictionary_ or _hash map_ or _associative array_.

Here’s how you create a map:

```go
agesMap := make(map[string]int)
```

You don’t need to set how many items the map will hold.

You can add a new item to the map in this way:

```go
agesMap["flavio"] = 39
```

You can also initialize the map with values directly using this syntax:

```go
agesMap := map[string]int{"flavio": 39}
```

You can get the value associated with a key using:

```go
age := agesMap["flavio"]
```

You can delete an item from the map using the `delete()` function in this way:

```go
delete(agesMap, "flavio")
```

## Loops in Go

One of Go’s best features is to give you fewer choices.

We have one loop statement: `for`.

You can use it like this:

```go
for i := 0; i < 10; i++ {
	fmt.Println(i)
}
```

We first initialize a loop variable, then we set the _condition_ we check for with each iteration to decide if the loop should end. Finally we have the _post statement_, executed at the end of each iteration, which in this case increments `i`.

`i++` increments the `i` variable.

The `<` _operator_ is used to compare `i` to the number `10` and returns `true` or `false`, determining if the loop body should be executed or not.

We don’t need parentheses around this block, unlike other languages like C or JavaScript.

Other languages offer different kind of loop structures, but Go only has this one. We can simulate a `while` loop, if you’re familiar with a language that has it, like this:

```go
i := 0

for i < 10 {
	fmt.Println(i)
  i++
}
```

We can also completely omit the condition and use `break` to end the loop when we want:

```go
i := 0

for {
	fmt.Println(i)

	if i < 10 {
		break
	}

  i++
}
```

I used a `if` statement inside the loop body, but we haven’t seen _conditionals_ yet! We’ll do that next.

One thing I want to introduce now is `range`.

We can use `for` to iterate through an array using this syntax:

```go
numbers := []int{1, 2, 3}

for i, num := range numbers {
	fmt.Printf("%d: %d\n", i, num)
}

//0: 1
//1: 2
//2: 3
```

Note: I used `fmt.Printf()` which allows us to print any value to the terminal using the _verbs_ `%d` which mean _decimal integer_ and `\n` means add a line terminator.

It’s common to use this syntax when you don’t need to use the index:

```go
for _, num := range numbers {
  //...
}
```

We're using the special `_` character that means “ignore this” to avoid the Go compiler raising an error saying “you’re not using the `i` variable!”.

## Conditionals in Go

We use the `if` statement to execute different instructions depending on a condition:

```go
if age < 18 {
	//underage
}
```

The `else` part is optional:

```go
if age < 18 {
	//underage
} else {
  //adult
}
```

and can be combined with other `if`s:

```go
if age < 12 {
	//child
} else if age < 18  {
  //teen
} else {
	//adult
}
```

If you define any variable inside the `if`, that’s only visible inside the `if` (same applies to `else` and anywhere you open a new block with `{}`).

If you’re going to have many different if statements to check a single condition, it’s probably better to use `switch`:

```go
switch age {
case 0: fmt.Println("Zero years old")
case 1: fmt.Println("One year old")
case 2: fmt.Println("Two years old")
case 3: fmt.Println("Three years old")
case 4: fmt.Println("Four years old")
default: fmt.Println(i + " years old")
}
```

Compared to C, JavaScript, and other languages, you don’t need to have a `break` after each `case`.

## Operators in Go

We've used some operators so far in our code examples, like `=`, `:=` and `<`.

Let’s talk a bit more about them.

We have assignment operators `=` and `:=` we use to declare and initialize variables:

```go
var a = 1

b := 1
```

We have comparison operators `==` and `!=` that take 2 arguments and return a boolean:

```go
var num = 1
num == 1 //true
num != 1 //false
```

and `<`, `<=`, `>`, `>=`:

```go
var num = 1
num > 1 //false
num >= 1 //true
num < 1 //false
num <= 1 //true
```

We have binary (require two arguments) arithmetic operators, like `+`, `-`, `*`, `/`, `%`.

```go
1 + 1 //2
1 - 1 //0
1 * 2 //2
2 / 2 //1
2 % 2 //0
```

`+` can also join strings:

```go
"a" + "b" //"ab"
```

We have unary operators `++` and `--` to increment or decrement a number:

```go
var num = 1
num++ // num == 2
num-- // num == 1
```

Note that unlike C or JavaScript we can’t prepend them to a number like `++num`. Also, the operation does not return any value.

We have boolean operators that help us with making decisions based on `true` and `false` values: `&&`, `||` and `!`:

```go
true && true  //true
true && false //false
true || false //true
false || false //false
!true  //false
!false //true
```

Those are the main ones.

## Structs in Go

A **struct** is a _type_ that contains one or more variables. It’s like a collection of variables. We call them _fields_. And they can have different types.

Here’s an example of a struct definition:

```go
type Person struct {
	Name string
	Age int
}
```

Note that I used uppercase names for the fields, otherwise those will be _private_ to the package. And when you pass the struct to a function provided by another package, like the ones we use to work with JSON or database, those fields cannot be accessed.

Once we define a struct we can initialize a variable with that type:

```go
flavio := Person{"Flavio", 39}
```

and we can access the individual fields using the dot syntax:

```go
flavio.Age //39
flavio.Name //"Flavio"
```

You can also initialize a new variable from a struct in this way:

```go
flavio := Person{Age: 39, Name: "Flavio"}
```

This lets you initialize only one field, too:

```go
flavio := Person{Age: 39}
```

or even initialize it without any value:

```go
flavio := Person{}

//or

var flavio Person
```

and set the values later:

```go
flavio.Name = "Flavio"
flavio.Age = 39
```

Structs are useful because you can group unrelated data and pass it around to/from functions, store in a slice, and more.

Once defined, a struct is a type like `int` or `string` and this means you can use it inside other structs, too:

```go
type FullName struct {
	FirstName string
	LastName string
}

type Person struct {
	Name FullName
	Age int
}
```

## Functions in Go

A function is a block of code that’s assigned a name, and contains some instructions.

In the “Hello, World!” example we created a `main` function, which is the entry point of the program.

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}
```

That’s a special function.

Usually we define functions with a custom name:

```go
func doSomething() {

}
```

and then you can call them, like this:

```go
doSomething()
```

A function can accept parameters, and we have to set the type of the parameters like this:

```go
func doSomething(a int, b int) {

}

doSomething(1, 2)
```

`a` and `b` are the names we associate to the parameters internally to the function.

A function can return a value, like this:

```go
func sumTwoNumbers(a int, b int) int {
	return a + b
}

result := sumTwoNumbers(1, 2)
```

Note that we specified the return value _type_.

A function in Go can return more than one value:

```go
func performOperations(a int, b int) (int, int) {
	return a + b, a - b
}

sum, diff := performOperations(1, 2)
```

It’s interesting because many languages only allow one return value.

Any variable defined inside the function is local to the function.

A function can also accept an unlimited number of parameters, and in this case we call it a _variadic function_:

```go
func sumNumbers(numbers ...int) int {
	sum := 0
	for _, number := range numbers {
		sum += number
	}
	return sum
}

total := sumNumbers(1, 2, 3, 4)
```

## Pointers in Go

Go supports pointers.

Suppose you have a variable:

```go
age := 20
```

Using `&age` you get the pointer to the variable, its memory address.

When you have the pointer to the variable, you can get the value it points to by using the `*` operator:

```go
age := 20
ageptr = &age
agevalue = *ageptr
```

This is useful when you want to call a function and pass the variable as a parameter. Go by default copies the value of the variable inside the function, so this will not change the value of `age`:

```go
func increment(a int) {
	a = a + 1
}

func main() {
	age := 20
	increment(age)

	//age is still 20
}
```

You can use pointers for this:

```go
func increment(a *int) {
	*a = *a + 1
}

func main() {
	age := 20
	increment(&age)

	//age is now 21
}
```

## Methods in Go

You can assign a function to a struct, and in this case we call it a _method_.

Example:

```go
type Person struct {
	Name string
	Age int
}

func (p Person) Speak() {
	fmt.Println("Hello from " + p.Name)
}

func main() {
	flavio := Person{Age: 39, Name: "Flavio"}
	flavio.Speak()
}
```

You can declare methods to be pointer receiver or value receiver.

The above example shows a value receiver. It receives a copy of the struct instance.

This would be a pointer receiver that receives the pointer to the struct instance:

```go
func (p *Person) Speak() {
	fmt.Println("Hello from " + p.Name)
}
```

## Interfaces in Go

An interface is a _type_ that defines one or more _method signatures_.

Methods are not implemented, just their signature: the name, parameter types and return value type.

Something like this:

```go
type Speaker interface {
	Speak()
}
```

Now you could have a function accept any type that implements all the methods defined by the interface:

```go
func SaySomething(s Speaker) {
	s.Speak()
}
```

And we can pass it any struct that implements those methods:

```go
type Speaker interface {
	Speak()
}

type Person struct {
	Name string
	Age int
}

func (p Person) Speak() {
	fmt.Println("Hello from " + p.Name)
}

func SaySomething(s Speaker) {
	s.Speak()
}

func main() {
	flavio := Person{Age: 39, Name: "Flavio"}
	SaySomething(flavio)
}
```

## Where to Go from Here

This handbook is an introduction to the Go programming language.

Beside these basics, there are many things to learn now.

Garbage collection, error handling, concurrency and networking, the filesystem APIs, and much more.

The sky is the limit.

My suggestion is to pick a program you want to build and just start, learning the things you need along the way.

It will be fun and rewarding.

Note: [you can get a PDF and ePub version of this Go Beginner's Handbook here](https://thevalleyofcode.com/download/go/).