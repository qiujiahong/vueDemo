# v-text

## 演示效果

* v-text演示
 
 ## 实现
 ```html
    <div id="app">
        <span>{{message}}</span> = <span v-text="message"></span>
        <hr>
        <span>{{messageItem}}</span> = <span v-html="messageItem"></span>
        
    </div>
    <script>
        var vm = new Vue({
            el:'#app',
            data:{
                message: 'hello word.',
                messageItem: '<h1>title</h1>'
            }
        })    
    </script>
 ```
 
 ## [完整代码](v-text.html)
