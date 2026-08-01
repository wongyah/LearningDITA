# 使用领域元素

DITA 专门定义了一些元素，用来编写编程语言、计算机软件和用户界面等方面的主题。这些元素叫做领域定制元素。

领域定制元素是从现有元素定制而来，可以用在所有定制的主题类型中，比如概念型主题、任务型主题和参考型主题。不过，参考型主题中用得最多。

编写参考型主题时，推荐使用语义明确的领域元素，理由如下：

- 其他写作人员可以了解与内容有关的附加信息。
- 便于进行多维搜索，比如查找文件名中包含产品名称"X"的文件。
- 文档发布程序可以使这些内容以特定格式显示，引起读者注意。

以下是一些常用的领域元素：

编程领域
: `<apiname>`、`<codeblock>`、`<codeph>`（code phrase，即行内代码）、`<option>`、`<parml>`（parameter list，即参数列表）、`<synph>`（syntax phrase，即语法短语）

软件领域
: `<cmdname>`（command name，即命令名称）、`<filepath>`、`<varname>`（variable name，即变量名称）、`<userinput>`、`<systemoutput>`

用户界面
: `<uicontrol>`（user interface control，即界面元件)、`<menucascade>`、`<wintitle>`（window title，即视窗标题)、`<screen>`

其中，使用频率最高的两个界面元素是：`<uicontrol>` 和 `<menucascade>`。`<uicontrol>` 元素可以用来标记用户界面上的按钮或者菜单项。如果要标记级联菜单，使用 `<menucascade>` 元素，该元素中可以添加多个 `<uicontrol>` 元素。

```xml
……选择<menucascade><uicontrol>文件</uicontrol><uicontrol>打开</uicontrol></menucascade>。
```

文档发布程序会在两个菜单项之间插入合适的字符。这样，所有级联菜单都会使用相同的分隔符，以统一的格式显示。

```
…… 选择「文件」>「打开」
```

如果你想深入了解领域元素，请参见[《OASIS DITA 1.3 规范》](https://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/containers/technicalContent-domain-elements.html#technicalContent-domain-elements)

另外，强烈建议将领域元素的具体用法写进写作指南中。
