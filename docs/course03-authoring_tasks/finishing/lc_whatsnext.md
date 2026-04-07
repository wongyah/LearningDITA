# 插入后置任务

`<taskbody>` 元素中的最后一个子元素是 `<postreq>`（读作“postrequisite”，即后置任务）元素。

使用 `<postreq>` 元素编写任务完成后用户必须要做的事情。例如：

- 关机或关闭文件
- 记录任务完成情况
- 执行后续任务

<!-- [视频：在任务型主题中结束性元素的次序](https://youtu.be/scYD2nY7NMA) -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在 `<example>` 元素的后面，插入一个 `<postreq>` 元素。

    ```xml
    ...
        </example>
        <postreq>
        </postreq>
      </taskbody>
    </task>
    ```

3. 在 `<postreq>` 元素中添加内容如下：

    ```xml
    ...
        </example>
        <postreq>
          <ul>
            <li>使用相机再观察一次鸭子。</li>
            <li>去观看其他鸭子。</li>
          </ul>
        </postreq>  
      </taskbody>
    </task>
    ```

4. 对照[随堂练习的参考答案] (`lesson3/l_task_finishing.dita`)，自行批改一下你刚刚完成的练习作业 (`l_new_task_start.dita`)。

## 课后练习

1. 打开文件 `lesson3/l_task_finishing_exercise_start.dita`，使用该文件将以下内容转换成 DITA：

    --8<-- "sample_content.md:start"
    <h2 style="margin: .64em 0 .64em;">管理变革</h2>

    1.  向高层管理人员和一线员工展示变革的价值。
    2.  提供培训和知识转移。
        - 线下培训
        - 在线培训
        - 面向培训师的培训
    3.  发现新工作流程中的问题，并识别哪些问题的合理的、哪些问题是由于抵触情绪和本能而提出的。
    4.  通过试点项目向参与者说明工作流程中的变化。

    **结果**

    当公司的工作流程发生变化时，良好的管理至关重要。如果管理不善，新流程很可能会实施失败。糟糕的管理会不仅会扼杀新流程的实施，还会让所有相关人员陷入困境。

    **示例**

    如果没有良好的变革管理，那些习惯性坚决反对变革的员工可能会获得其他团队成员的支持，最终导致几乎所有人都拒绝使用新系统。

    **下一步**

    成功管理了变革之后，你就可以在新系统中创建有用的内容了。

    --8<-- "sample_content.md:end"

2. 对照[课后练习的参考答案] (`lesson3/l_task_finishing_exercise.dita`)，自行批改一下你刚刚完成的练习作业 (`lesson3/l_task_finishing_exercise_start.dita`)。

<!-- links -->
[随堂练习的参考答案]: l_task_finishing.md#_2
[课后练习的参考答案]: l_task_finishing.md#_3