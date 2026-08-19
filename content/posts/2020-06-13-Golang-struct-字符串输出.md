+++
title = 'Golang学习记录'
description = 'struct 字符串输出'
date = '2020-06-13'
tags = ['Go', 'struct']
showToc = true
+++


通过阅读 image.Point 源码学习到，定义结构体同时可以根据结构体设置接口如 String() ，会在输出时调用这个方法，改变输出结果。

```` go

type point struct {
	X int
	Y int
}

func (p point) String() string {
	return "|" + strconv.Itoa(p.X) + "," + strconv.Itoa(p.Y) + "|"
}

var t [2]point
var t2 = [...]point{ {X:0,Y:0} }
fmt.Println(t)
fmt.Println(t2)

````
#### 输出
````
 [|0,0| |0,0|]
 [|0,0|]
````
