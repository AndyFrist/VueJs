Vue 学习笔记
el:挂在标签

#vue 组件的生命周期
beforeCreate  
created  data(), methods()等方法 得到执行 最早可以在此方法中访问接口

beforemount
mounted  

beforeUpdate
updated

destory

#常见指令有
v-text,v-html,v-on
v-show，v-if，v-bind，v-else（是否操纵dom元素是取决于前面使用的是v-show，还是v-if）
v-for，v-model

       
v-text 设置标签的文本值，注意v-text会全部覆盖标签内的内容
    使用插值表达式{{}}可以替代v-text

v-html  对于普通文本设置标签文本值和v-text没有任何区别，但是对于内容中是HTML结构那就会被解析出来

v-on  指令的作用是：为元素绑定事件，v-on:click，简写是@click。绑定的方法定义在methods属性中，方法的内部
    可以用this关键字访问到定义在打data的的数据

本地应用小案例：计数器

v-show 控制页面中的元素显示，v-show可以接受变量和表达式，写在表达式后面的内容最终都会解析为布尔值
    ，如果为true就显示，如果为false就隐藏。其本质是控制元素的display的值none。

v-if 根据表达式的真假，切换元素的显示和隐藏。（操纵dom元素，频繁的切换会影响性能，频繁切换的情况使用v-show）

v-bind  指令的作用是：为元素绑定属性。完整写法是v-bind：属性名，简写直接省略v-bind，：属性名

本地应用小案例：图片切换

v-for 指令的作用是根据数据生成列表，数组经常和v-for结合使用，语法是（item，index）in 数据    
    item和index可以结合其他指令一起使用，数组的变化是响应式的，会同步更新到页面列表上。

v-on补充之@keyup
    事件绑定的方法写成函数调用的形式，可以传入自定义参数，定义方法是需要定义形参来接收传入的实参，
     事件的后面跟上。修饰符可以对事件进行限制eg:@keyup.enter可以限制触发的按键为回车。修饰符有很多种。
     
v-model 获取和设置表单元素的值（双向绑定数据）
    绑定的数据会和表单元素相关联
    绑定的数据《==》表单元素的值
    
本地应用小案例：记事本    

##axios功能强大的网络请求库
引入<script src="https://umpkg.com/axios/dist/axios.min.js"></script>
axios.get(地址：？key=value&key=value).then(function(response){},function(err){})
axios.post(地址,{key=value,key=value}).then(function(response){},function(err){})
    
##vue常用的组件库
muse mint Vant eleme 这些库只能和Vue结合使用
##优秀的代码片段
MUI bootstrap  任何项目都可以使用，不局限于技术，可以用于react vue html5

##动画
1自定义动画
2第三方动画库animate.css
3钩子函数实现动画
