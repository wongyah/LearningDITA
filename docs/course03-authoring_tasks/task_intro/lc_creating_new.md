# 新建任务型主题

一个最简单的任务型主题，至少要包含一个根元素 `<task>`（带 `id` 属性），`<task>` 元素中至少要包含一个 `<title>` 元素。

在 `<title>` 元素的后面，可以插入一个 `<shortdesc>` 元素或 `<abstract>` 元素，然后才是用来添加正文内容的 `<taskbody>` 元素。`<taskbody>` 元素中的内容需要按照特定的顺序排列。本节课将按照出现顺序逐个介绍 `<taskbody>` 中的各个元素。

<!-- [视频：创建任务型主题](https://youtu.be/7E7RYKHQ6C4) -->

## 随堂练习

1. 为文件 `l_task_start.dita` 创建一个副本，然后在编辑器中打开。
   
    !!! note "注意"
        如果你使用的是支持 DITA 的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。
   
    你看到的文件内容应该是这样的：

    - 第一行（以 `<?xml` 开头）是XML声明。XML声明是XML文件的一个标准组成部分。
    - 第二行是文档类型声明（即DOCTYPE声明），用来声明该文件是一个严格任务主题。对主题内容进行验证时，程序会用到该信息。每个主题类型的文档类型（即DOCTYPE）都各不相同，包括通用任务主题。
    - 第三行是 `<task>` 元素的开始标签，还带有一个属性值为 `my_first_task` 的 `id` 属性。
    - 第四行是 `<title>` 元素，其内容是该主题的标题。

2. 在 `<title>` 元素中，编辑标题文本如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Task//EN" "task.dtd">
    <task id="my_first_task">
      <title>观看野鸭</title>
    </task>
    ```

3. 在 `<title>` 元素的后面，插入一个 `<taskbody>` 元素。

    !!! note "注意"
        任务型主题的正文内容将全部添加到 `<taskbody>` 元素中。

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Task//EN" "task.dtd">
    <task id="my_first_task">
      <title>观看野鸭</title>
      <taskbody> </taskbody>
    </task>
    ```

    这是严格任务主题的主体。接下来，本讲将教你如何在 `<taskbody>` 元素中插入头两个子元素。