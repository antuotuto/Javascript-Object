# 列表页面

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <div id="container"></div>
    <script>
            function Product() {
                // 产品名称
                this.name = '1'
                // 产品价格
                this.price = 2
                // 折扣
                this.zekou = '3'
                // 产品图片
                this.image = '4'
            }

            Product.prototype = {
                // 绑定
                bindDOM: function () {
                    var str = '';
                    str += '<div>'
                    str += '<p>' + this.name + '</p>'
                    str += '<span>' + this.price + '</span>'
                    str += '<i>' + this.zekou + '</i>'
                    str += '<h1>' + this.image + '</h1>'
                    str += '</div>'
                    return str;
                }
            }

            window.onload = function () {
                // 抽象 类和实例
                var product1 = new Product()
                product1.name = "王安安"
                var product2 = new Product()
                product2.name = "王一一"
                var product3 = new Product()
                product3.name = "王二二"
                var product4 = new Product()
                product4.name = "王三三"
                // 用数组保存数据
                var products = [product1, product2, product3, product4]
                // 针对单个对象整体进行编程
                var str = ''
                for (var i = 0; i < products.length; i++) {
                    str += products[i].bindDOM()
                }
                var container = document.getElementById('container')
                container.innerHTML = str;
            }
    </script>
</body>
</html>
```



