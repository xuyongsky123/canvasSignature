<h2>canvasSignature简介&nbsp;&nbsp;&nbsp;&nbsp;<a href="http://www.shdnfw.com/plugin/canvasSignature/demo.html">手写签名（电子签名canvasSignature.js)使用示例</a></h2>
<p>canvasSignature是基于html5 canvas及jquery实现手写签名（电子签名）功能的js组件</p>

<hr/>

<h3>1、开始工作：</h3>
<p>
  需要最先引入jquery (Bootstrap中文网开源项目免费 CDN 服务)：
</p>
```html
<script type="text/javascript" src="//cdn.bootcss.com/jquery/1.9.1/jquery.min.js"></script>
```
<p>
  我们需要在页面中引入关键js：
</p>
```html
<script type="text/javascript" src="....../canvasSignature.js"></script>
```

<h3>2、使用：</h3>
<h4>html：</h4>
<p>
  （html canvas签名框准备，id为test可自定义）
</p>
```html
<canvas id="test" width="500" height="300">
    您的浏览器当前不支持canvas画布，请更换别的浏览器进行签名操作
</canvas>
```

<h4>js（相应的方法调用）：</h4>
<p>
  初始化签名样式（这里仅支持一个签名，如需多个签名框需改写组件）
</p>
```javascript
$('#test').canvasSignature({
    fillStyle:'transparent',	//生成图片背景色，默认为透明
    lineWidth:10,	//笔画粗细（尺寸），默认为四像素粗细
    strokeStyle:'red'	//笔画颜色，默认为黑色
});
```
<p>
  清除重写
</p>
```javascript
$('#test').clearSignature();
```
<p>
  生成图片（生成图片格式base64包括：jpg、png格式）
</p>
```javascript
$('#test').createSignature('png');
```


<h3>3、方法说明：</h3>
<table>
  <tr>
    <th>方法名</th>
    <th>参数</th>
    <th>说明</th>
  </tr>
  <tr>
    <td>canvasSignature</td>
    <td>
      fillStyle：生成图片背景色，默认为透明(字符串)<br/>
      lineWidth：笔画粗细（尺寸），默认为四像素粗细(数字)<br/>
      strokeStyle：笔画颜色，默认为黑色(字符串)<br/>
      注意：参数是以对象形式传入，如:<pre>$('#test').canvasSignature({
    fillStyle:'transparent',	//生成图片背景色，默认为透明
    lineWidth:10,	//笔画粗细（尺寸），默认为四像素粗细
    strokeStyle:'red'	//笔画颜色，默认为黑色
});</pre>
    </td>
    <td>初始化签名框（主要）</td>
  </tr>
  <tr>
    <td>clearSignature</td>
    <td>
      无
    </td>
    <td>清除签名</td>
  </tr>
  <tr>
    <td>createSignature</td>
    <td>
      生成图片格式base64包括：jpg、png格式(默认可不填)(字符串)<br/>
      注意：参数是以字符串形式传入，如:<pre>$('#signName').createSignature('png');</pre>
    </td>
    <td>生成图片</td>
  </tr>
</table>

<h3>4、兼容性：</h3>
<p>
  兼容IE9及以上浏览器（支持canvas标签功能的浏览器）
</p>
