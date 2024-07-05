
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
  * 也可以对一个Javascript对象进行遍历，此处未成功，不会用？？？---解决，如下person定义
  ```html
  return {
                    list: [1, 2, 3, 4, 5],
                    person: {
                        name: "Tom",
                        age: 17,
                        school: "ABC"
                    }
                }
  ```
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
  * 在form表单上使用@submit.prevent="addTask"，这里的submit.prevent如何理解？---见4.1.3,禁止默认的事件，仍然不太明白。
  * v-model和输入框绑定；
  * 添加任务的函数向列表里添加元素，随后显示在ul, li里；
  * 这里的splice函数，是删除元素？？如何理解？？
## 第三章 Vue 组件的属性和方法
* 3.1.1 属性基础
  * [vue3.1.1.html](vue3.1.1.html)
  * 使用组件实例直接获取属性；
  * 我们可以动态地向组件实例中添加属性，但是这种方式添加的属性不能被响应式系统跟踪，其变化无法同步到页面元素？？？如何理解
* 3.1.2 方法基础
  * [vue3.1.2.html](vue3.1.2.html)
  * 可以直接使用组件实例调用此方法；
  ```html
  let instance = Vue.createApp(App).mount("#Application")
  instance.add()
  ```
* 3.2.1 计算属性
  * [vue3.2.1.html](vue3.2.1.html)
  * 计算属性最终的值都是由存储属性通过逻辑计算得来的；
  * 影响其值的存储属性发生变化时，计算属性也会同步的更新；
* 3.2.2 使用计算属性还是函数
  * [vue3.2.2.html](vue3.2.2.html)
   * 函数，每次访问都会重新执行函数内的逻辑代码得到的结果；
* 3.2.3 计算属性的赋值
  * [vue3.2.3.html](vue3.2.3.html)
  * 计算属性默认是取值的方法，通常称这为get方法；
  * 也可以手工实现赋值的方法，set；
  * 类似于类的默认构造函数；
* 3.2.4 属性侦听器
  *  [vue3.2.4.html](vue3.2.4.html)
  * 有点类似于Ajax的一种机制，不太理解？？？
  ```html
  searchText(oldValue, newValue) {
      if (newValue.length > 10) {
          alert("文本太长了！")
      }
  }
  ```
* 3.3.1 手动实现一个限流函数
  * [vue3.3.1.html](vue3.3.1.html)
  * 页面中有一个按钮，通过按钮打印输出当前的时间，要求这个按钮的两次事件触发间隔不小于2秒；
* 3.3.2 使用Lodash库实现函数限流
  * [vue3.3.2.html](vue3.3.2.html)
  * 这个库貌似功能比较强大，先体验一下；
* 3.4.1 文本输入框
  * [vue3.4.1.html](vue3.4.1.html)
  * 文本输入框的双向绑定v-model；
* 3.4.2 多行文本输入框
  * [vue3.4.2.html](vue3.4.2.html)
  * 多行文本输入框
* 3.4.3 复选框和单选框
  * [vue3.4.3.html](vue3.4.3.html)
  * 复选框如果不指定value，则会显示布尔值；
  * 复选框需要指定一个list的变量，才能生效；
  * 单选框radio
* 3.4.4 选择列表
  * [vue3.4.4.html](vue3.4.4.html)
  * 选择列表，及多选列表（需要按住ctrl）；
* 3.4.5 两个常用的修饰符
  * [vue3.4.5.html](vue3.4.5.html)
  * 使用lazy修饰符，相当于懒加载，一直等到该文本框失去焦点时开始加载；trim是去首尾的空格符；
* 3.5.1 为HTML标签绑定class属性
  * [vue3.5.1.html](vue3.5.1.html)
  * <div :class="{blue:isBlue, red:isRed}">根据属性的值变化；
  * <div :class="style">可将其设置为一个vue组件中的数据对象；
  * <div :class="[redClass, fontClass]">还支持使用数组对象控制class属性；
* 3.5.2 绑定内联样式
  * [vue3.5.2.html](vue3.5.2.html)
  * 通过内置的style属性来设置样式，内联CSS属性用的是驼峰式，fontSize；
* 3.6.1 用户注册界面的练习
  * [vue3.6.1.html](vue3.6.1.html)
  * 部分渲染的练习；
  * 检查用户名，密码，邮箱；
  <img decoding="async" src="./images/3.6.1.png" width="20%">
## 第四章 处理用户交互
* 4.1.1 事件监听示例
  * [vue4.1.1.html](vue4.1.1.html)
  * 也可以直接将要执行的逻辑代码放入@click赋值的位置；
  ```html
  <button @click="this.count += 1">点击</button>
  ```
  * Event对象中会存储当前事件的很多信息，例如事件类型、鼠标位置、键盘按键情况等，这句如何理解？？？--4.2.1
* 4.1.2 多事件处理
  * [vue4.1.2.html](vue4.1.2.html)
  * 如果要进行多事件处理，在绑定事件时都要采用内联调用的方式绑定；
* 4.1.3 事件修饰符
  * [vue4.1.3.html](vue4.1.3.html)
  * 事件捕获：我们在页面上触发了一个单击事件时，事件首先会从父组件依次传递到子组件，这一过程通常被形象的称为事件捕获；
  * 事件冒泡：当事件传递到最上层的子组件时，其还会逆向地再进行一轮传递，从子组件 依次向下传递，这一过程称为事件冒泡；
  * 我们在vue使用@click的方式绑定事件时，默认监听的是DOM事件的冒泡阶段；
  * 理解事件的传递对处理页面用户的交互，至关重要；
  * 有时候我们不希望事件触发传递，这时候用到stop；
* 4.2.1 常用事件类型
  * [vue4.2.1.html](vue4.2.1.html)
  * 常用的交互事件有，点击，双击，表单的文本框的变化，焦点，鼠标按下，移动，右键等；
  * 表单的文本框的change，内容变化，是在按了回车之后起效；

  https://www.cnblogs.com/huanzi-qch/p/13915891.html