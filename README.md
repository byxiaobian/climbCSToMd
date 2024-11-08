# 🔥climbCSToMd-1.0深度转化🔥
## ✨️将CSDN , 简书文章深度爬取转化为Markdown文档✨️
`原理`:
- 🚀使用`jsoup`解析csdn以及简书文档,配合`flexmark`深度转换,支持大多数的Markdown语法,能够快速解析和渲染大型Markdown文档,可支持表格,脚注,自定义节点,任务列表,代码块等一些复杂的转换..........

`使用`:

- 🚀直接将CSDN以及简书文章的URL传入即可

- 🚀支持URL批量爬取 , 自定义摘要信息批量爬取,

- 🚀支持图片自动转换[目前只支持阿里云OSS]

  

> **因脚本插件是java编写 所以需要有Java环境 JDK版本需求1.8**
>
> 需要注意: 路径末尾不要跟路径符号,文章的命名自动命名为文章标题.md



## 例如：

### 🎯获取单个文章爬取转markdown
```java
命令: 
java -jar -u[文章URL] -m[平台类型] -s[保存路径]   //平台类型 1是csdn 2是简书
示例:
java -jar -u https://blog.csdn.net/weixin_66461496/article/details/143449370 -m 1 -s E:\temp\markdown
```
### 🎯获取指定文件里的URL批量爬取转markdown
```java
命令:
java -jar -m[平台类型] -s[保存路径] -f[文件URL路径]
示例:
java -jar -m 1 -s E:\temp\markdown -f E:\temp\markdown\urls.txt

```
### 🎯自定义摘要信息批量爬取转markdown

> 在软件目录下有一个文件 `config.json` 里 , 按照JSON格式填写即可,填写完后执行命令.

```
命令:
java -jar -m[平台类型] -s[保存路径] -j
示例:
java -jar -m 1 -s \temp\markdown -j
```

![](https://soobsj.oss-cn-hangzhou.aliyuncs.com/images/202411082359732.png)

### 🎯图床采用阿里云OSS 配置

> 在软件当前目录下 有一个 tc.conf 的文件 , 里面填写相对应的OSS信息即可 , enabled为开启关闭状态 !



![](https://soobsj.oss-cn-hangzhou.aliyuncs.com/images/202411090009293.png)
