#   记录平时总结的东西

##### 结构目录如下
* lisa.github.io/
	* build_code/ (gulp build后的文件在这里)
	* css/	(compass生成的css文件)
	* js/	(文件中使用到的js)
	* scss/	(sass文件存放目录)
	  * common/ (公用scss例如reset等)
	  	* [various .scss]
	  * css3/ (一些css3属性定义)
	  * mixin/ (自定义mixin例如animation等)
	  	* [various .scss]
	  * webkit/ (单独webkit的效果)
	  * [various .scss]
	* tmpl/	
	  * [various.html]  (源html静态文件)
	* images/    ( 项目中用到的所以图片包括小icon切片)
	* wiki/ (一些文案的记录)
	* node_modules/ (gulp package folder)
	* gulpfile.js
	* package.json (will be added when gulp is installed via CLI)
	* readme.md

##### css3属性定义 

>  直接   @import "css3/css3" 就可以使用

1. [animation](https://github.com/lisaRao/lisa.github.io/blob/master/sass/animation_demo.scss)
   使用方法 如下 `一定注意需要定义$flag 变量值[ true|false]`
   

		@charset "utf-8";

		$flag: true;

		@import "css3/css3";
		@include keyframes(moveX){
			0%, 100% {
				background-color: red;  
				transform:translateX(50px); 
			} 
			50% {
				background-color: blue;
				transform:translateX(100px); 
			}
		}

		@include keyframes(fadeOutTop){
			0% {
				transform: tanslateY(0);
			}
			100% {
				transform: translateY(-100%);
			}
		}

		.animation {
			width: 50px;
			height: 50px;
			background-color: green;
			@include animation(moveX 800ms 2s both,fadeOutTop .3s forwards);    
		}



|
+- app
|   +- index.html
|   +- assets
|       +- js
|          +- foo.js
|          +- bar.js
+- dist
|   +- index.html
|   +- js
|       +- optimized.js
|   +- style.css

