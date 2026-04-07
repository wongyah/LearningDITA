# 插入任务示例

`<example>` 元素主要用来编写整个任务的示例。`<example>` 元素和 `<stepxmp>` 元素很相似。只不过，`<stepxmp>` 元素主要用来编写某个操作步骤的示例，而不是整个任务的示例。

<!-- [视频：在任务型主题中插入任务示例](https://youtu.be/kQS7FCSLJ7E) -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在 `<result>` 元素的后面，插入一个 `<example>` 元素。

    ```xml
    ...
        </result>
        <example>
        </example>
      </taskbody>
    </task>
    ```

3. 在 `<example>` 元素中添加内容如下：

    ```xml
    ...
        </result>
        <example>
          <p>别指望会有<a href="https://dai.ly/x2j6pt1">《混乱达菲鸭》</a>那种荒诞不经的行为。</p>
        </example>
      </taskbody>
    </task>
    ```