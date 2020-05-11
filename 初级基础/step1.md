# 快速实现 hello word --- 小学篇 #

### 开始上手之前我们先把ts环境搞定：

> 以下命令会在全局环境下安装 tsc 命令，安装完成之后，我们就可以在任何地方执行 tsc 命令

> 安装ts依赖
``` bash
$ npm install -g typescript
```


### 首先我们从一个简单的🌰开始

>上面安装好ts环境后，我们就可以开始上手写了，但不如何下手，那么我们就新建一个文件夹命名为tsdemo，此文件夹下创建一个hello.ts文件，这个时候我们可以在里面任意发挥ts的语法各种高级的操作命名了

> 例如

``` bash
function sayHello(person: string) {
    return 'Hello, ' + person;
}
let user = 'word';
console.log(sayHello(user)) // Hello, word

```

> 执行下面命令即可生成hello.js

```bash
$ tsc hello.ts
```
> 但是这个时候写完了，如何验证自己的语法是否正确，或者如何看到我的console的值呢？接下来我们需要执行下如下命令：

> 执行以下操作创建package.json文件

```bash
 $ npm init

```
> 接下来修改配置文件
> 修改的内容  ("tsc":"tsc --watch")

```bash
 {
  "name": "tsdemo",
  "version": "1.0.0",
  "description": "",
  "main": "hello.js",
  "scripts": {
      "tsc":"tsc --watch",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```
> 再执行以下操作创建ts的配置文件

```bash
 $ tsc --init
```
> 以下命名启动服务，即可完成初步的ts转换js以及验证你当前写的ts文件是否有语法错误等等
```bash
 $ npm run tscs
```
> 现在呢还是看不到我consolelog的内容，接下来就要操作如何看到我的这个log的值，首先再切换一个控制台到当前项目目录下。

> 以下执行当前命令 控制台显示当前打印log的值
``` bash
  $ node hello
```

> 为了不用每次更改都要重启服务实现我们的操作实时更新，首先安装服务

```bash
$ npm install nodemon -g
```

  > 接下来修改配置文件
  > 修改的内容  ("dev": "nodemon ./hello.js")

``` bash
{
"name": "tsdemo",
"version": "1.0.0",
"description": "",
"main": "hello.js",
"scripts": {
    "dev": "nodemon ./hello.js",
    "tsc":"tsc --watch",
    "test": "echo \"Error: no test specified\" && exit 1"
},
"author": "",
"license": "ISC"
}

```


> 以下命令就可以试试看到自己更改的值

``` bash
$ npm run dev

```



> 小学一年级的课文内容结束.


![](https://oscimg.oschina.net/oscnet/fb36dcf3719ec8d53e1d57368b3c83d972d.jpg)