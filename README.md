# vue-dragging  

  vue-dragging，一个自己写的vue插件，可以给任意标签添加拖拽的功能
### Install
`yarn add vue-dragging `

### 演示(demo)
<a href="#">点击这里</a>

### How to use

普通html
```javascript
<script src="./vue.js"></script>
<script src="./vue-drag.min.js"></script>
```
是vue-drag.js不是vue-dragging.js

如果你的项目使用vue-cli搭建的 那么请这样使用:
```javascript
import Vue from 'vue'
import vueDrag from 'vue-dragging'
Vue.use(vueDrag)
```

在html当中添加标签，然后添加一个'v-drag'，假设为：
```html
<div class="demo">
  <div class="drag"  v-drag></div>
</div>
```
然后给要实现拖拽的标签添加css属性：
```css
.drag {
      position: absolute;
      top: 20px;
      left: 20px;
      width: 200px;
      height: 200px;
      background: green;
    }
```
### 进阶

加入了一个可拖拽区域和不可拖区域的方法，示例如下:

```html
        <div class="demo2" v-drag:dragable>
            <div id="dragable"><span>这里可以拖动</span></div>
            <div class="content"><span>这里不可以</span></div>
        </div>
```

`v-drag`后面的参数代表了可以拖拽的部分 而conten部分是不可拖拽的，这里class和id的名称可以自取，
但要注意可拖拽部分的id和`v-drag`后面的参数对应
