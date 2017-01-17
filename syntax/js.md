# syntax of miniProgram js

## 逻辑层(App Service)

小程序开发框架的逻辑层是由JavaScript编写。

小程序的js语法遵循：

```
用于跨文件调用函数
引用： var show = require('../../utils/show.js')
调用： show.toast('hello')
```

## 调用回调方式

```
var api = require('../../utils/api.js')
api.oauth({
    username: 'jiek',
    password: '123456'
    success: function(data) {
        show.toast(data.access_token) //成功时toast出token
    }，
    fail: funcation(reason) {
        show.toast(reason.data) //失败时的数据toast
    }
    ...
})
```

## 定义方式 #utils/api.js

```
function oauth(args) {
    var username=args.username, password=args.password, callback=args.success, fail=args.fail

    wx.request({
        ...
        success: function (resource) {
            callback(resource.data)
        }
        ...
    })
}

module.exports = { //此文件对外开放函数申明外
    oauth: oauth,
}
```
