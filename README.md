# Helen
//随机数
function randomNum(min, max) {
	return parseInt(Math.random() * (max - min) + min);
}
//随机颜色
function randomColor() {
	var r = parseInt(Math.random() * 256);
	var g = parseInt(Math.random() * 256);
	var b = parseInt(Math.random() * 256);

	var colorString = "rgb(" + r + "," + g + "," + b + ")";
	return colorString;
}
//获取内部外部样式表中的样式属性的属性值
// obj--- 元素节点
// name----属性名
function getStyle(obj, name){
	if (obj.currentStyle) {
		return obj.currentStyle[name];
	}else{
		return window.getComputedStyle(obj,null)[name];
	}
}

//设置元素样式属性
//obj--元素节点
//name--样式属性名
//value--样式属性值
function setStyle(obj, name, value) {
	obj.style[name] = value;
}


//获取宽度
function $w() {
	return document.documentElement.clientWidth || document.body.clientWidth || window.innerWidth;
}

//获取高度
function $h() {
	return document.documentElement.clientHeight || document.body.clientHeight || window.innerHeight;
}
