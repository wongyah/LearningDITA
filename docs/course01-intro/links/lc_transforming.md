# 文档转换

一般情况下，文档不会使用 DITA 文件作为交付格式。你需要为 DITA 文件设置样式表，并将其转换成 HTML、PDF 或其他格式的文件。这个过程叫做转换。

``` mermaid
flowchart LR
  A@{ shape: docs, label: "topicref"} -- 转换 --> B@{ shape: doc, label: "PDF"}
  A@{ shape: docs, label: "topicref"} -- 转换 --> C@{ shape: doc, label: "HTML"}
  subgraph DITA导图
  A
  end
  subgraph 输出文件
  B
  C
  end
```

DITA 开放工具包 (DITA-OT) 是用扩展样式表语言 (XSL) 编写的样式表库。你可以将 DITA-OT 当作文档发布的起点。默认情况下，使用 DITA-OT 生成的文档是出名的难看。真正生成文档时，大家通常都会对文档转换过程进行优化。

!!! tip "小贴士"
    DITA-OT 并不是唯一一个能将 DITA 文件转换成文档的发布工具。你也可以使用商用软件发布文档。有些软件既能编辑 DITA 文件，也能进行文档转换。有些软件没有内容编辑功能，只有文档转换功能。

文档转换和导图是各自独立、互不依赖的两个文件。对于同一个导图，你可以使用多个文档转换程序将其发布成多种格式的文档。例如，你可以使用 PDF 转换程序将一个导图发布成 PDF 文档，也可以使用在线帮助转换程序将这个导图发布成在线帮助文档。

## 相关链接

- [DITA-OT](https://www.dita-ot.org)
- 网络研讨会：[DITA-OT 入门](https://www.youtube.com/watch?v=xFPRnJrRo8o)（视频，53分钟）

<!-- abbr -->
*[DITA-OT]: DITA Open Toolkit
*[XSL]: EXtensible Stylesheet Language