# My learning trip of SVG

##L1: SVG概览
1. SVG是一种矢量图形格式。
2. SVG w3c v1.1标准：http://www.w3.org/TR/SVG11/
	浏览器支持情况： http://caniuse.com/#cats=SVG
3. SVG可以：
	- 在浏览器直接打开
	- 在HTML中使用<img>标签引用（embed、object、iframe）
	- 在HTML中使用<svg>标签
	- 作为CSS背景

##L2: SVG基本属性

##L3：SVG编译器DEMO
###SVG基本API
* 创建图形： document.createElementNS(ns ,tagName)
  SVG的定义是在自己的一个namespace下，不在html/window下
* 添加图形： element.appendChild(childElement)
* 设置/获取属性：
element.setAttribute(name,value)
element.getAttribute(name)