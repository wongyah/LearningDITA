# 添加行内样式

DITA使用行内元素为段落中的文本片段添加行内样式：

| 元素 | 说明 |
|---|---|
| `<b>` | 粗体 |
| `<i>` | 斜体 |
| `<u>` | 带下划线的文本 |
| `<term>` | 术语（需要提供定义的词汇或短语） |
| `<cite>` | 引用的词汇或短语 |
| `<varname>` | 变量名称（根据用户语境的变化而变化的词汇或短语） |
| `<sub>` | 下标 |
| `<sup>` | 上标 |

大家比较熟悉行内元素`<b>`、`<i>`和`<u>`，看一眼就会用了。不过，由于它们只强调文本的格式，也很容易用错，从而无法实现内容和格式分离的目的。因此，尽量省着用这些元素。在大多数情况下，最好使用语义更加明确的元素，比如`<term>`、`<cite>`或 `<varname>`元素。

在下面的示例中，你将先学习如何插入`<b>`、`<i>`和`<u>`元素，然后再学习如何将它们替换为语义更加明确的元素。

## 随堂练习

1. 为文件 `lesson3/l_concept_elements_start.dita` 创建一个副本，然后在编辑器中打开。

    !!! note "注意"
        如果你使用的是支持DITA的编辑器，请使用文本模式，不要使用写作模式或者其他可视模式。

    你看到的文件内容应该是这样的：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
     </conbody>
    </concept>
    ```

2. 插入一个`<p>`元素（其中包含`<b>`、`<i>`和`<u>`元素），如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      <p>鸭子出生后的头<u>两个星期</u>，每天<b>24小时</b>随时需要<i>进食</i>和<i>喝水</i>。</p>
     </conbody>
    </concept>
    ```

    在段落中添加了`<b>`元素，相当于标明"24小时"的格式应该是粗体。同理，在段落中添加了`<i>`元素，相当于标明"进食"和"喝水"的格式应该是斜体；在段落中添加了`<u>`元素，相当于标明"两个星期"的格式应该下划线文本。

    这些行内元素虽然可以强调重要的词汇，但它们没有任何语义。假设你想以后再给"24小时"添加定义，或者为所有表示进食频率的词汇统一设置格式。你与其使用`<b>`元素将这些词语简单地标记为粗体，倒不如使用`<term>`元素将它们标记为重要的术语。

    在下一步中你将会看到，有不少功能相似但语义更加丰富的元素可以替代`<i>`和`<u>`元素。

3. 在`<p>`元素的后面，再插入一个`<p>`元素。新`<p>`元素的内容和上一个`<p>`元素相同，只是将`<b>`元素换成了`<term>`元素，将`<i>`元素换成了`<cite>`元素，将`<u>`元素换成了`<varname>`元素，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      <p>鸭子出生后的头<varname>两个星期</varname>，每天<term>24小时</term>随时需要<cite>进食</cite>和<cite>喝水</cite>。</p>
     </conbody>
    </concept>
    ```

    在本例中，你使用`<varname>`元素标记了"两个星期"，表示这个时间值可以根据用户的实际情况加以调整（例如，某些品种的鸭子（在出生后）需要随时进食和喝水的阶段可能不只两个星期。你使用`<term>`元素标记了"24小时"，表示这是一个待定义的术语。最后，你使用`<cite>`元素标记了"进食"和"喝水"，表示这两个词汇可以根据需要予以引注。

4. 在最后一个`<p>`元素的后面，再插入一个`<p>`元素。新的`<p>`元素中包含一个`<sub>`元素，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给小鸭子喂食</title>
     <conbody>
      <p>由于鸭子饲料又干又硬，小鸭子需要充足的水（H<sub>2</sub>O）来保持喙部清洁。</p>
     </conbody>
    </concept>
    ```

    `<sub>`元素是用来标记下标或者比正常文本字体小、位置偏低的文本的。在本例中，`<sub>`元素用来标记"H<sub>2</sub>O"中的"2"，让它显示为下标。

5. 在最后一个`<p>`元素的后面，再插入一个`<p>`元素。新的`<p>`元素中包含一个`<sup>`元素，如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
    <concept id="concept_elements">
     <title>给鸭子喂食</title>
     <conbody>
      <p>你可以用回收的塑料容器自制矮矮的、防溢出的喂食器，也可以从 E-Z-Feed<sup>2</sup> 购买现成的产品。</p>
     </conbody>
    </concept>
    ```

    `<sub>`元素是用来标记上标或者比正常文本字号小、位置偏高的文本的。在本例中，`<sub>`元素用来标记鸭子饲料公司的公司名称（"E-Z-Feed^2^"）中的"2"，让它显示为上标。

    !!! note "注意"
        切勿使用`<sup>`元素创建脚注编号。虽然脚注编号的字号和位置看上去与上标差不多，但创建脚注应该使用`<fn>`元素，这一点会在后面的课程中会细讲。
