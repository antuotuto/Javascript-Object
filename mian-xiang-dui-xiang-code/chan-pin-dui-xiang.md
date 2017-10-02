# 产品对象

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>产品对象</title>
</head>
<body>
    <h2 id="title">如何去买一个手机</h2>
    <h3 id="des">奥术大师</h3>
    <div id="price"></div>
    <script>
        // 抽象
        // 产品对象 ： 名称 价格 描述
        function Product(){
            // 标题
            this.title = 'iphone8'
            // 价格
            this.price = 300
            // 图片
            this.images = []
            // 描述
            this.description = '最好的手机'
        }

        Product.prototype = {
            buy:function(){},
            getDetail:function(){},
            // 对代码分类进行管理
            bindDOM:function(){

            },
            bindEvents:function(){

            }
        }

        window.onload = function(){
            // 对象实例化
            var me = new Product();
            me.title = "王安安"
            me.price = 4399
            // 获取元素
            var title = document.getElementById('title')
            var price = document.getElementById('price')
            // 绑定元素
            title.innerHTML = me.title
            price.innerHTML = me.price
            // 绑定事件
        }
    </script>
</body>
</html>
```



