# 在文本编辑器中创建主题

DITA 文件是 XML 文件的一种，而 XML 文件是纯文本文件。因此，你可以在任何一个文本编辑器中编辑 XML 文件。

在 DITA 中，一条 XML 声明、一条文档类型声明、一个包含标题和 id 属性的主题元素就能组成一个最简单的主题了。仅此而已！

下面是一个简单又合法的主题：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD DITA Topic//EN" "topic.dtd"> 
<topic id="my-first-topic"> 
    <title>你好，世界！</title> 
</topic> 
```

这个主题虽然合法，但没什么实际用处，因为它的正文中没有任何内容。要让主题变得有用一点，你得添加一些这样的内容：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD DITA Topic//EN" "topic.dtd">
<topic id="my-first-topic">
    <title>你好，世界！</title>
    <body>
        <p>在这里写一个段落</p>
        <ul>
            <li>有序列表很好用</li>
            <li>尤其是列表项不少于两个的时候</li>
        </ul>
        <note>还有，别忘了写个注释！</note>
    </body>
</topic>
```