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
        function Product(){
            this.title = 'iphone8'
            this.price = 300
            this.images = []
            this.description = '最好的手机'
        }
        
        Product.prototype = {
            buy:function(){

            },
            getDetail:function(){
            
            }
        }

        window.onload = function(){
            var me = new Product();
            me.title = "王安安"
            me.price = 4399
            var title = document.getElementById('title')
            var price = document.getElementById('price')
            title.innerHTML = me.title
            price.innerHTML = me.price
        }

    </script>
</body>
</html>
```



