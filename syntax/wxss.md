# syntax of miniProgram wxss

weixin style sheets

兼容与适配界面reference: [官方文档](https://mp.weixin.qq.com/debug/wxadoc/dev/framework/view/wxss.html)

weixin style sheets
## 全局样式与局部样式
定义在 app.wxss 中的样式为全局样式，作用于每一个页面。在 page 的 wxss 文件中定义的样式为局部样式，只作用在对应的页面，并会覆盖 app.wxss 中相同的选择器。

**样式导入： @import "common.wxss";   //必须以分号结尾**

## 尺寸单位
rpx（responsive pixel）: 可以根据屏幕宽度进行自适应。规定屏幕宽为750rpx。如在 iPhone6 上，屏幕宽度为375px，共有750个物理像素，则750rpx = 375px = 750物理像素，1rpx = 0.5px = 1物理像素。

|设备 |rpx换算px (屏幕宽度/750) |px换算rpx (750/屏幕宽度) |
|--|--|--|
|iPhone5 | 1rpx = 0.42px | 1px = 2.34rpx |
|iPhone6 | 1rpx = 0.5px | 1px = 2rpx |
|iPhone6 Plus | 1rpx = 0.552px | 1px = 1.81rpx |

## 选择器
目前支持的选择器有：

|选择器|样例|样例描述|
|--|--|--|
|.class|.intro|选择所有拥有 class="intro" 的组件|
|#id|#firstname|选择拥有 id="firstname" 的组件|
|element|view|选择所有 view 组件|
|element, element|view, checkbox|选择所有文档的 view 组件和所有的 checkbox 组件|
|::after|view::after|在 view 组件后边插入内容|
|::before|view::before|在 view 组件前边插入内容|