- DOM/document 文档就是网页， js内存里，则是文档对象模型
js -> html 转化
DOM JS 数据结构tree appendchild 组成一棵树
ul>li>textnode
document.createElement('tag') 标签节点
document.createTextNode('babab') 文本节点

哪怕是文字，都是节点，都是对象 
前端js，html，js，css中js是王者，js可以操控html，js，这些API叫做DOM API
document.createElement('div')
document.appendchild()
document.createTextNode() 面向API编程

- 面向商务编程
this.state.liked true/false html 更新
1.分布
    动态的讲Like button 添加到页面上
    likeButton class 方便复用
    既要用 html 来快速完成DOM ，又要能添加事件
    1. 要dom对象
    2.要innerHTML

js中的this指向，在每个函数都有this  this是个指针
具体指向谁  由其调用方式决定
1. 作为对象的方法调用，this指向对象本身
2. 作为事件函数，this指向事件发生的元素
    bind 可以强行去绑定函数内部的thia指向谁
    call立即执行

- 封装 class 复用
    构造函数 constructor 申明属性 this.state
    render() 渲染到页面上
    changeLikeText()

    class LikeButton{
         constructor(){

    }
    render(){

    }
    changeLikeText(){}
    }


createDOMFromString 写到外面
代码思维的顶级
createDOMFromString不该属于LikeButton类 属于独立的
util方法 其他地方也能用
   

