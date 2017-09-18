# mobileHack
移动端踩坑

####移动端1px解决方案

因为devicePixelRatio的关系，移动端设置样式border-width:1px 实际上会显示2px的边框。
针对这个问题，业内也有很多解决方案，border-image，伪类之类的，实现起来比较繁琐也灵活性不够。
其实，在大部分情况下我们只要做如下的设置即可

```
@media (-webkit-min-device-pixel-ratio: 2) {
    .one-pixel-border {
        border-width: 0.5px;
    }
}
```
半像素处理。iOS8.0以上即可支持。

