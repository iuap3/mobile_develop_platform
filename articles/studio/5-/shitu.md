# 平台关键视图

本章主要介绍UAP Mobile 开发中用到的几个关键的视图。它们是UAP Mobile 透视图、LogCat、控制台、属性视图、大纲视图、错误日志。

检查是否在透视图中

在开发过程中，通过控制台查看日志信息，发生错误的时候在控制台中有相应的错误信息输出，在控制台uap mobile build console视图里,所有信息都会记录显示。

## UAP MOBILE透视图

开发UAP Mobile项目，首先需要确认已经正确安装了UAP Studio。UAP Mobile项目开发，需要使用到UAP MOBILE透视图，在UAP MOBILE透视图中提供了许多支持业务组件项目开发的功能。

打开UAP Studio，通过菜单“窗口”->“打开透视图”，选择“UAP Mobile”，见下图：

![](/articles/studio/5-/images/image23.png)

![](/articles/studio/5-/images/image24.png)

## LogCat

LogCat是用来监测真实手机端信息输出，在UAP Studio的工具栏上可以直接打开LogCat，如下图所示：

![](/articles/studio/5-/images/image25.png)

下图是运行出来后LogCat的默认状态：

![](/articles/studio/5-/images/image26.png)

### 过滤Log信息

LogCat提供过滤Log信息功能，在LogCat页签的条件搜索框内输入关键字进行日志过滤。

在查看LogCat时，建议先清除一下信息，然后启动运行APP，此时在LogCat中可以看到加载首页List页面的整个过程的Log信息。

为了能快速找到我们调试需要的log，可以再LogCat的搜索框内进一步进行过滤。 

例如，搜索框内输入【tag:uap_mobile_js_engine】，在LogCat中会仅仅显示tag为【UAP_MOBILE_JS_ENGINE】类型的日志。在其中找到load js finish一行，完整信息是“js finished : file:///android_asset/loads/loadListController.html”

这是表明系统加载loadListController.html完成，接下来就能在logcat中看到该页面加载过程中执行的JS过程。如下图所示：

![](/articles/studio/5-/images/image27.png)

### 查找定位JS代码

选中一行日志，在鼠标右键菜单中点击“Filter similar message”，如下图所示：

![](/articles/studio/5-/images/image28.png)

系统弹出如下窗口：

![](/articles/studio/5-/images/image29.png)

拷贝出$router.eval(xxx, xxx, {…})这样的js代码，如果要进行JS调试话，这就是调试代码的入口点。

注：$router在JS运行时是一个系统级的全局对象，所有原生调用JS方法都是从$router的eval方法开始的，其中eval方法的第一参数是JSController的全名，第二个参数就是运行JS业务代码的方法的字符串形式，第三个参数是当前Context对象。

在调试的时候，首先要找到的就是$router.eval(xxx,xxx,{})代码。

## 控制台

通过菜单“窗口”->“显示视图”->“其他”，选择“控制台”，见下图：

![](/articles/studio/5-/images/image30.png)

控制台是开发类工具所有信息的输出，在配合ui设计器时会被经常使用到。

![](/articles/studio/5-/images/image31.png)

## 大纲视图

在“显示视图”选择“大纲”，见下图:

![](/articles/studio/5-/images/image32.png)

大纲视图为查看界面控件树的层次提供支持。如下图所示：

![](/articles/studio/5-/images/image33.png)

## 错误日志

在“显示视图”选择“错误日志”，见下图:

![](/articles/studio/5-/images/image34.png)

错误日志主要是为了记录设计态过程中发生的错误。

通常错误日志部署在下方，错误日志窗口采用列表的形式列出所有错误信息，并且可以根据错误的消息、插件名称或错误日期进行排序显示。如下图所示：

![](/articles/studio/5-/images/image35.png)

## 属性视图

在“显示视图”选择“属性”打开属性视图，见下图:

![](/articles/studio/5-/images/image36.png)

## 模型视图(实体)（企业版）

该视图用于显示、设置MBE，MBP 文件的属性。

“窗口”-》“显示视图”-》“MDP 视图”-》“模型视图”。

![](/articles/studio/5-/images/image37.png)

![](/articles/studio/5-/images/image38.png)

## 属性视图(实体)

“窗口”->“显示视图”->“其他”->“属性视图(context)”，该视图用于显示、设置context 的属性。

![](/articles/studio/5-/images/image39.png)














