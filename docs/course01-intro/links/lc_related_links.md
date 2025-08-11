# 相关链接

在主题的末尾，你可以插入一个相关链接（`<related-links>`）。相关链接主要用来提供一些可能对读者有用的额外信息。

相关链接中包含链接和链接文本。下面是一个示例：

```xml
<topic id="sample">
    <title>示例标题</title>
    <body> ... </body>
    <related-links>
        <link href="https://www.example.com" format="html" scope="external">
            <linktext>示例链接</linktext>
        </link>
    </related-links>
</topic>
```

在 `<link>` 元素中，你可以使用 `href` 属性设置链接目标，还可以使用 `format` 属性和 `scope` 属性声明链接目标的格式和来源。如果链接目标是网页或者不在当前导图中的文件，`scope` 属性的属性值应设置为 `external`。

除此之外，你还可以使用 `<linktext>` 元素设置链接文本。

!!! note "注意" 
    在导图中创建指向内部主题的链接时，尽量不要使用相关链接。相关链接与交叉引用一样，也属于内联链接。如果源主题和目标主题不在同一个导图中，链接就会失效，而且不会有任何错误报告。如果可以，最好还是使用关系表创建链接。