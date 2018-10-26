# CodeCollection
个人代码整理集合
==
阻止冒泡：
--
```JavaScript
var event = event || window.event;
if(event && event.stopPropagation)
{
  event.stopPropagation(); //w3c 标准
}
else
{
  event.cancelBubble = true; //ie678 iee浏览器
}
```
