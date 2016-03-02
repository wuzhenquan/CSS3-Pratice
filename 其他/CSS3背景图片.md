<link :="stylesheet" href="http://yandex.st/highlightjs/6.1/styles/default.min.css">
<script src="http://yandex.st/highlightjs/6.1/highlight.min.js"></script>
<script>
    hljs.tabReplace = '    ';
    hljs.initHighlightingOnLoad();
</script>


## CSS3之背景图片

通常我们在页面上添加图片的时候, 在`<img src=""></img>`添加上图片链接就好了, 然而这种方法添加的图片, 对图片的的样式更改, 自由度比较低. CSS3中的定义元素的背景图片, 使得元素上图片的可操作性更高,具体的有:

- backgroun-image: 添加一个或多个背景图片
- background-origin:设置元素背景图片的起始位置
- background-clip: 裁剪背景图片
- background-size: 设置背景图片中的大小
- background-repeat: 设置背景图片是否重复

在代码中的形式是这样的

	.div{
		background: url(图片链接地址);
   		background-position: 参数;
    	background-repeat: 参数;
    	background-size: 参数;
	}

具体分析:

### background-origin

注意, 当`background-repeat:no repeat;`时, background-origin才有效

三种情况

- `background-origin: border-box;`图片从边框开始显示
- `background-origin: padding-box;`图片从内边距开始显示
- `background-origin: content-box;`图片从内容区域开始显示

不设置时默认值为padding-box

![](http://img.mukewang.com/531003de0001166903660166.jpg)

### background-clip

四种情况

- `background-clip ： border-box;`图片从边框开始裁剪
- `background-clip ： padding-box;`图片从边框开始裁剪
- `background-clip ： content-box;`图片从边框开始裁剪
- `background-clip ： no-clip;`向外裁剪背景图片

不设置式的默认值是no-clip

![](http://img.mukewang.com/5310065d0001c95103660166.jpg)

### background-size

- `background-size: auto;`原始图片大小显示
- `background-size: 长度值 宽度值;`成对出现, 自定义图片的长度和宽度
- `background-size: 百分比;` 如果值是100%, 则图片大小和所在元素大小一样
- `background-size: cover;`图片缩放以填满所在的元素
- `background-size: contain;`背景图片等比缩放至某一边紧贴容器边缘为止。



	