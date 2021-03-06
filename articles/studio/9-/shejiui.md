# 设计UI

## 设计UI页面

设计window界面，拖动控件面板中的控件到设计器画布，根据需要设计你的window界面，如下列图表：

1、**布局控件 **

![](/articles/studio/9-/images/image101.png)

2、**基础控件**

![](/articles/studio/9-/images/image102.png)

3、**图表控件**

![](/articles/studio/9-/images/image103.png)

4、**Widgets**

支持可视化的widget设计，并支持在UI设计器的控件列表中自定义widget的图标和名称。

![](/articles/studio/9-/images/image104.png)

5、**高级控件**

![](/articles/studio/9-/images/image105.png)

6、多媒体控件

提供多媒体功能，图片、录音、音频视频等控件。

![](/articles/studio/9-/images/image106.png)

7、**组合控件**

提供组合控件，导航栏、工具栏等等控件。

![](/articles/studio/9-/images/image107.png)

**注意**：

→ 移动应用开发平台提供了属性配置,开发者可在应用中根据需要灵活添加修改控件库，所以在使用如二维码、地图等控件时，需要在工程上选择需要的控件库。否则应用会出现闪退情况。具体操作步骤如下: 

1、在UAP Mobile Explorer视图窗口中选择配置项目后,点击鼠标右键, 如下图:

![](/articles/studio/9-/images/image108.png)

 
2、在属性配置窗口的UAP Mobile Settings→Native Natures窗口中进行控件选择， 如下图：

![](/articles/studio/9-/images/image109.png)

 
→ 在Andorid开发环境下移动地图控件支持Baidu地图, 在iOS下支持的是高德地图。在使用地图控件时，需要开发者首先注册地图 key，否则地图控件将不能正常使用。申请注册地图key操作步骤详细, 可参考Baidu地图开发官方网站 ( http://developer.baidu.com/map/ ) 。



## 设置UI控件属性

点击设计器下方的焦点控件指示条上的View1，见下图：

![](/articles/studio/9-/images/image110.png)

在属性视图可以设置：属性，样式，动作，动作列表，组件列表，其中后两项为window特有的功能，见下图：

![](/articles/studio/9-/images/image111.png)

→ **属性**：通用属性，根据控件不同而不同

  ♢ **基本**

   ◆ **是否可见**：是否在页面上显示

   ◆ **唯一标示**：window ID

   ◆ **是否可用**:是否是可用状态

  ♢ **控制器**

   ◆ **命名空间**：window的Controller对应的命名空间

   ◆ **控制器名称**:window对应的Controller名称

  ♢ **绑定(设置页面的数据来源Context)**:

   ◆ **上下文**：能够选择组件下的Context，如选择dpo文件，见下图：

![](/articles/studio/9-/images/image112.png)

→ **样式**

![](/articles/studio/9-/images/image113.png)

通用属性，设置的样式及布局，对应属性信息请参照CSS盒模型。

→ **动作**

![](/articles/studio/9-/images/image114.png)

通用属性，设计对应控件等的事件

→ **动作列表**

“动作”的作用是用于调用服务器端处理，或者页面流转，或者创建动作使用JavaScript方法执行逻辑、调用设备服务（如GPS、电话等等）。

动作列表中，包含“增加”、“修改”、“删除”三个功能，见下图：

![](/articles/studio/9-/images/image115.jpeg)

点击“增加”，弹出对话框，输入动作名“text”，及其他明细，见下图：

![](/articles/studio/9-/images/image116.png)

点击“确定”，即增加了动作“text”，见下图：

![](/articles/studio/9-/images/image117.png)









 



















