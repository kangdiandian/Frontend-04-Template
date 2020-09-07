学习笔记
#搜索
###广度优先搜索使用的是队列的形式，深度优先搜索使用的是栈的形式
* 队列：遵循先进先出的原则
    所以pop(从数组末尾删除元素，删除数组最后一个元素)和unshift(从数组第一个位置添加元素)组合，push(从数组末端添加一个或者多个元素)和shift(删除数组第一个元素)组合，形成的就是队列的形式
* 栈：  遵循先进后出的原则
      所以pop和push组合，就是栈的形式


# LL算法构建AST（抽象语法树）
https://segmentfault.com/a/1190000016231512?utm_source=tag-newest

### 四则运算实例

#### 词法定义
* tokenNumber:
    * 1, 2, 3, 4, 5, 6, 7, 8, 9, 0
* operator: +, -, *, /之一
* whiteSpace: <SP>
* lineTerminator: <LF> <CR>

* <AdditiveExpression>组成情况
    <Number>
    |<MultiplicativeExpression><*><MultiplicativeExpression>
    |<MultiplicativeExpression></><MultiplicativeExpression>
    |<AdditiveExpression><+><MultiplicativeExpression>
    |<AdditiveExpression><-><MultiplicativeExpression>
