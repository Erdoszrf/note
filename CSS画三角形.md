# CSS画一个三角形出来
### 具体原理实现
- 一个加了边框的DIV
- DIV边框的划分规则
1.CSS中的边框划分如图所示，只有这样才能公平划分top，left，right，bottom四条边
```
div{
  width:100px;
  height:100px;
  background:skyblue;
  border:50px solid black;
  border-top-color:red;
  border-left-color:yellow;
  border-bottom-color:blue;
}
```
![](http://upload-images.jianshu.io/upload_images/9439180-cd9775c2f18a8ff5.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 如果我们把DIV的高和宽都设置为0，那么我们就得到了四个三角形
```
div{
  width:0;
  height:0;
  background:skyblue;
  border:50px solid black;
  border-top-color:red;
  border-left-color:yellow;
  border-bottom-color:blue;
}
```
![](http://upload-images.jianshu.io/upload_images/9439180-32f1325e763bf39e.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

3.如果把其中三条边的颜色设置为透明，那么我们就得到了一个标准的等腰三角形
```
div{
  width:00px;
  height:00px;
  border:50px solid black;
  border-top-color:transparent;
  border-left-color:transparent;
  border-right-color:transparent;
}
```
![](http://upload-images.jianshu.io/upload_images/9439180-b82ec8432292fe52.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4.通过把上边框的width设置为0px，得到这样的一个三角形
```
div{
  width:00px;
  height:00px;
  border:50px solid black;
  border-top-color:transparent;
  border-left-color:blue;
  border-right-color:transparent;
  border-bottom-color:transparent;
  border-top-width:0;
}
```
![](http://upload-images.jianshu.io/upload_images/9439180-5102871ca5e8f454.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 转载请注明来源
