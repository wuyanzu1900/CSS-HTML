## 格式化上下文
koa:ctx === context
token:泛指
上下文的概念
```js
let a = 123
function foo(){
    return a + 1;
}
foo()
```
## BFC
block-formation-context
隔离的容器

## 新建一个BFC
- float
- absolute
- display: inline-blocks || table-cell || table-caption
- overflow 不为visiable
- 根元素默认新建 BFC



## flex布局
react-native 只支持flex，RN已经证明了知用flex是可以很好地完成布局


## float
一开始设计之初用来文字环绕


后来float用来做布局，float清除
clear:both(left,right)



## BFC规则
- 盒子在垂直方向上，从上往下布局
- 垂直方向上的距离由margin决定，同一个BFC之内，垂直方向上block-formation-context margin会折叠(留白,够了就行)

- 由于有float元素，一个盒子大小可能会缩小，除非它新建BFC(overfloat清除浮动)
- BFC区域不会与float重叠(左侧固定，右侧自适应)


## normal flow
normal flow:
position:
float:本意用来做文字环绕，几行几列
flex: