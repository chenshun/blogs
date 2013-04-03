# 雇员：employes
***
##功能描述：业主添加新雇员

###请求：/employes
###请求类型：POST

```json
{
  "username": "15151555114",
  "shopID": "154d454a578e475",
  "status": ["active", "leaved", "suspend"]
}
```
###必要项目
*`username`
*`shopID`
*`status`


##响应
###`201` - 添加成功
###`400` - 请求参数错误
###`401` - 权限不够


##功能描述：业主获取所有雇员信息

###请求：/employes
###请求类型：GET

##响应
###`201` - 请求成功
```json
[{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "active",
  "phone": "15155522244",
  "displayName": "张良",
  "idcard": "320123199005123210"
}]
```
###`400` - 请求参数错误
###`401` - 权限不够


##功能描述：业主条件查询雇员信息

###请求：/employes?phone=15252522212&displayName=张良&idcard=320123199005123210&createdAt=1364804674255&leaveAt=1364809674255
###请求类型：GET
###允许的queryKey为：displayName、phone、idcard、createdAt、leaveAt

##响应
###`201` - 请求成功
```json
[{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "active",
  "phone": "15155522244",
  "displayName": "张良",
  "idcard": "320123199005123210"
}]
```
###`400` - 请求参数错误
###`401` - 权限不够


##功能描述：业主更新雇员信息

###请求：/employes/:id
###请求类型：PUT

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
###必要项目
*`shopID`
*`username`
*`status`


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够


##功能描述：雇员离职

###请求：/employes/:id
###请求类型：PUT

```json
{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "leaved",
  "phone": "15155522244",
  "displayName": "张良",
  "idcard": "320123199005123210"
}
```
###必要项目
*`shopID`
*`username`
*`status`


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
