# jquery.pageScroll

jquery单页滚屏插件。

## 兼容性

- IE7+
- Mobile Browser

## 快速上手

	<link rel="stylesheet" href="jquery.pageScroll.css">

	<div id="main" class="wrapper">
		<div class="page">page1</div>
		<div class="page">page2</div>
		<div class="page">page3</div>
		<div class="page">page4</div>
	</div>

	<script src="jquery-1.11.3.js"></script>
	<script src="jquery.pageScroll.js"></script>
	<script>
		$('#main').pageScroll();
	</script>

[查看demo](http://htmlpreview.github.io/?https://github.com/huanz/jquery.pageScroll/blob/master/demo/index.html)

## API说明

### 参数

	$('*').pageScroll({
    	pageContainer: '.page',
    	easing: 'ease',
    	animationTime: 1000,
    	pagination: true,
    	keyboard: true,
    	beforeMove: function(pageIndex, $el) {},
        afterMove: function(pageIndex, $el) {},
        loop: false
	});
	
#### pageContainer

每屏的选择器，默认是`.page`。

#### easing

动画缓冲效果，默认是`ease`，其它可选的还有：`linear` | `ease-in` | `ease-out` | `ease-in-out` | `cubic-bezier(<number>, <number>, <number>, <number>)`。

#### animationTime

每屏动画切换的时间，这段时间内，不能重复切换，默认是`1000ms`。

#### pagination

是否显示右边的分页信息，默认显示是`true`。

#### keyboard

是否开启通过键盘上下键来控制上下屏，默认开启是`true`。

#### beforeMove / afterMove

屏幕切换时会分别触发这两个函数，传入两个参数。

`pageIndex`：当前屏索引，从`0`开始。

`$el`：当前屏的外层jquery节点对象。

#### loop

是否开启循环滚动，默认不开启是`false`。


### 方法

#### moveToPage

跳转到某一屏：`$('*').moveToPage(pageIndex)`。





