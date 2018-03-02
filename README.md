# My learning trip of SVG

##L1: SVG概览
1. SVG是一种矢量图形格式。
2. SVG w3c v1.1标准：http://www.w3.org/TR/SVG11/
	浏览器支持情况： http://caniuse.com/#cats=SVG
  xmlns="http://www.w3.org/2000/svg"
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

##L4-1：SVG定位 世界 视窗 视野
###世界
  世界是无限的，用坐标轴定位。
###视窗
  参考窗口的定义：定义实际能看到的范围。width/height
###视野
  定义视窗和世界的相对位置。
  viewBox=“x y width heigh
  preserveAspectRatio="x(Min/Mid/Max)y(Min/Mid/Max)/none meet/slice"
  参数一：世界保持原缩放比例的对齐方式。none为按照viewBox的长宽比进行缩放，此时meet/slice值无效。

##L4-2：SVG颜色
###线性渐变：
<linearGradient id="grad1" x1="0" y1="0" x2="1" y2="1" gradientUnits="objectBoundingBox">
  <stop offset="0" stop-color="#3aa34c"/>
  <stop offset="0.7" stop-color="#d58d4b"/>
  <stop offset="1" stop-color="#d5554b"/>
</linearGradient>
  (x1,y1) - (x2,y2):起始点和结束点
  gradientUnits==> objectBoundingBox(default)/userSpaceOnUse:定位：自我坐标系/世界坐标系
  stop:关键点的位置和颜色

###径向渐变：
<radialGradient id="grad1" cx="0.5" cy="0.5" r="0.5" fx="0.8" fy="0.2" gradientUnits="objectBoundingBox">
  <stop offset="0" stop-color="#3aa34c"/>
  <stop offset="0.7" stop-color="#d58d4b"/>
  <stop offset="1" stop-color="#d5554b"/>
</radialGradient>
  用circle方式描述：cx,cy,r
  可以有聚光灯偏移效果：fx,fy

