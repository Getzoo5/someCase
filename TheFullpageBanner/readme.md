#fullpage.js实现全屏显示的案例

######准备：
1.fullpage.js文件
2.jquery.min.js文件

##简介
######fullPage.js 是一个基于 jQuery 的插件，它能够很方便、很轻松的制作出全屏网站，主要功能有：



- 支持鼠标滚动


- 支持前进后退和键盘控制


- 多个回调函数



- 支持手机、平板触摸事件




- 支持 CSS3 动画


- 支持窗口缩放


- 窗口缩放时自动调整


- 可设置滚动宽度、背景颜色、滚动速度、循环选项、回调、文本对齐方式等等


##兼容性

jQuery 兼容

兼容 jQuery 1.7+。

浏览器兼容

 
IE8+ ✔  Chrome ✔	Firefox ✔	Opera ✔	Safari ✔

使用方法

###1、引入文件

	<link rel="stylesheet" href="css/jquery.fullPage.css">
	<script src="js/jquery.min.js"></script>

	<!-- jquery.easings.min.js 用于 easing 参数，也可以使用完整的 jQuery UI 代替，如果不需要设置 easing 参数，可去掉改文件 -->
	<script src="js/jquery.easings.min.js"></script>

	<!-- 如果 scrollOverflow 设置为 true，则需要引入 jquery.slimscroll.min.js，一般情况下不需要 -->
	<script src="js/jquery.slimscroll.min.js"></script>

	<script src="js/jquery.fullPage.js"></script>

###2、HTML

	<div id="dowebok">
    	<div class="section">
        	<h3>第一屏</h3>
    	</div>
    	<div class="section">
        	<h3>第二屏</h3>
    	</div>
    	<div class="section">
       	 	<h3>第三屏</h3>
    	</div>
    	<div class="section">
       		<h3>第四屏</h3>
    	</div>
	</div>

每个 section 代表一屏，默认显示“第一屏”，如果要指定加载页面时显示的“屏幕”，可以在对应的 section 加上 class=”active”，如：

	<div class="section active">第三屏</div>
同时，可以在 section 内加入 slide，如：

	<div id="dowebok">
    <div class="section">第一屏</div>
    <div class="section">第二屏</div>
    <div class="section">
        <div class="slide">第三屏的第一屏</div>
        <div class="slide">第三屏的第二屏</div>
        <div class="slide">第三屏的第三屏</div>
        <div class="slide">第三屏的第四屏</div>
    </div>
    <div class="section">第四屏</div>
	</div>

###3、JavaScript

	$(function(){
   		$('#dowebok').fullpage();
	});

##配置

###1、选项

选项	类型	默认值	说明
verticalCentered	字符串	true	内容是否垂直居中
resize	布尔值	false	字体是否随着窗口缩放而缩放
slidesColor	函数	无	设置背景颜色
anchors	数组	无	定义锚链接
scrollingSpeed	整数	700	滚动速度，单位为毫秒
easing	字符串	easeInQuart	滚动动画方式
menu	布尔值	false	绑定菜单，设定的相关属性与 anchors 的值对应后，菜单可以控制滚动
navigation	布尔值	false	是否显示项目导航
navigationPosition	字符串	right	项目导航的位置，可选 left 或 right
navigationColor	字符串	#000	项目导航的颜色
navigationTooltips	数组	空	项目导航的 tip
slidesNavigation	布尔值	false	是否显示左右滑块的项目导航
slidesNavPosition	字符串	bottom	左右滑块的项目导航的位置，可选 top 或 bottom
controlArrowColor	字符串	#fff	左右滑块的箭头的背景颜色
loopBottom	布尔值	false	滚动到最底部后是否滚回顶部
loopTop	布尔值	false	滚动到最顶部后是否滚底部
loopHorizontal	布尔值	true	左右滑块是否循环滑动``
autoScrolling	布尔值	true	是否使用插件的滚动方式，如果选择 false，则会出现浏览器自带的滚动条
scrollOverflow	布尔值	false	内容超过满屏后是否显示滚动条
css3	布尔值	false	是否使用 CSS3 transforms 滚动
paddingTop	字符串	0	与顶部的距离
paddingBottom	字符串	0	与底部距离
fixedElements	字符串	无	
normalScrollElements		无	
keyboardScrolling	布尔值	true	是否使用键盘方向键导航
touchSensitivity	整数	5	
continuousVertical	布尔值	false	是否循环滚动，与 loopTop 及 loopBottom 不兼容
animateAnchor	布尔值	true	
normalScrollElementTouchThreshold	整数	5
