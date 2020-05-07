- 选择器；
1. ！imporant 权重：1，0，0，0，0
2. inline-style 权重：1，0，0，0；
3. id 权重：0，1，0，0；
4. class/伪类/属性选择器 权重： 0，0，1，0；（0，0，1，0*10==>0,0,11,0）
5. div（元素选择器）/伪元素 权重：0，0，0，1；
6. *（通配符）/ >(儿子)/ +相邻的兄弟 权重：0，0，0，0；
id权重大于class权重，从左到右开始比较。优先级从上往下依次排列
7. 伪元素：
div::before{
    content:
}
(插入div标签内容开始位置)
dix::after{
    content:
}
（插入div标签内容结束为位置）
div::first-line{
    color:
}
8. 伪类：
ul li:nth:child(2){
    color:
}
9. 属性选择器
[type="text"]{
    padding=4px;
}
