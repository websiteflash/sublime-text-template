我本来打算写一个sublime的插件，用来在code的时候插入一些固定的代码，比如一些声明或者是代码片段，但是当我学习编写sublime插件的过程中发现，原来sublime提供了一个很好的工具可以让我直接实现这一目标。

通过 Tools->New Snippet ，会创建一个snippet的模版:

```
<snippet>
  <content><![CDATA[
Hello, ${1:this} is a ${2:snippet}.
Write anything you want here.
]]></content>
  <!-- 设置响应的字符，比如这里设置为hello，那么当我们在敲入hello时，sublime就会出现自动提示框 -->
  <tabTrigger>hello</tabTrigger>
  <!-- 指定配置的文件类型，如果是js文件的话，就是source.js -->
  <scope>source.js</scope>
  <!-- 描述信息, 出现提示时，对该命令的描述 -->
  <description>my snippet demo</description>
</snippet>
```

将这个文件保存到 `Sublime Text\Data\Packages\User` 下，保存的文件，后缀名为 `.sublime-snippet`，比如：`hello.sublime-snippet`

到这里，就完成了。如果要创建更多的模版，只要按上面的步骤创建新的文件就可以。

