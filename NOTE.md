# GankDaliy

整个项目借鉴自 @drakeet 的妹纸。但是在原项目基础上，在代码层面和UI层面上做了自己的修改。

源代码： [https://github.com/maoruibin/GankDaily](https://github.com/maoruibin/GankDaily)

较简单采用MVP架构

Retrofit+RxAndroid

Material Design风格(AppBarLayout+ToolBar+RecyclerView)

Android与JavaScript的互相调用

DialogFragment上通过Webview加载本地Html资源文件

View.setColorFilter 对ImageView的模糊处理

Android5.0 过渡动画

PhotoView查看图片

Gralde控制生成APK文件名称

##### 笔记
> onPostCreate 	
> 
> "onPostCreate是指onPostCreate方法是指onCreate方法彻底执行完毕的回调"
> 
> [http://www.jianshu.com/p/d586c3406cfb](http://www.jianshu.com/p/d586c3406cfb)

-
> View#post与Handler#post的区别，以及导致的内存泄漏分析	
> 
> [http://www.jianshu.com/p/7d5808eae883](http://www.jianshu.com/p/7d5808eae883)

-

Android L新特性之 页面内容&共享元素过渡动画
>[http://www.jianshu.com/p/50f62d9e60e1](http://www.jianshu.com/p/50f62d9e60e1)
> [http://jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0113/2310.html](http://jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0113/2310.html)


---
# MeiZi	
作者&设计:drakeet 数据来自代码家的干货网站：http://gank.io
	
源代码：[https://github.com/drakeet/Meizhi](https://github.com/drakeet/Meizhi)	
	
WebView常用配置	进度显示,网页标题显示在ToolBar

***Material Design*** 	*CoordinatorLayout+AppBarLayout+CollapsingToolBarLayout+ToolBar*

FloatingActionButton.Behavior	自定义Behavior

TextSwitcher	该View具有设置动画的API-setInAnimation,setOutAnimation(直接使用系统提供的淡入淡出)

RxJava 使用多种操作符	

Retrofit 解析时间指定一个固定的格式	GsonConverterFactory.create(gson) setDateFormat("yyyy-MM-dd'T'HH:mm:ss.SSS'Z'")

单个gradle文件统一管理所有module的共有编译信息	"compileSdkVersion buildToolsVersion minSdkVersion targetSdkVersion
versionCode versionName"

Gralde控制生成APK文件名称	

Retrolambda使用	

Otto 是square公司出的一个事件库（pub/sub模式），用来简化应用程序组件之间的通讯。

AlarmManager+BroadcastReceiver+HeadsupCompat(第三方Library) 定时弹出悬挂式Notification 看下图
![screenshot1](./screenshot1.png)

横竖屏切换布局的处理(当前版本在清单文件中使Activity强制竖屏,相关代码不执行了)

TextView设置2种不同样式文本

RecyclerView的Item布局中某个View执行显示动画，非整个Item的显示动画

##### 笔记
> ImageView显示的图片资源可以是通过XML属性或者Java代码指定显示的图片内容，可以通过设置Resource、Uri 、Bitmap对象、Drawable对象来指定。  
> 
> ScaleType属性的修改本质上根据设定的枚举将变换赋值给mMatrix，最终通过onDraw中的矩阵操作实现。
> 	
> ImageView 的scaleType 属性 [http://www.jianshu.com/p/32e335d5b842](http://www.jianshu.com/p/32e335d5b842)

> cropToPadding属性可以让图片内容是在padding基础上进行变换（缩放，移动），根据实践如果使用了mScrollX mScrollY属性或者scaleType设置为MATRIX类型时会配合用到这个属性

>adjustViewBounds属性主要是让ImageView根据图片原有比例的约束下将调整大小，注意必须要限定住宽或者高，即将其中一个属性设置为match_parent或者确定尺寸。
>
>ImageView学习笔记 [http://www.jianshu.com/p/1fa1321f106c](http://www.jianshu.com/p/1fa1321f106c)

-
> AppCompatTheme 包含背景点击效果 "?attr/selectableItemBackground" -视图范围内展示波纹效果
> ![image1](./images/image1.gif)
> 
> ?android:attr/selectableItemBackgroundBorderless –将波纹效果延伸至视图之外。
> 
> ![image1](./images/image2.gif)

- 
> Android5.0新特性推出了悬挂式Notification [http://www.jianshu.com/p/e766ce44268b](http://www.jianshu.com/p/e766ce44268b)

-
>Fragment

>setRetainInstance(true) 旋转时 Fragment 不需要重新创建。fragment始终持有父Activity的引用,即使在父Activity被销毁和重新创建之后。
>
>setHasOptionsMenu(true) 无论如何, 你必须在 onCreate() 期间调用 setHasOptionsMenu() 来指出fragment愿意添加item到选项菜单(否则, fragment将接收不到对 onCreateOptionsMenu()的调用)

---
# Douya
作者:
Zhang Hai

Douban, Inc.

Android Developer Intern

July 2016 – Sept. 2016, Beijing, China 
	
源代码：[https://github.com/DreaminginCodeZH/Douya](https://github.com/DreaminginCodeZH/Douya)	

***Material Design***

DrawerLayout

VectorDrawable



##### 笔记
系统5.0以上设置透明状态栏
> 
> view.setSystemUiVisibility(
                    View.SYSTEM_UI_FLAG_LAYOUT_STABLE | View.SYSTEM_UI_FLAG_LAYOUT_FULLSCREEN);
getWindow().setStatusBarColor(Color.TRANSPARENT)
[http://blog.csdn.net/guolin_blog/article/details/51763825](http://blog.csdn.net/guolin_blog/article/details/51763825)

允许使用transitions  
> getWindow().requestFeature(Window.FEATURE_CONTENT_TRANSITIONS); 

关闭shared element overlay
>setSharedElementsUseOverlay(false)

IntentService
>[鸿洋文章链接](http://blog.csdn.net/lmj623565791/article/details/47143563)

保存图片到系统
>[MediaStore.Images.Media.insertImage](http://blog.csdn.net/t12x3456/article/details/9099209)

StrictMode严苛模式
>[StrictMode就是用来指定一系列策略（policy），对相应规则（rule）进行检查并且做出反应。](https://www.jianshu.com/p/113b9c54b5d1)

# Bailan

应用商店App,Retorfit2+Rxjava2+Mvp+Dagger2架构开发多层封装，高度解耦，框架比较成熟

源代码： [https://github.com/guzhigang001/Bailan](https://github.com/guzhigang001/Bailan)

#### 技术亮点

 Dagger2 

 Android6.0运行时权限

 RecycleView高级封装，万能RecycleView，试用90%以上布局

 通过高度计算设计沉浸式状态栏

 多种自定义控件(比如自定义轮播图，下载进度Progress，SubTabNavitagor,Flowlayout,阻尼回弹View，伸缩TextView等)

 功能强大，健壮，完善的网络请求库(基于Rxjava2，retrofit2，GreenDAO，Okhttp3的网络请求库，支持多文件下载，断网重新请求，Rxjava生命周期管理，缓存数据，断电续传，异常处理....)

 **利用AIDL获取缓存信息** 

 观察者模式多页面下载进度同步

 自定义带进度WebView

 应用下载后自定义安装

 自定义Activity跳转动画

 根据数据请求结果动态更新界面

------------

##### 笔记
> Dagger2 	
> 
> 依赖注入框架，为了进一步解耦和方便测试，我们会使用依赖注入的方式构建对象.特点:在编译期间自动生成代码
> 
> [https://www.jianshu.com/p/24af4c102f62](https://www.jianshu.com/p/24af4c102f62)

-
> 
> 
> 


---