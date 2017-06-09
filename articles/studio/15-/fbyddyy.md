# 发布移动端应用APP

## 编译生成原生代码

UAP Mobile 编译工具支持两种打包方式，本地打包（只支持Andorid打包）和云打包（支持iOS和Andorid打包）。

一键式打包又可分为本地编译打包和云打包，一键式打包默认都是Andorid打包。

**本地编译打包**

UAP Mobile 编译工具 ->本地编译打包，该编译打包只支持Andorid版本。

![](/articles/studio/15-/images/image159.png)

编译打包支持后台运行，如下图所示：

![](/articles/studio/15-/images/image160.png)

编译打包成功后，弹出创建成功提示窗口。如下图所示：

![](/articles/studio/15-/images/image161.png)

点击确定，安装包生成完毕。

→ **云打包**

鼠标右键点击UAP Mobile 编译工具->云打包

![](/articles/studio/15-/images/image162.png)

手动打包采用的是云打包的方式，它可选择生成iOS或Android下的应用, 手动打包过程分为两步，第一步先生成代码，然后再生成安装包。

手动打包首先选中组件，并点击鼠标右键，可见弹出框，点击弹出框中的“UAP Mobile 编译工具”下的“生成代码”, 如下图所示：

![](/articles/studio/15-/images/image163.png)

选择登陆页面，及需要应用中添加的页面，后点击下一步，如下图所示：

![](/articles/studio/15-/images/image164.png)

在弹出页面中选择生成应用部署的设备的环境IOS 或Android，最后点击“完成”按钮，至此编译完成。

![](/articles/studio/15-/images/image165.png)

→ **属性**

♢ **Platform Selection**：IOS,Android

♢ **APP ID**:编译dsl的包名

♢ **Project Name**:编译dsl的工程名

♢ **Ref Icon**:应用图标

♢ **Ref Libs**:引用的包

当编译成功时弹出的成功框，如下图所示：

![](/articles/studio/15-/images/image166.png)

## 导出应用包

首先选中组件，并点击鼠标右键，可见弹出框，点击弹出框中的“UAP Mobile工具”下的“导出原生包”, 如下图所示：

![](/articles/studio/15-/images/image167.png)

在弹出页面中选择生成应用部署的设备的环境IOS 或Android，最后点击“完成”按钮，至此编译完成。

![](/articles/studio/15-/images/image168.png)

→ **属性**

♢ **Compress JS**: 是否压缩JAVASCRIPT

♢ **Compress Html**: 是否压缩Html

♢ **Select Export Location**: 导出的文件生成的位置

导出的应用包如下图所示：

![](/articles/studio/15-/images/image169.png)

→ 安装测试方式：

♢ 电脑安装个iTunes，即可安装

♢ 或安装91助手，双击*.ipa即可

![](/articles/studio/15-/images/image170.png)

## MA打包

在开发平台中提供MA Package打包工具，按照MA Package规范打包出可以在MA导入的ZIP包。

MA打包必须支持MA2.7以上版本，打包Source目录下的类。最终生成zip包。包名称是appID+MA打包版本号。

首先选中组件，并点击鼠标右键，可见弹出框，点击弹出框中的“UAP Mobile工具”下的“MA打包”, 如下图所示：

![](/articles/studio/15-/images/image171.png)

## 发布到MA

在移动门户上，可查看发布的MA。

“窗口”->“首选项”，配置MA Server地址。

![](/articles/studio/15-/images/image172.png)

首先选中组件，并点击鼠标右键，可见弹出框，点击弹出框中的“实时预览”，如下图所示：

![](/articles/studio/15-/images/image173.png)

![](/articles/studio/15-/images/image174.png)

点击弹出框中的“发布到MA”。
