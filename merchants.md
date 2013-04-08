# 商户：merchants
***
##创建商户

##请求
###POST /merchants

```json
{
  "name": "卡罗酒吧",
  "fullName": "南京卡罗酒吧",
  "telephone": "02551234567",
  "email": "kaluojiuba@qq.com",
  "address": "江宁区胜太路",
  "status": ["open", "suspend", "closed"]
}
```
###必要项目
* `name`  
* `fullName`  

###默认项目
* `status` - "open"


##响应
###`201` - 添加成功
```json
{
  "id": "4545a454e454c4d45",
  "name": "卡罗酒吧",
  "fullName": "南京卡罗酒吧",
  "address": "江宁区胜太路",
  "telephone": "02551234567",
  "zip": "",
  "email": "kaluojiuba@qq.com",
  "userID": "e8a69acd47baf94c",
  "status": "open",
  "createdAt": "1365402743500"
}
```
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主更新商户信息

##请求
###PUT /merchants/:id

```json
{
  "name": "卡罗酒吧",
  "fullName": "南京卡罗酒吧",
  "address": "江宁区胜太路",
  "telephone": "02551234567",
  "zip": "",
  "email": "kaluojiuba@qq.com",
  "status": "open"
}
```

##响应
###`200` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
