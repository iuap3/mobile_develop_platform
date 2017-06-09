# 调试方式1 

## 启动LogCat

在studio的工具栏上可以直接打开LogCat，如下图所示：

![](/articles/studio/13-/images/image200.png)

LogCat启动通常需要一定的时间。下图是运行出来后LogCat的默认状态：

![](/articles/studio/13-/images/image201.png)

## 过滤跟调试有关的Log信息

LogCat启动后，在LogCat页签的条件搜索框内输入【tag:uap】或者【tag:uap_mobile_js_】，进行日志过滤，加入条件的好处就是，我们只看跟我们有关系日志。

接下来我们调试一个APP的首页List页面加以说明。

在查看LogCat时，可以先清除一下LogCat内的信息，然后我们启动运行APP，此时在LogCat中可以看到加载首页List页面的整个过程的Log信息。

为了能快速找到我们调试需要的log，可以再LogCat的搜索框内进一步进行过滤。

例如，搜索框内输入【tag:uap】，在LogCat中会仅仅显示tag为【UAP 】开头的类型的日志，如下图所示：

![](/articles/studio/13-/images/image203.png)

搜索框内输入【tag:uap_mobile_js_engine】，在LogCat中会仅仅显示tag为【UAP_MOBILE_JS_ENGINE】类型的日志。在其中找到load js finish一行，完整信息是“js finished : file:///android_asset/loads/loadListController.html”

这是表明系统加载loadListController.html完成，接下来就能在logcat中看到该页面加载过程中执行的JS过程。如下图所示：

![](/articles/studio/13-/images/image204.png)

## 查找定位要调试的JS代码

在上图中，鼠标选中jsmethod：$router.eval……..这一行，在鼠标右键菜单中点击Filter similar message….，如下图所示：

![](/articles/studio/13-/images/image205.png)

弹出如下窗口，拷贝出$router.eval(xxx, xxx, {…})这样的js代码，这就是我们要调试代码的入口点接下来对这句js代码进行调试。这里我们简单讲一下$router.eval()方法。$router在JS运行时是一个系统级的全局对象，所有原生调用JS方法都是从$router的eval方法开始的，其中eval方法的第一参数是JSController的全名，第二个参数就是运行JS业务代码的方法的字符串形式，第三个参数是当前Context对象，所以我们在调试的时候，首先要找到$router.eval(xxx,xxx,{})这样的代码

![](/articles/studio/13-/images/image206.png)

## 开始调试JS代码

我们打开工程目录native\android\asset\loads文件夹，在该文件夹内有一组HTML文件。这些HTML分别对应应用中的页面，每一个html文件对应一个dsl页面。其命名规则为loadxxxController.html，例如List页面对应的HTML文件为loadListController.html。JS调试就是从调试这些HTML文件开始，如下图所示：

![](/articles/studio/13-/images/image138.png)

我们找到native\android\asset\loads\loadListController.html并打开，打开方式可以使用任意的编辑器，这里我们使用Studio默认自带的HTML Editor打开，如下图所示：

![](/articles/studio/13-/images/image139.png)

在下图位置粘贴刚才复制的JS代码，并在JS代码前加入debugger;并保存，如下图所示

![](/articles/studio/13-/images/image140.png)

接下可以使用任何JS调试工具进行调试。这里推荐使用Chrome浏览器进行调试。当然你也可以使用其它浏览器（例如IE、Safari等）进行调试。

我们打开Chrome浏览器，按F12，启动开发者工具，如下图所示：

![](/articles/studio/13-/images/image141.png)

当然也可以在浏览器的工具菜单中打开【开发者工具】，如下图所示：

![](/articles/studio/13-/images/image142.png)

Chrome浏览器的开发者工具进行JS代码调试，不熟悉的可以在晚上搜索一下如何使用，这里我们不做过多的介绍了。

接下来，我们把native\android\asset\loads\loadListController.html页面拖拽如chrome浏览器中，浏览器会自动在我们写【debugger】的地方断点断住，如下图所示：

![](/articles/studio/13-/images/image143.png)

我们在开发者工具的Source中找到我们写JS代码的JSController文件，双击打开，在我们要调试的listview0_onload方法中设置一个断点，如下图所示：

![](/articles/studio/13-/images/image144.png)

接下来按F8或者开发者工具中的继续运行按钮，让JS代码运行至我们打断点的地方，如下图：

![](/articles/studio/13-/images/image145.png)

接下来可以单步（F10配合F11）进行调试了，配合开发者工具中的Watch Expressions可以实时查看变量可以进一步帮助我们调试。

这里说明一点，由于是在浏览器进行web调试，本身和原生（安卓）运行环境没有任何关联，所以在遇到执行原生服务的时候，是没有办法调试的(例如上面例子中$ctx.push(json))，但是我们可以通过LogCat监视我们执行的结果信息。

 总之，借助LogCat和web浏览器我们可以使用web调试的方式来帮助我们进行JS业务代码逻辑的调试。

















