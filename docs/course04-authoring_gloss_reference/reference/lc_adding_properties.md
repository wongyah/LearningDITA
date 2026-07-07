# 插入属性表

在许多 API 参考文档或命令行参考文档中，语法图的后面都会放上一个列表或表格。在列表或表格中，对各个关键字、占位符和其他选项进行详细说明。语法图用来说明应该在哪里使用这些对象，属性表用来说明为什么要使用这些对象。

例如，在导出图片的命令中，**filetype**参数的参数值可以是 `gif`、`png`、`bmp` 和 `svg`。你需要说明每一种文件类型的具体含义。

在参考型主题中，你可以使用 `<properties>` 元素来编写此类内容。`<properties>` 元素是 `<refbody>` 元素的合法子元素。

一个 `<properties>` 元素中可以包含一个或多个 `<property>` 元素，一个 `<property>` 元素说明一个属性。一个 `<property>` 元素中可以包含三个子元素：`<proptype>`（属性类型）、`<propvalue>`（属性值）和 `<propdesc>`（属性说明）。这些元素的典型应用场景如下：

| 文档类型 | `<proptype>` | `<propvalue>` | `<propdesc>` |
| :--- | :--- | :--- | :--- |
| **命令行的参考文档** | 命令参数 | 参数值或关键字 | 参数说明（参数的含义和用途） |
| **API 参考文档** | 函数参数 | 参数的数据类型或对象类型 | 参数说明及其对 API 的影响 |
| **数据库参考文档** | 数据库字段或列标题 | 数据类型 | 内容描述 |

如果命令参数（`<proptype>`）中包含多个关键字，第一个关键字可以使用 `<property>` 元素和它的三个子元素（`<proptype>`、`<propvalue>` 和 `<propdesc>`）。其余的关键字，也使用 `<property>` 元素，但只需要两个子元素（`<propvalue>` 和 `<propdesc>`）。

`<properties>` 元素是从 `<simpletable>` 元素定制而来的，在文档中通常显示为表格。你还可以使用 `<prophead>` 元素和它的三个子元素（`<proptypehd>`、`<propvaluehd>` 和 `<propdeschd>`）为属性类型、属性值和属性说明创建列标题。

[视频：创建属性表](https://youtu.be/njVoKQqltlA)

## 随堂练习

1. 请打开上一讲使用的练习文件 `l_reference_start.dita`。

2. 在 `<refsyn>` 元素的后面，插入一个 `<properties>` 元素，再插入一个子元素 `<prohead>`：

    ```xml
       ...
      </refsyn>
      <properties>
       <prophead>
       </prophead>
      </properties>
     </refbody>
    </reference>
    ```

3. 在 `<prophead>` 元素中，插入一个 `<proptypehd>` 元素、一个 `<propvaluehd>` 元素和一个 `<propdeschd>` 元素，并添加内容如下：

    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Reference//EN" "reference.dtd">
    <reference id="my_first_ref">
     <title>tNav</title>
     <refbody>
       ...
      </refsyn>
      <properties>
       <prophead>
        <proptypehd>属性类型</proptypehd>
        <propvaluehd>属性名称</propvaluehd>
        <propdeschd>属性说明</propdeschd>
       </prophead>
      </properties>
     </refbody>
    </reference>
    ```

    !!! note "注意"
        这三个元素必须按既定顺序排列，但不是每个都必须出现。否则，就会变成不合法的文档。

4. 在 `<prohead>` 元素的后面，插入一个 `<property>` 元素。

    ```xml
    ... </refsyn>
     <properties>
     <prophead>
     <proptypehd>属性类型</proptypehd>
     <propvaluehd>属性名称</propvaluehd>
     <propdeschd>属性说明</propdeschd>
     </prophead><property>
     </property></properties>
     </refbody>  </reference>
    ```

5. 在 `<property>` 元素中，插入一个 `<proptype>` 元素、一个 `<propvalue>` 元素和一个 `<propdesc>` 元素，并添加内容如下：

    ```xml
    ... </refsyn>
     <properties>
     <prophead>
     <proptypehd>属性类型</proptypehd>
     <propvaluehd>属性名称</propvaluehd>
     <propdeschd>属性说明</propdeschd>
     </prophead><property>
     <proptype>表格</proptype>
     <propvalue>dbo.DBBL</propvalue>
     <propdesc>钻水鸭</propdesc>
     </property></properties>
     </refbody>  </reference>
    ```

    !!! note "注意"
        如果跳过了某一个属性标题，也必须跳过相应的属性元素。例如，如果 `<prophead>` 元素中没有插入 `<propdeschd>`，`<property>` 元素中也不能插入 `<propdesc>` 元素。

6. 再插入几个 `<property>` 元素，并添加内容如下。

    ```xml
    ... </refsyn>
     <properties>
     <prophead>
     <proptypehd>属性类型</proptypehd>
     <propvaluehd>属性名称</propvaluehd>
     <propdeschd>属性说明</propdeschd>
     </prophead>
     <property>
     <proptype>表格</proptype>
     <propvalue>dbo.DBBL</propvalue>
     <propdesc>钻水鸭</propdesc>
     </property><property>
     <proptype></proptype>
     <propvalue>dbo.DVNG</propvalue>
     <propdesc>Diving ducks</propdesc>
     </property>
     <property>
     <proptype></proptype>
     <propvalue>dbo.WHST</propvalue>
     <propdesc>Whistling ducks</propdesc>
     </property>
     <property>
     <proptype>View</proptype>
     <propvalue>regn.ne</propvalue>
     <propdesc>Ducks located primarily in the northeast</propdesc>
     </property>
     <property>
     <proptype></proptype>
     <propvalue>regn.se</propvalue>
     <propdesc>Ducks located primarily in the southeast</propdesc>
     </property>
     <property>
     <proptype></proptype>
     <propvalue>pttrn.migr</propvalue>
     <propdesc>Ducks organized by migratory pattern</propdesc>
     </property></properties>
     </refbody>  </reference>
    ```

## 课后练习

1. 打开文件 `lesson1/l_reference_exercise_start.dita`，使用该文件将以下内容转换成 DITA：

    ```
    <hr/>
     <h3>addEntry</h3>
     <p>The <i>addEntry</i>
     command is used to enter a new documentation release into the content analysis database.</p>
     <tt><i>-addEntry</i>
     {nLanguage | nVersion | nOutput}</tt>
     <table>
     <tr>
     <td>Required?</td>
     <td>Parameter</td>
     <td>Description</td>
     </tr>
     <tr>
     <td>Yes</td>
     <td>nLanguage</td>
     <td>The language displayed by default</td>
     </tr>
     <tr>
     <td></td>
     <td>nVersion</td>
     <td>The version of the content displayed by default</td>
     </tr>
     <tr>
     <td></td>
     <td>nOutput</td>
     <td>The required delivery format</td>
     </tr>
     </table>
     <hr/>
    ```
