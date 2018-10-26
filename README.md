# CodeCollection
## 个人代码整理集合
#### 阻止冒泡：
```JavaScript
var event = event || window.event;
if(event && event.stopPropagation)
{
  event.stopPropagation(); //w3c 标准
}
else
{
  event.cancelBubble = true; //ie678 ie浏览器
}
```
##### 封装可视区域宽度：
```JavaScript
function client(){
	if(window.inerWidth != null)//ie9 + 最新浏览器
	{
		return {
			width: window.innerWidth,
			height: window.innerHeight
		}
	}
	else if(document.compatMode == "CSS1Compat")//标准浏览器
	{
		return {
			width: document.documentElement.clientWidth,
			height: document.documentElement.clientHeight
		}
	}
	return { //怪异浏览器
		width: document.body.clientWidth,
		height: document.body.clientHeight
	}
}
//调用
console.log(client().width);
console.log(client().height);
```







