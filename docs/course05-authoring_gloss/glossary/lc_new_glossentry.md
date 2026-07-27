# 新建术语词条主题

一个最简单的术语词条主题，至少要包含一个带 `id` 属性的根元素 `<glossentry>`（glossary entry，即术语词条）。`<glossentry>`元素中至少要包含一个 `<glossterm>`（glossary term，即术语）元素。

`<glossterm>`元素是 `<title>` 元素的定制元素。任何可以在 `<title>` 元素中使用的元素，都可以在 `<glossterm>` 元素中使用。

`<glossdef>`元素必须位于 `<glossterm>` 元素的后面，用来给术语下定义。任何可以在 `<section>` 元素中使用的元素，都可以在 `<glossdef>` 元素中使用，除了 `<title>` 元素。

`<glossdef>`元素的后面，可以跟一个 `<glossbody>`（glossary body，即术语正文）元素。`<glossbody>` 元素中可以包含一系列子元素，用来为术语提供更详细的信息。有关 `<glossbody>` 元素的内容，超出了本讲的讨论范围，将在本课的后续部分介绍。

<!-- [视频：创建术语词条主题](https://youtu.be/6JrvPjKwphM) -->

!!! note "注意"
    通常，术语词条的文件名都会加上一个前缀"g_"，方便以后查找。不过在本课程中，为了与其他练习资料的命名保持统一，我们仍然使用"l_"。

## 随堂练习

1. 为文件 `l_glossentry_start.dita` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    你看到的文件内容应该是这样的：

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <!DOCTYPE glossentry PUBLIC "-//OASIS//DTD DITA Glossary//EN" "glossary.dtd">
    <glossentry id="duck">
      <glossterm></glossterm>
    </glossentry>
    ```

    - 第一行（以 `<?xml` 开头）是XML声明。XML声明是XML文件的一个标准组成部分。
    - 第二行是文档类型声明（即DOCTYPE声明），用来声明该文件是一个术语词条主题。对主题内容进行验证时，程序会用到该信息。每个主题类型的文档类型（即DOCTYPE）都各不相同，包括通用任务主题。
    - 第三行是 `<glossentry>` 元素的开始标签。`id` 是 `<glossentry>` 元素的必选属性。
    - 第四行是 `<glossterm>` 元素。

2. 在 `<glossterm>` 元素中，插入需要下定义的术语。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE glossentry PUBLIC "-//OASIS//DTD DITA Glossary//EN" "glossary.dtd">
    <glossentry id="duck">
      <glossterm>鸭子</glossterm>
    </glossentry>
    ```

3. 在 `<glossterm>` 元素的后面，插入一个 `<glossdef>` 元素。

    尽量为 `<glossentry>` 元素的 `id` 属性设置一个语义贴切的属性值，最好切合术语的含义，便于以后引用。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Glossary//EN" "glossary.dtd">
    <glossentry id="duck">
      <glossterm>duck</glossterm>
      <glossdef>
        <p>一种会游泳的鸟类，趾间有蹼，喙宽而扁平，叫起来嘎嘎的。</p>
      </glossdef>
    </glossentry>
    ```

4. 对照[随堂练习的参考答案] (`lesson1/l_glossentry.dita`)，自行批改一下你刚刚完成的练习作业。

<!-- links -->
[随堂练习的参考答案]: sa_glossentry.md#_2
