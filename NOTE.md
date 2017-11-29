### GankDaliy

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


---
### MeiZi	
作者:drakeet 数据来自代码家的干货网站：http://gank.io
	
源代码：[https://github.com/drakeet/Meizhi](https://github.com/drakeet/Meizhi)	
	
WebView常用配置	进度显示,标题

Material Design 	CoordinatorLayout+AppBarLayout+CollapsingToolBarLayout+ToolBar+NestedScrollView

FloatingActionButton.Behavior	监听RecyclerView滑动设置behavior

TextSwitcher	具有设置动画的API(直接使用系统提供的淡入淡出)

RxJava 使用多种操作符	

Retrofit 解析时间指定一个固定的格式	GsonConverterFactory.create(gson) setDateFormat("yyyy-MM-dd'T'HH:mm:ss.SSS'Z'")

单个gradle文件统一管理所有module的共有编译信息	"compileSdkVersion buildToolsVersion minSdkVersion targetSdkVersion
versionCode versionName"

Gralde控制生成APK文件名称	

Retrolambda使用	

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
> View#post与Handler#post的区别，以及导致的内存泄漏分析	
> 
> [http://www.jianshu.com/p/7d5808eae883](http://www.jianshu.com/p/7d5808eae883)
