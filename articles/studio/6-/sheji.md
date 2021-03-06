# 设计MBE

点击MBE设计器空白处，在“属性”页签输入名称空间和所属模块，带黄色感叹号的内容是必填项，见下图：

![](/articles/studio/6-/images/image58.png)

→ **属性**

**ID**：MBE文件的唯一标识

**代码风格**：选择风格样式

**多语资源ID**：多语资源ID

**多语资源模块名**：多语资源模块名

**扩展标签**：方便查找该元数据的附加信息

**是否预加载**：是否预先加载数据

**所属模块**：所属的模块

**选择组件**：用于设置需要映射的普通BE

**增量开发**：是否是增量开发

**主实体**：设置主实体

→ **连接线**

点击MBE设计器右上角的左向箭头，展开控件面板，见下图：

![](/articles/studio/6-/images/image59.png)

可以从工具箱拖动组件到画布中开始工作，如从“业务组件工具箱”拖动“实体”到画布，见下图：

![](/articles/studio/6-/images/image60.png)

选择画布中的“实体”组件，将光标落在属性行上，可设置其属性名称，并可以进行增加删除等操作。

![](/articles/studio/6-/images/image61.png)

→ **界面说明**：

**名称**：字段名称

**显示名称**：字段的显示名称

**类型样式**：Single:单数据

             Array:数组类型的数据

             List:列表类型的数据

             Ref:引用类型的数据


**类型**：字段数据类型

**描述**：数据描述信息

**缺省值**：数据默认值

**最大值**：数据最大值

**最小值**：数据最小值

**长度**：数据字段长度

**精度**：数据精度

**访问策略**：设置访问数据实体的类型

下图为设置完成的“实体”组件：

→ **关联关系工具箱**：

属性设置完成后，使用关联关系工具箱中的关系线进行联系连接。

![](/articles/studio/6-/images/image62.png)

→ 组合线 

普通的聚合,从子实体画到头实体，源属性必选项，下图这种设置可表示1对N的关系：

![](/articles/studio/6-/images/image63.png)

点击【关联关系工具箱】->【组合】图标，选中需组合的实体，在拖动关系后，部分属性已经自动设置。

![](/articles/studio/6-/images/image64.png)

→ **多样性**

  **目标**：对应目标值

  **源**：对应源值

→ **连接**

  **目标**：目标实体

  **源点**：源实体

点击保存按钮，保存MBE文件，见下图：

![](/articles/studio/6-/images/image65.png)






