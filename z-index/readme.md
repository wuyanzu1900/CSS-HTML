## 
我们的一个网页是沿着一条Z轴排开的(类似ps之中的图层)

## 层叠上下文形成 z-index 调整的就是这个层叠上下文
1. position 不为 static
2. filter transform perspective 不为none
3. willchange

## layers
共同点：都是z-轴 顺序
**transform:translate3d**
**will-change**
perspective
backface-visibility 为hidden
css3里面的animation动画开始的时候


## 
js->relayout->repaint->composite(合成) -GPU


## 提升layers的好处
- 当前这个layers的变化不会影响其他layers
- 对于transform，opacity 产生了变化，不会经过relayout repaint 跳到 composite

## 
video
有 3D transform
backface-visibility 为 hidden
对 opacity、transform、fliter、backdropfilter 应用了 animation 或者 transition（需要是 active 的 animation 或者 transition，当 animation 或者 transition 效果未开始或结束后，提升合成层也会失效）
will-change 设置为 opacity、transform、top、left、bottom、right（其中 top、left 等需要设置明确的定位属性，如 relative 等）
