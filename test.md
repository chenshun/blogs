# 雇员：employes
***
##功能描述：业主添加新雇员

###请求：/employes
###请求类型：POST

```json
{
  "username": "15151555114",
  "shopID": "154d454a578e475",
  "status": ["active", "leaved", "suspend"],
  "idcard": "320123199105163415"
}
```
###必要项目

*`username`
*`shopID`

###默认项目

*`status`-"active"
##响应

###`201` - 添加成功
###`400` - 请求参数错误
###`401` - 权限不够


##功能描述：业主查询所有雇员信息

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
  "status": "active"
}]
```
###`400` - 请求参数错误
###`401` - 权限不够



##功能描述：业主查询某一雇员信息

###请求：/employes/:id
###请求类型：GET

##响应
###`201` - 请求成功
```json
{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "active"
}
```
###`400` - 请求参数错误
###`401` - 权限不够



##功能描述：业主更新雇员信息

###请求：/employes/:id
###请求类型：PUT

```json
{
  "shopID": "154d454a578e475",
  "status": ["active", "leaved", "suspend"]
}
```
###必要项目

shopID

###默认项目

status: "active"

##响应

###`201` - 添加成功
###`400` - 请求参数错误
###`401` - 权限不够




##功能描述：雇员离职

###请求：/employes/:id
###请求类型：PUT

```json
{
  "shopID": "154d454a578e475",
  "status": "leaved",
}
```
###必要项目

shopID

###默认项目

status: "leaved"

##响应

###`201` - 添加成功
###`400` - 请求参数错误
###`401` - 权限不够
