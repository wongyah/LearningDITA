# 插入简单表格

概念型主题中，有两个元素可以用来创建表格：`<simpletable>`和`<table>`。

无论什么时候，都尽量使用`<simpletable>`元素，尤其是简短的表格。如果是大型表格或者格式特别复杂的表格，就使用`<table>`元素。

`<simpletable>`元素中的常用元素有：

| 元素 | 说明 |
|------|------|
| `<sthead>` | 简单表格中的标题行。`<sthead>`元素中可以包含一个或多个`<stentry>`元素。一个`<simpletable>`元素中最多只能有一个`<sthead>`元素。 |
| `<strow>` | 简单表格中的数据行。`<strow>`元素中可以包含任意数量的`<stentry>`元素。一个`<simpletable>`元素中可以有一个或多个`<strow>`元素。 |
| `<stentry>` | 简单表格中的单元格。在`<simpletable>`元素中，`<stentry>`元素是用来盛放单元格内容的。根据最佳实践，单元格中的文本应该放在`<p>`元素中。 |

本讲的主要内容是`<simpletable>`元素的基本用法。

![示例：简单表格的可视格式](../media/images_and_tables/simpletable.png)

## 随堂练习

请继续使用文件`lesson2/l_concept_images_tables_start.dita`进行练习，将`<simpletable>`元素插入到文件中。

!!! note "注意"
    如果你使用的是支持DITA的编辑器，当你按照示例练习时，编辑器可能会在`<simpletable>`元素中自动插入一些子元素。

1. 在`<conbody>`元素中，`<fig>`元素后面，插入一个`<simpletable>`元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      </fig>
      <simpletable>
      </simpletable>
     </conbody>
    </concept>
    ```

2. 在`<simpletable>`元素中，插入一个`<sthead>`元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      <simpletable>
       <sthead>
       </sthead>
      </simpletable>
     </conbody>
    </concept>
    ```
    
    `<sthead>`元素为简单表格创建了一个标题行。

3. 在`<sthead>`元素中，插入两个`<stentry>`元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      <sthead>
       <stentry><p>鸭龄</p></stentry>
       <stentry><p>重要时刻</p></stentry>
      </sthead>
      ...
     </conbody>
    </concept>
    ```
    
    每个`<stentry>`元素都代表一个单元格。`<sthead>`元素中有多少个`<stentry>`元素，就代表简单表格里有多少列。
    
    刚刚添加的每个`<stentry>`元素，按照最佳实践，里面的文本都放在了`<p>`元素里。

4. 在`<sthead>`元素的后面，插入一个`<strow>`元素如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      </sthead>
      <strow>
      </strow>
      ...
     </conbody>
    </concept>
    ```
    
    `<strow>`元素为简单表格创建数据行，数据行位于标题行之后并且紧跟标题行。

5. 在`<strow>`元素中，插入两个`<stentry>`元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      <strow>
       <stentry><p>7 周</p></stentry>
       <stentry><p>第一次尝试飞起来</p></stentry>
      </strow>
      ...
     </conbody>
    </concept>
    ```
    
    `<sthead>`元素和每一个`<strow>`元素都应该有相同数量的`<stentry>`元素。

6. 在第一个`<strow>`元素的后面，插入两个数据行，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_images_tables">
     <title>小鸭子的生长发育</title>
     <conbody>
      ...
      </strow>
      <strow>
       <stentry><p>12-14 周</p></stentry>
       <stentry><p>体重达到成年鸭子的水平</p></stentry>
      </strow>
      <strow>
       <stentry><p>1 年</p></stentry>
       <stentry><p>具有繁殖能力</p></stentry>
      </strow>
      ...
     </conbody>
    </concept>
    ```
    
    在一个`<simpletable>`元素中，可以插入一个或多个`<strow>`元素。
