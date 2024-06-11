https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/63

https://github.com/febobo/web-interview/issues/38

Set

1.成员不能重复
2.只有健值，没有健名，有点类似数组。

可以遍历，方法有add, delete,has

weakSet

1. 成员都是对象
2. 成员都是弱引用，随时可以消失。 可以用来保存DOM节点，不容易造成内存泄漏
3. 不能遍历，方法有add, delete,has

Map

1. 本质上是健值对的集合，类似集合
2. 可以遍历，方法很多，可以干跟各种数据格式转换

weakMap

1. 直接受对象作为健名（null除外），不接受其他类型的值作为健名
2. 健名所指向的对象，不计入垃圾回收机制
3. 不能遍历，方法同get,set,has,delete