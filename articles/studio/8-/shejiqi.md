# Context模型设计器

Context是UI端的数据模型，移动应用平台的运行框架通过Context建立界面数据与MBE的联系。可以从以下几个角度理解：

→ **Context 构成**

♢ 模型、属性字段、模型间关系。类似实体模型，不过Context 运行在移动端，可以理解为MVC 架构的Model 层。

→ **Context 功能**

♢ 只是表明前台界面与后台数据之间的绑定关系，真正的数据是通过callService()方法传递的。

→ **Context 与MBE 关系**

♢ 开发过程中如果已经设计MBE 模型，Context 可以依据MBE 创建。如果没有MBE 模型，可以直接创建Context。

♢ Context 负责移动端数据的绑定、收集。如果有MBE，Context 提交数据到MBE，实现数据的持久化。如果没有MBE，需要有对应的服务接收Context 的数据。

