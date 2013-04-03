# 商户：merchants
***
##业主添加新雇员

##请求
###POST /merchants

```json
{
  "username": "15155522244",
  "shopID": "154d454a578e475",
  "status": ["active", "leaved", "suspend"]
}
```
###必要项目
* `shopID`  
* `username`  

###默认项目
* `status` - "active"


##响应
###`201` - 添加成功
```json
{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "active",
  "phone": "15155522244",
  "displayName": "张良",
  "idcard": "320123199005123210"
}
```
###`400` - 请求参数错误
###`401` - 权限不够
***


##业主更新商户信息

##请求
###PUT /merchants/:id

```json
{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "status": "active",
  "phone": "15155522244",
  "displayName": "张良",
  "idcard": "320123199005123210"
}
```
###必要项目
* `shopID`  

##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
