# CALS 表格

在 DITA 中，CALS 表格（`<table>`）的后代元素如下：

`<title>`
: 表格标题。每个 CALS 表格最多只能有一个表格标题。

`<tgroup>`
: 表格组。每个 CALS 表格中至少要有一个表格组。表格组可以包含列参数、标题行和表格主体。

`<colspec>`
: 列参数。CALS 表格中的每一列都可以设置一组列参数。

`<thead>`
: 标题行。每个表格组中最多只能有一个标题行。

`<tbody>`
: 表格主体。每个表格组中必须有且只能有一个表格主体。

`<row>`
: 表格行。每个标题行或表格主体中，可以有任意数量的表格行。

`<entry>`
: 单元格。每个表格行中至少要有一个单元格，也可以有多个单元格。

在 CALS 表格的单元格中，既可以添加文本，也可以插入常用的块元素和行内元素。

下面是一个 CALS 表格示例。示例表格中有一个标题行、一个表格行，每行都分成了三列。在本例中，`<tgroup>` 元素中只设置了一个属性：`cols` 属性。`cols` 属性可以用来设置 CALS 表格中的列数，是 `tgroup` 元素的唯一必选属性。

```xml
<table>
  <tgroup cols="3">
    <thead>
      <row>
        <entry>标题行，第一列</entry>
        <entry>标题行，第二列</entry>
        <entry>标题行，第三列</entry>
      </row>
    </thead>
    <tbody>
      <row>
        <entry>表格行，第一列</entry>
        <entry>表格行，第二列</entry>
        <entry>表格行，第三列</entry>
      </row>
  </tbody>
  </tgroup>
</table>
```

上面的表格会显示如下：

--8<-- "sample_snippet.md:start"
| 标题行，第一列 | 标题行，第二列 | 标题行，第三列 |
|---------------|---------------|---------------|
| 表格行，第一列 | 表格行，第二列 | 表格行，第三列 |
--8<-- "sample_snippet.md:end"

下面是一个复杂一点的表格：

```xml
<table>
  <title>我的第一个表格</title>
  <tgroup cols="2">
    <colspec colname="c1" colnum="1" colwidth="1*"/>
    <colspec colname="c2" colnum="2" colwidth="4*"/>
    <thead>
      <row>
          <entry>标题行，第一列</entry>
          <entry>标题行，第二列</entry>
      </row>
    </thead>
    <tbody>
      <row>
        <entry>第一行，第一列</entry>
        <entry>第一行，第二列</entry>
      </row>
      <row>
        <entry namest="c1" nameend="c2">这是一个横跨两列的合并单元格</entry>
      </row>
      <row>
        <entry morerows="1">这是一个纵跨两行的合并单元格</entry>
        <entry>第三行，第二列</entry>
      </row>
      <row>
        <entry>第四行，第二列</entry>
      </row>
    </tbody>
  </tgroup>
</table>
```

上面的表格会显示如下：

--8<-- "sample_snippet.md:start"
<table border="1">
  <tr>
    <th>标题行，第一列</th>
    <th>标题行，第二列</th>
  </tr>
  <tr>
    <td>第一行，第一列</td>
    <td>第一行，第二列</td>
  </tr>
  <tr>
    <td colspan="2">这是一个横跨两列的合并单元格</td>
  </tr>
  <tr>
    <td rowspan="2">这是一个纵跨两行的合并单元格</td>
    <td>第三行，第二列</td>
  </tr>
  <tr>
    <td>第四行，第二列</td>
  </tr>
</table>
--8<-- "sample_snippet.md:end"

使用 CALS 表格时，请注意以下事项：

- 在 `<colspec>` 元素中，使用属性为表格列设置列名（`colname`）、列号（`colnum`）和列宽（`colwidth`）。在本例中，第一列的列宽属性值是“[1*](file://e:\my_repos\public\learningDITA\DITA-1.3\zh-cn\course01-intro\tables\lc_table_simple.dita)”，第二列的列宽属性值是 `4*`。列宽属性值中的星号表示，这里的列宽设置是比例值。也就是说，本例中两个表格列的列宽比例是 1:4，即第一列的列宽是整个表格宽度的 20%，第二列的列宽是整个表格宽度的 80%。
- CALS 表格中的每一行都使用一个 `<row>` 元素。在 `<row>` 元素中有若干个 `<entry>` 元素，每个 `<entry>` 元素都是一个单元格。
- 在第二行中，只有一个横跨两列的合并单元格。单元格的起始列是 `namest` 属性的属性值“c1”（即第一列），单元格的结束列是 `nameend` 属性的属性值“c2”（即第二列）。
- 在第三行中，第一个单元格是一个纵跨两行的合并单元格。单元格的起始行是当前行，单元格是结束行是当前行的行数与 `morerows` 属性的属性值之和（即第四列）。

在 DITA 中插入表格，最好还是使用可视化编辑器。可视化编辑器通常会自动设置表格属性，用起来比较省心。如果使用文本编辑器手搓表格代码，你得有颗大心脏才行！
