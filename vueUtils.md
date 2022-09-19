Vue

1、路由传递props数据

函数写法：

```js
props:($route) => ({k:$route.params.k,q:$route.query.q})
```

 2、重写push、replace方法

重写vueRouter构造函数的方法时，要用 call方法修改其上下文this 

3、动态添加背景颜色

css使用hover    js使用:class="{cur:currentIndex==index}"

:style="{display:currentIndex==index?'block':'none'}"

4、因为事件触发非常频繁，每一次触发回调函数都要去执行。而回调函数内部有计算，很可能出现浏览器卡顿现象

防抖：快速触发，只执行最后一次

节流：把频发触发变成少量触发

插件lodash 或者闭包＋延时器

5、三级联动 点击事件跳转路由传参 使用事件委派+自定义属性dataset

6、公共组件数据请求可以放在根组件中mounted中调用 （性能优化）

7、mockjs

8、$nextTick 经常和插件一起使用（保证页面结构一定是有的）

9、函数默认参数 fun（params = {}）{}

10、合并参数 `Object.assign(params,this.$route.query,this.​$route.params)`

11、搜索页 查询修改页面数据处理 监听路由变化 `watch：{$route(newV,oldV){}}`

12、发请求传参数如果参数可有可无，this.params = undefined 代替this.params = '' "这样这个字段不会带给服务器

13、全局事件总线：`this.$bus.​$emit（"clear"） this.$bus.$on("clear",()`=>{})

14、数组去重的方法 字符串split方法 数组splice方法

15、路由跳转传参如果是复杂数据如对象 通过浏览器会话存储sessionStorage传递JSON数据

16、临时身份uuid 使用插件uuid生成 通过本地存储存储添加到请求拦截器请求头当中 config.headers.xxx

17、全选判断使用arr.every()方法

18、计数器+- 改变数量 要加节流 防止用户点击过快

19、获取多个异步操作的执行结果 Promise.all

20、去除表单默认行为.prevent

21、vuex不是持久化存储 页面刷新数据就没了

22、数组find方法 查找数组中符合条件的元素

23、把API文件里所有请求函数 在Main.js而入口函数注册 Vue.prototype.$API = API

24、组件库：React(Vue):antd[PC] antd-mobile[mobile]

Vue: ElementUI[PC] vant[mobile]

25、路由守卫（全局守卫、路由独享守卫、组件内守卫）控制页面跳转权限

26、图片懒加载 插件vue-lazyload

27、自定义Vue插件（手写一个）

28、xshell操作 配置nginx反向代理