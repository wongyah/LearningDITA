# 插入其他元素

在DITA中，还有很多元素也很重要。这儿就有三个：

| 元素 | 说明 |
|---|---|
| `<fn>` | 脚注 |
| `<menucascade>` | 级联菜单，比如【文件】>【另存为】。一个`<menucascade>`元素中必须包含一个或多个`<uicontrol>`元素。一个`<uicontrol>`元素中包含一个菜单项。 |
| `<dl>` | 定义列表。定义列表是一系列术语及其定义的列表。定义列表的默认格式与两列的表格差不多。定义列表包含一个或多个条目。每个条目使用一个`<dlentry>`元素标记，里面包含一个术语（使用`<dt>`元素标记）和一个或多个定义（使用`<dd>`元素标记）。 |

## 随堂练习

请继续使用文件 `lesson3/l_concept_elements_start.dita` 练习，将上面提到的元素插入到文件中。

1. 在最后一个 `<p>` 元素的后面，再插入一个 `<p>` 元素。新的 `<p>` 元素中包含一个 `<fn>` 元素，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      <p>小鸭子饮食中需要的蛋白质含量比成年鸭要高。<fn>对于刚出生的小鸭子，推荐饮食中的蛋白质含量为18-20%。</fn></p>
     </conbody>
    </concept>
    ```

    `<fn>` 元素标明了脚注编号在正文中的位置。默认情况下，当你将DITA文件发布为可视格式时，`<fn>` 元素中的文本显示在页面底部（PDF文件）或者主题的末尾（HTML页面）。

2. 在最后一个 `<p>` 元素的后面，再插入一个 `<p>` 元素。新的 `<p>` 元素中包含一个 `<menucascade>` 元素，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      <p>你可以使用电子表格来记录你需要为小鸭子补充鸭粮和水的时间，点击<menucascade> </menucascade>。</p>
     </conbody>
    </concept>
    ```

    在本例中，`<menucascade>` 元素用来说明新建电子表格需要使用的菜单项。

3. 在 `<menucascade>` 元素中，插入一个 `<uicontrol>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      <menucascade>
       <uicontrol>文件</uicontrol>
      </menucascade>
      ...
     </conbody>
    </concept>
    ```

    在本例中，`<uicontrol>` 元素中的内容是新建电子表格时需要使用的第一个菜单项的名称："文件"。

4. 在 `<uicontrol>` 元素的后面，再插入两个 `<uicontrol>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      <menucascade>
       <uicontrol>文件</uicontrol>
       <uicontrol>新建</uicontrol>
       <uicontrol>电子表格</uicontrol>
      </menucascade>
      ...
     </conbody>
    </concept>
    ```

    在默认情况下，发布为可视文档时，两个 `<uicontrol>` 元素之间会插入一个箭头，以表示菜单项之间的层级关系。

    在本例中，通过 `<menucascade>` 和 `<uicontrol>` 元素，用户就知道先点【文件】，再点【新建】，然后再点【电子表格】了。

    `<uicontrol>` 也可以单独使用，不是非和要 `<menucascade>` 一起用。例如，你可以使用 `<uicontrol>` 元素标记一个词汇，以表示这个词汇是用户应该点击的按钮名称。由于 `<uicontrol>` 元素中的内容会以特殊格式显示，所以没必要在 `<uicontrol>` 元素中再使用 `<b>` 元素或者其他行内元素。

5. 在 `<menucascade>` 元素的后面，依次插入一个 `<p>` 元素和一个 `<dl>` 元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      </menucascade>
      <p>家鸭可以根据体重分为不同的等级。有了这些体重等级，你就可以基于鸭子的食量来选择鸭子品种。</p>
      <dl>
      </dl>
     </conbody>
    </concept>
    ```

    `<dl>` 元素可以为定义列表建立内容框架。

6. 在 `<dl>` 元素中，插入一个 `<dlentry>` 元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      <dl>
       <dlentry>
       </dlentry>
      ...
     </conbody>
    </concept>
    ```

    每个 `<dlentry>` 元素中都有一个术语和它的定义。一个 `<dlentry>` 元素中可以有一个或多个 `<dd>` 元素。

7. 在 `<dl>` 元素中，插入一个 `<dt>` 元素和一个 `<dd>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      <dlentry>
       <dt>矮脚鸭</dt>
       <dd>体重最轻、飞行能力最强的鸭子，比如绿头鸭。</dd>
      ...
     </conbody>
    </concept>
    ```

    `<dt>` 元素中的内容是术语，`<dd>` 元素中的内容是术语的定义。

8. 在 `<dlentry>` 元素的后面，再插入三个 `<dlentry>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      ...
      </dlentry>
      <dlentry>
       <dt>轻型鸭</dt>
       <dd>体重第二轻、产蛋最好的鸭种，比如卡基·康贝尔鸭。</dd>
      </dlentry>
      <dlentry>
       <dt>中型鸭</dt>
       <dd>体重中等、性情通常最温顺的鸭种，比如瑞典鸭。</dd>
      </dlentry>
      <dlentry>
       <dt>重型鸭</dt>
       <dd>体重最重、性情通常最友善的鸭种，比如北京鸭。</dd>
      </dlentry>
      ...
     </conbody>
    </concept>
    ```

9. 对照[随堂练习的参考答案] (`lesson3/l_concept_elements.dita`)，自行批改一下你刚刚完成的练习作业 (`lesson3/l_concept_elements_start.dita`)。

## 课后练习

1. 打开文件 `lesson3/l_concept_elements_exercise_start.dita`，使用该文件将以下内容转换成DITA：

    --8<-- "div_exercise_content.md:start"
    
    <h2 style="margin: .64em 0 .64em;">提升产品的关注度</h2>
    
    技术内容能够帮助组织提升其产品在市场中的关注度。 理论上说，技术内容的目标受众是**产品的客户**，即那些购买产品后查阅产品文档的人。
    
    然而一项民意调查显示，大约有三分之一的客户[^1]会在购买产品前先看文档，而文档的质量会影响他们的购买决策。

    [^1]: 《客户对产品文档的看法》，由莎伦·伯顿开展的一项在线民意调查。
    
    要吸引潜在客户，技术内容必须做到以下三点： 可搜索、易查找、易发现。
    
    **可搜索**
    客户可以通过网络搜索找到您的内容。
    
    **易查找**
    客户可以通过相关关键词快速检索到您的内容。
    
    **易发现**
    您的内容能让人们主动链接或引用。
    
    想要阅读更多内容，请前往**目录** > **商业目标** > **营销与产品关注度** > **提升产品的关注度**.
    
    ///Footnotes Go Here///

    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`lesson3/l_concept_elements_exercise.dita`)，自行批改一下你刚刚完成的练习作业 (`lesson3/l_concept_elements_exercise_start.dita`)。


[随堂练习的参考答案]: sa_concept_elements.md#_2
[课后练习的参考答案]: sa_concept_elements.md#_3
