# 用户 - User
***
## 用户注册
注册一个新用户

##请求
###POST /users

```json
{
  "displayName": "张业主",
  "phone": "1891234578",
  "idcard": "320103197901011234",
  "male": true,
  "birthday": "19790101",
  "email": "18912345678@189.cn",
  "roles": [
    "owner",
    "user",
    "administrator"
  ],
  "username": "18912345678",
  "password": "123456"
}
```
###必要项目
* `username`
* `passowrd`
* `phone` - 与 **email** 有其中之一就可以
* `email` - 与 __phone__ 有其中之一就可以

###默认项目
* `roles` - ["user"]
* `male` - true

##响应

###`201` - 创建成功
```json
{
  "created_id": "e8a69acd47baf94c"
}
```


###`400` - 请求参数错误
###`409` - 用作用户名的电话号码或电子邮件已经被注册过。
***


## 用户登录
##请求
###POST /users/login

```json
{
  "username": "18912345678",
  "password": "123456"
}
```
###必要项目
* `username`
* `password`

##响应
###`200` - 登录成功
###`401` - 登录失败
***


## 用户登出
##请求
###POST /users/logout

##响应
###`200` - 登出成功
***


## 更新用户信息
##请求
###PUT /users/:id

```json
{
  "password": "123456",
  "displayName": "张业主",
  "phone": "1891234578",
  "idcard": "320103197901011234",
  "male": true,
  "birthday": "19790101",
  "email": "18912345678@189.cn",
  "roles": ["owner", "user", "administrator"]
}
```

##响应
###`200` - 更新成功
###`400` - 参数错误
###`401` - 权限不够
###`409` - 请求冲突
