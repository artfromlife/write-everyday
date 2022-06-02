# 像素 物理像素 逻辑像素 分辨率

## 像素
```angular2html
像素是没有大小的， 像素本身就是一个单位， 可以理解为一个格子

屏幕的尺寸是英寸为单位的 ， 这个量的是屏幕的对角线的长度 1英寸 = 2.54厘米

根据尺寸 和 分辨率 确定你的 1 像素 到底是多大
```
图片放大缩小 占据的实际的格子数目也会相应的增多减少

## 设备像素
```angular2html
device pixels 设备像素， 也就是物理像素（硬件生产方面的） dp


```
### 逻辑像素
```angular2html
device independent pixels (设备独立像素) dip

```
### 设备像素比
```angular2html
devicePixelRatio = dp / dip
浏览器查看 dpr window.devicePixelRatio
告诉浏览器应使用多少屏幕实际像素来绘制单个 CSS 像素
```
