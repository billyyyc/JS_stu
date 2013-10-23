ECMAScript:翻译、解释器
DOM:Document Object Model赋予JS操作HTML的能力
BOM:Browser Object Model跟浏览器有关，都称BOM操作


变量类型
typeof(对象类型)

12;'adsfa';true;function;document
number/string/boolean/function/object;undefined
undefined:1、真的没有定义；2、定义了但是没有赋值

oTxt.value=12,但是类型是字符串

类型转换：
1、强制类型转换
parseInt()与NaN
可以将字符串转为num(parseInt是用来转换整数的，parseFloat用来转换小数，不确定是否是小数，就用第二个)
从左到右扫描，只会提取数字，碰到非数字就停止，
从头开始都没有数字就出现NaN‘非数字’
任何数和NaN想加的话 都是NaN
NaN和NaN是不相等的
isNaN（对象）：判断对象是不是NaN
2、隐式类型转换
==（左右不一的时候，先会转换类型然后比较）
===不转换，直接比
a-b 会把a/b转换成num后相减，因为减号只有一个功能就是相减


变量的作用域
局部变量（只能在定义它的函数里面作用）
全局变量（定义在所有函数之外）
闭包：子函数可以使用父函数的变量

命名规范（函数类型才需要，变量不用）
匈牙利命名法：1、类型前缀2、首字母大写
oTxt aLi
数组就用a开头、对象用o、整数用i


运算符
算术：+、-、*、/、%（求模）
赋值：=、+=、-=、/=、%=
	++只能一次加1
	+=等于=+
	i+=2等于i=i+2
关系：<、>、<=、>=、==、===、!=
逻辑：&&与、||或、！否(取反)
优先级：括号


判断
1、
if(){}
else if(){}
else{}
2、
switch(变量)
{
	case值1：
	语句1；
	case值2：
	语句2；
	。。。
	default：
	默认语句；
}
?:   三元运算符，作用等于if、else
条件?语句1:语句2；

break中断循环
continue中断本次循环

什么是true（有东西）：非零的数字、非空字符串、非空对象
什么是false（没有东西）：零、空字符串、空对象null、undefined

Json(没有length)
json{a:12,b:321,c:3212}
json.a
json.b++
json['c']

数组用for in循环一般只给json用这种循环
for(var i in json){}
