
# study
《循序渐进Vue.js 3 前端开发实战》



## 第一章 从前端基础到Vue.js 3
* 1.5.1 第一个应用  
  * [vue1.5.1.html](vue1.5.1.html)
  * 使用vue实现的计数器应用比使用Javascript直接操作HTML元素方便的多；  
* 1.5.2 用户登录界面
  * [vue1.5.2.html](vue1.5.2.html)
  * 登录完成后，输入框需要隐藏，需要提供按钮让用户登出
  * v-model用来进行双向绑定，输入的方案和绑定的变量的值； 
## 第二章 Vue 模板应用  
* 2.1.1 了解模板插值
  * [vue2.1.1.html](vue2.1.1.html)
  * 了解插值一次的v-once，HTML插值v-html，以及属性值绑定v-bind；
* 2.1.2 了解模板指令
  * [vue2.1.2.html](vue2.1.2.html)
  * 了解指令增加参数，指令修饰符，v-bind, v-on的简写: @；
* 2.2.1 使用v-if指令进行条件渲染
  * [vue2.2.1.html](vue2.2.1.html)
  * 条件渲染的if, else之间不能有其它语句，否则失效；但是vs code也没有报错；
  * 条件渲染可实现多个逻辑分支；
  * 可直接渲染到div上，也可以渲染到专用的template上；
    * 问题注意在渲染的时候这个绑定的生效范围.mount("#Application")；
* 2.2.2 使用v-show指令进行条件渲染
  * [vue2.2.2.html](vue2.2.2.html)
  * 也可以使用v-show条件渲染，看上去的效果是一样的；
  * v-show不能用else，v-if在条件为假的时候不会被渲染；v-show在条件为假的时候也会被渲染，只不过是通过display:none的方式不显示出来；
  * v-if具有更高的切换性能消耗；v-show具有更高的初始渲染性能消耗；
  ```html
  <h1 style="display: none;">v-show的标题在这里</h1>
  ```
* 2.3.1 v-for指令的使用方法
  * [vue2.3.1.html](vue2.3.1.html)
  * v-for可针对列表，也可针对对象列表，可获取到索引；
  * 也可以对一个Javascript对象进行遍历，此处未成功，不会用？？？
* 2.3.2 v-for指令的高级用法
  * [vue2.3.2.html](vue2.3.2.html)
  * 对列表可进行一系列操作，排序，反序，追加，删除元素等；
  * 可重新定义一个对列表的处理函数，而遍历这个函数的结果；
  ```html
  handle(l) {
      return l.filter(obj => obj.name == "Mary")
  }
  ```
* 2.4.1 实现待办任务的列表应用
  * [vue2.4.1.html](vue2.4.1.html)
  * 在form表单上使用@submit.prevent="addTask"，这里的submit.prevent如何理解？
  * v-model和输入框绑定；
  * 添加任务的函数向列表里添加元素，随后显示在ul, li里；
  * 这里的splice函数，是删除元素？？如何理解？？
## 第三章 Vue 组件的属性和方法
* 3.1.1 属性基础
  * 