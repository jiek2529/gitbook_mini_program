# create page创建页方法

## 创建步骤
1. Pages 下创建目录,eg: hello
+ 创建wxml, hello目录下创建：hi.wxml
+ hi.wxml里添加相应内容
+ 创建wxss, hello目录下创建wxml同文件名:hi.wxss
+ 创建js， hello目录下创建同名文件： hi.js
+ 根目录下app.json里把新建页引入进去，即可使用

注: 目录与页名可不同，但wxml wxss js的文件名一致为同一作用域。