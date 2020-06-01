# live2d

> 在前端页面中使用live2D

## 普通静态页中

# 首先先下载L2Dwidget.min.js（在html文件夹的js中）

# 在html中引用该js

# 初始化
```javascript
L2Dwidget.init({"display": {
	"superSample": 2,
	"width": 200,
	"height": 400,
		"position": "right",
		"hOffset": 0,
	"vOffset": 0
	}
});
```

## vue中使用

# 首先下载文件资源（可以直接下载我的，在static中）

# 在根目录中的index.html中引入js

```javascript
<script src="/static/live2dw/lib/L2Dwidget.min.js"></script>
```

# 在App.vue中初始化
```javascript
created(){
	setTimeout(()=>{
      window.L2Dwidget.init({
      pluginRootPath: 'live2dw/',
      pluginJsPath: 'lib/',
      pluginModelPath: 'live2d-widget-model-z16/assets/',
      tagMode: false,
      debug: false,
      model: { jsonPath: '../static/live2dw/live2d-widget-model-shizuku/assets/shizuku.model.json' },//资源文件
      display: { position: 'right', width: 200, height: 400 },//尺寸与位置
      mobile: { show: true },//跟随鼠标
      log: true
    })
    },1000)
}
```