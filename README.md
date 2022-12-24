
# study
循序渐进Vue.js 3 前端开发实战


# list  


* 1.5.1 第一个应用  
  * [vue1.5.1.html](vue1.5.1.html)
  * 使用vue实现的计数器应用比使用Javascript直接操作HTML元素方便的多；  
* 1.5.2 用户登录界面
  * [vue1.5.2.html](vue1.5.2.html)
  * 登录完成后，输入框需要隐藏，需要提供按钮让用户登出
  * v-model用来进行双向绑定，输入的方案和绑定的变量的值； 
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
