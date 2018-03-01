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
* 创建图形： document.createElementNS(SVG_NS ,tagName)
  SVG的定义是在自己的一个namespace下，不在html/window下
  const SVG_NS = 'http://www.w3.org/2000/svg'
* 添加图形： element.appendChild(childElement)
* 设置/获取属性：
element.setAttribute(name,value)
element.getAttribute(name)

##L4：SVG 世界 视窗 视野
###世界
  世界是无限的，用坐标轴定位。
###视窗
  参考窗口的定义：定义实际能看到的范围。width/height
###视野
  定义视窗和世界的相对位置。
  viewBox=“x y width height”
  preserveAspectRatio="x(Min/Mid/Max)y(Min/Mid/Max)/none meet/slice"
  参数一：世界保持原缩放比例的对齐方式。none为按照viewBox的长宽比进行缩放，此时meet/slice值无效。