# 如何使用元数据?

在 DITA 中，你可以在很多地方设置元数据：

- 主题上
- 元素上
- 导图上（导图可以将多个主题组织在一起，生成文档或帮助系统等。《使用DITA导图和书籍导图》一课将对此进行详细讲解。）

如果要为整个主题添加元数据，使用 `<prolog>` 元素。这是一个关于主题元数据的简单示例：

```xml
<topic id="xyz">
    <title>元数据示例</title>
    <prolog> 
        <author>王烨，技术传播百态说</author> 
        <critdates> 
            <created date="2025-08-15"/> 
        </critdates> 
    </prolog>
    <body> 
        <p>将正文写在这里</p> 
    </body> 
</topic>
```

作者信息写在 `<author>` 元素中，关键日期写在 `<critdates>` 元素中。`<critdates>` 元素有两个子元素：`<created>`  元素里写创建日期，`<revised>` 元素里写修改日期。

`<prolog>` 元素中的常用子元素有：

`<author>`
: 写作人员或作者

`<critdates>`
: 关键日期，比如创建日期（`<created>`）和修改日期（`<revised>`）

`<copyright>`
: 版权信息，比如版权年份（`<copyryear>`）和版权所有者（`<copyrholder>`）

`<vrm>`
: 产品的版本信息

!!! important "重要"
    `<prolog>` 元素只能为整个主题提供元数据，例如作者、创建日期和修订日期。在DITA中，`<prolog>`元素中的元数据不会用来筛选主题。

如果要为元素添加元数据，通常使用元素属性。这是一个示例：

```xml
<step>
    <cmd>寻找小鸭子的饲料盒。</cmd>
    <info audience="novice">找到后，目测小鸭子的饲料盒里能装多少饲料。</info>
</step>
<step>
    <cmd>量出小鸭子所需的饲料。</cmd>
</step>
<step>
    <cmd>将饲料倒入搅拌机中。</cmd>
</step>
<step>
    <cmd>将搅拌好的饲料倒入饲料盒的料盘中。</cmd>
</step>
```

新手可能不知道饲料盒上有计量功能，需要特意提醒一下。如果是给老用户看的文档，你在生成文档时就可以跳过带有 `audience="novice"` 属性的 `<info>` 元素。

你也可以在导图中为某个主题添加元数据，比如在引用该主题的 `<topicref>` 元素上添加属性。这样，你就可以在生成文档时跳过某个主题。这是一个示例：

```xml
<topicref href="abc.dita">
<topicref href="def.dita" audience="novice">
```

在 DITA 中，可以用来对内容进行筛选或条件处理的属性有：

- `audience`
- `product`
- `platform`
- `otherprops`
- `deliveryTarget`

如果需要其他属性，你可以让信息架构师利用DITA定制功能自行定义。下面是一些常见的定制属性：

`customer`
: 客户信息

`region`
: 地区或区域等地理信息。

`product-family`
: 产品所属的系列等信息。
