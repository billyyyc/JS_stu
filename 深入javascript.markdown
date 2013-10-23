返回值return
与函数传参相反（从函数给外界反馈的东西）
return如果是空的就是undefined

函数传参
arguments可变参，不定参
arguments是数组有length

style只能获取行间样式
currentStyle获取非行间样式（只兼容IE，高版本chrome也支持）
getComputerStyle（oDiv,随便放个东西）.width(IE7不支持)
处理兼容性方法：
if(oDiv.currentStyle)
{
oDiv.currentStyle….
}//IE
else
{
getComputerStyle….
}//FF
 总结：有它用它，没有它就用它'；
 为了方便封装成函数
 funciton getStyle(obj,name)
 {
 if(obj.currentStyle)
{
return obj.currentStyle[name];
}//IE
else
{
getComputerStyle(obj,false)[name];
}//FF
 }
这种方法只适合单一样式，不适合复合样式
复合样式，例如background，其实包含颜色图片等等，它不是一个明确的样式，没办法用getStyle，需要用backgroundColor这个单一样式。

数组
var a=[1,2,3];一般用这种形式
var a=new Array(1,2,3)

var a=[1,2,3,4,5,6,7,8]
arr.length=3;
效果是数组变成3个数，说明length可以获取的同时，也可以写！
push可以往尾部添加；pop是尾部删除
shift是删除头部，unshift往头部添加
splice
删除用法(起点位置,长度);
添加用法（起点，长度0，'a','b','c'）;
替换(2,2,'a','b')删除两个并替换成a，b

a.concat（b）数组a和数组b连接
join（分隔符）
 sort:调用一句arr.sort();就可以a-z，1-9排序
 sort只认识字符串！所以数字会出问题！
 arr.sort(function (n1,n2))
 {
 if(n1<n2)
 {return n1-n2;}(正数正序，负数反序)
 修正sort



















