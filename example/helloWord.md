 # Hello word

 ## 演示效果

引用vue，input输入框输入的数据同步到p标签中。

![](./assets/2018-08-04-14-55-33.png)
 
 ## 实现
 ```html
<!-- 引用vue后续将不会在说明vue的引用，生产环境中请使用最小版 -->
<script src="../assets/js/vue.js"></script>

<div id="app">
    <p> {{message}}</p>
    <p> {{message+11}}</p>      
    <p><input type="text" v-model="message"></p>
</div>
<script>
    var vm = new Vue({
        el:'#app',
           data:{
               message: 'hello word.'
        }
    })    
</script>
 ```
 
 ## [完整代码](helloWord.html)
