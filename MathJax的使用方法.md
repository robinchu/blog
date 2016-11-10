目前，在网页或者MarkDown中引入数学公式的一种方法是在网页中引入MathJax脚本，下面介绍一下MathJax的使用方法。
<a href="http://www.littlenote.cn/wp-content/uploads/2016/01/mathjax.jpg" rel="attachment wp-att-60"><img class="alignnone size-full wp-image-60" src="http://www.littlenote.cn/wp-content/uploads/2016/01/mathjax.jpg" alt="mathjax" width="679" height="450" /></a>
### 引入脚本
在MathJax的官网上提供了完整的MathJax服务，资源连接是[https://cdn.mathjax.org/mathjax/latest/MathJax.js](https://cdn.mathjax.org/mathjax/latest/MathJax.js),但是，由于服务器在国外，可能会被屏蔽。这里我们自己搭建了MathJax服务，地址是[http://www.littlenote.cn/mathjax/MathJax.js](http://www.littlenote.cn/mathjax/MathJax.js)。下面是引入方法:
*注意：下面的引入方法使用的是我们自己搭建的服务器*
```html
<script type="text/javascript" src="http://www.littlenote.cn/mathjax/MathJax.js?config=TeX-AMS-MML_SVG">
</script>
```

### 引入配置脚本

```html
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}});
</script>
```

### 完整例程
<a href="http://www.littlenote.cn/wp-content/uploads/2016/01/mathjax_test.jpg" rel="attachment wp-att-89"><img src="http://www.littlenote.cn/wp-content/uploads/2016/01/mathjax_test.jpg" alt="mathjax_test" width="556" height="246" class="alignnone size-full wp-image-89" /></a>
