# 设计Context

打开Context文件，设计器界面右侧显示了可用的组件，见下图：

![](/articles/studio/8-/images/image79.png)

→ **组件使用说明**

♢ **new context**: 新建context

♢ **mbe entity**: 根据现有的mbe生成context

♢ **Reference**: 关联线

## Context创建

首先在右侧组件箱中点击要添加的组件，然后再在画布要创建区域中点击，将Components目录下的new context组件点击到画布中生成，见下图：

![](/articles/studio/8-/images/image80.png)

具体设计方法，可以参照MBE的设计过程，当Context处于焦点时，见下图：

![](/articles/studio/8-/images/image81.png)

→ **属性**

♢ **Cascade** : 是否展开

♢ **From**:来源

♢ **From-Type**:来源类型

→ **属性视图（Context的属性字段）**

在属性视同中，用户可对Context的属性进行增加或删除操作。

♢ **ContextID**: Context内属性的标示；

♢ **Mapping ID**：设置与MBE映射的字段；

♢ **DataType**：字段的数据类型。

→ **关联线**

![](/articles/studio/8-/images/image82.png)

→ **属性**

♢ **Child-Field**: 子域；

♢ **Parent-Field**: 父域；

♢ **Target Context ID**: 目标模型ID, 关联的目标Context；

♢ **Mapping Type**: 映射方式,1,1 描述源与目标Context之间的关系；

♢ **Source Context Property**: 关联的源属性。

## 从MBE生成Context（企业版）

根据设计好的MBE创建Context：点击Context编辑器的面板的“Components”中的“mbe entity”组件，点击画布弹出“引用数据集”窗口，选择MBE，见下图：

![](/articles/studio/8-/images/image83.png)

此处示例直接使用已定义的MBE属性，不做任何修改，点击“确定“直接保存，见下图：

![](/articles/studio/8-/images/image81.png)

并且还可以在此基础上自定义扩展，添加修改Context上的属性，见下图：

![](/articles/studio/8-/images/image84.png)




