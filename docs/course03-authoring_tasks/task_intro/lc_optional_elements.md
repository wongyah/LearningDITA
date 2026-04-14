# 插入介绍性元素

`<prereq>`（prerequisite，即前置任务）和 `<context>` 元素主要用来介绍任务型主题的主要内容（操作流程），二者均为可选元素。

`<prereq>` 元素主要用来说明用户在任务开始之前需要知道的事情或者准备工作，例如：

- 必备物品，比如双筒望远镜或安装了鸟类识别应用程序的智能手机
- 必备知识或信息，比如关于迁徙模式的知识
- 前置任务，比如学习识别鸭子的基础课程

`<context>` 元素主要用来说明与任务有关的背景信息，比如任务目标和用户收获。`<context>` 元素的内容应该尽可能简短。如果需要提供更详细的背景信息，请使用概念型主题。

`<prereq>` 和 `<context>` 虽然是可选元素，但它们必须按照既定次序排列：`<prereq>` 元素必须位于 `<context>` 元素的前面。

<!-- [视频：介绍性元素在任务型主题中的次序](https://youtu.be/Bhaeafcemis) -->

## 随堂练习

1. 打开上一节使用的练习文件 `l_task_start.dita`。

2. 在 `<taskbody>` 元素中，插入一个 `<prereq>` 元素。

    ```xml
    <taskbody>
      <prereq>
        <p>去观看野鸭之前，必须先了解一下野鸭长什么样。</p>
      </prereq>
    </taskbody>
    ```

3. 在`<prereq>`元素的后面，插入一个`<context>`元素。

    ```xml
    <taskbody>
      ... </prereq>
      <context>
        <p>观看野鸭可以让人平心静气、放松身心。</p>
        <p>阅读本文可以让你的野鸭观看之旅更加完美。</p>
      </context>
    </taskbody>
    ```

4. 对照[随堂练习的参考答案] (`lesson1/l_new_task.dita`)，自行批改一下你刚刚完成的练习作业 (`l_new_task_start.dita`)。

现在，你的任务型主题里有一个标题、一组前置任务和一段背景信息。下一讲将教你如何在任务型主题中插入操作流程。

## 课后练习

1. 打开文件 `lesson1/l_new_task_exercise_start.dita`，使用该文件将以下内容转换成 DITA：

    --8<-- "div_exercise_content.md:start"
    <h2 style="margin: .64em 0 .64em;">为你的内容策略编写商业案例</h2>

    **开始之前**
    
    全面评估你的内容和内容开发流程，了解当前策略和所需策略之间的差距。
     
    **任务说明**
    
    本教程将带你编写一个商业案例，该案例将阐述你们公司为什么需要一套新的内容策略。

    你可能会发现，你的公司可以在以下几个方面节省内容制作成本：

    - 流程自动化
    - 内容复用
    - 内容本地化
    
    --8<-- "div_exercise_content.md:end"

2. 对照[课后练习的参考答案] (`lesson1/l_new_task_exercise.dita`)，自行批改一下你刚刚完成的练习作业 (`lesson1/l_new_task_exercise_start.dita`)。

<!-- links -->
[随堂练习的参考答案]: sa_new_task.md#_2
[课后练习的参考答案]: sa_new_task.md#_3
