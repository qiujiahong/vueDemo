# v-on

## 演示效果

vue控制按钮事件。 

* 单击，``@click="fun"``
* 按enter,``@keyup.enter="onEnter"``
* 按F2,``@keyup.113="onF2"``，更多键值，参考该[网站](https://www.cnblogs.com/qtiger/p/5796001.html)

> 绑定组合键？

 
 ## 实现
 ```html
    <div id="app">
        <p> {{a}}</p>
        <p>
            <button v-on:click="jia">+1</button>
            <button @click="jian">-1</button>
        </p>
        <p>
                <input type="text" @keyup.enter="onEnter" v-model='b' ></input>
                <input type="text" @keyup.113="onF2" v-model='b' ></input>
                
        </p>
    </div>
    <script>
        var vm = new Vue({
            el: '#app',
            data: {
                a: 10,
                b: 0,
            },
            methods: {
                jia: function () {
                    this.a++;
                },
                jian: function(){
                    this.a--;
                },
                onEnter: function(){
                    if(isNaN(this.a))
                    {
                        this.a='0';
                    }
                    this.a = parseInt(this.a) + parseInt(this.b);
                },
                onF2: function(){
                    this.a = parseInt(this.a) - parseInt(this.b);
                }
            }
        })    
    </script>
 ```
 
 ## [完整代码](v-on.html)


 