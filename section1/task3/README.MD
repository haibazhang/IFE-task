

### 纯使用position来布局：

* 思路：static是默认的position。absolute没有设定位置时与static一致。absolute是相对最近的absolute父视图，如果没有这样的父视图，则相对body而言。因为left/mid/right可能需要设为absolute，所以main应当先设为absolute，并且四个方向都设为0。接下来，left视图不需要设置。mid视图需要设为absolute，因为被换行了，所以top需要改变。（想象下原来static的位置）我们发现mid是与left重叠，其实这里的“技巧”就是设定margin。right设为absolute后需要设定right和top（想象下原来static的位置）。当我们设置left中子视图（图片）竖直方向居中时，有一种方法是使用absolute，所以需要将left设为absolute。
* 小结：position结合盒子模型来做布局，设定参数会有比较高的耦合。


### 纯使用float来布局：


### 纯使用inline-block来布局：



### Tips:
* [How (Not) To Vertically Center Content](http://phrogz.net/CSS/vertical-align/index.html)
