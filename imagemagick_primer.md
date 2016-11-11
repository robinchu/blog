# Imagemagic Primer

## 命令格式

```

// v5.5.7以前
command [options] input_image output_image
// v5.5.7以后
command [options] image1 [options] image2... [options] out_image

```
在v6.0以后的命令行严格按照参数的的先后顺序做操作

```
convert -size 40X20 xc:red xc:blue -append -rotate 90 append_image.gif

```
IMv6 command Syntax

```
command { [-setting]... "image" | -operation }... "output_image"

```
options前面通常有"-"或"+", 后者主要用来关闭设置或者重置默认状态

`许多API仅仅提供对多列表图像中的第一个图像实现操作，而命令行可以实现全部的操作`


## API

imagicmagic支持多种语言的扩展

C/C++/JAVA/GO/PHP/C#/Python/Perl/Lua

## Command line VS API

* 只有一个active image list
	API根据语言特性支持多列表互操作
* 访问像素数据困难
	查询图像属性读取或者更新一些特殊的区域
* 不支持条件执行
	根据图像的衍生属性更新或者区分图像，例如，根据图像背景色执行不同的操作
* 不支持循环执行
	循环执行对图像的操作

## 缩放(resize)

给一个图对它进行尺寸缩放，支持按比例缩放，填充蓝色， 或者图像伸缩拉伸
## 扣取(chop)
扣取图片

$ convert -size 40X20 xc:red xc:blue -rotate 90 -append a1.gif

## 拼接(append)

### +append左右拼接
### -append上下拼接

## 批量修改图片(mogrify)

## 剥离简介信息(strip)

## 生成缩略图(thumbnail)

```shell

$ convert -define jpeg:size=240x180 image.jpg -thumbnail 120x90 thumbs/image.gif
$ mogrify -path thumbs -format gif -define jpeg:size=240x180 -thumbnail 120x90 '*.jpg'

```

`注意：-thumbnail不能remove ICC color profiles, 所以，如果要删除ICC，需要添加 -strip`



