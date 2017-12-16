## 思路
1. 用一个div，利用css的线性渐变实现上下分割的黑白

![](http://upload-images.jianshu.io/upload_images/9439180-c0135b4007e0ea90.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
.taiji{
  border:1px solid black;
  width:400px;
  height:400px;
  border-radius:50%;
  background: linear-gradient(to bottom, #ffffff 50%,#000000 50%);
}
```
2.利用**before**和**after**伪类，给太极加上两个半圆

![](http://upload-images.jianshu.io/upload_images/9439180-d934faebc9dc1c04.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
.taiji::before{
  content:'';
  background:black;
  position:absolute;
  width:200px;
  height:200px;
  border-radius:50%;
  left:0;
  top:25%;
}
.taiji::after{
  content:'';
  background:white;
  position:absolute;
  width:200px;
  height:200px;
  border-radius:50%;
  left:50%;
  top:25%;
}
```
3.现在我们需要实现最中心的两个小圆，但是如果利用div实现就违背了我们的初衷，所以我们可以优化上面的css，使用边框来让before和after实现效果

![](http://upload-images.jianshu.io/upload_images/9439180-4b637adf72a620e4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```
.taiji::before{
  content:'';
  background:white;
  border:75px solid black;
  position:absolute;
  width:50px;
  height:50px;
  border-radius:50%;
  left:0;
  top:25%;
}
.taiji::after{
  content:'';
  background:black;
  border:75px solid white;
  position:absolute;
  width:50px;
  height:50px;
  border-radius:50%;
  left:50%;
  top:25%;
} 
```

