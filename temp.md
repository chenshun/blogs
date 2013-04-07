# 雇员：employes
***
##业主添加雇员

##请求
###POST /employes

```json
{
  "username": "15155522244",
  "name": "张良",
  "phone": "15211144452",
  "idcard": "320125632541254789",
  "shopID": "154d454a578e475",
  "status": ["active", "leave", "suspend"]
}
```
###必要项目
* `shopID`  
* `username`  
* `name`  
* `phone`  
* `idcard`  

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
  "name": "张良",
  "idcard": "320123199005123210"
}
```
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主查询雇员信息

##请求
###GET /employes
###查询条件
`name` - 雇员姓名；示例：?name=张良  
`phone` - 雇员手机号码；示例：?phone=15252522212  
`idcard` - 雇员身份证号码；示例：?idcard=320123199005123210  
`createdAt` - 雇员入职时间；示例：?{"createdAt":{"$gt":1000}}  
`leaveAt` - 雇员离职时间；示例：?{"leaveAt":{"$gt":1000}}  
`skip` - 查询起始位置；示例：?skip=0  
`limit` - 查询长度；示例：?limit=20  

###默认项目
`skip` - 0  
`limit` - 20  


##响应
###`200` - 成功返回
```json
[{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "createdAt": "1364804674255",
  "leaveAt": "",
  "status": "active",
  "phone": "15155522244",
  "name": "张良",
  "idcard": "320123199005123210"
}]
```
###`204` - 无内容
###`304` - not modified
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主更新雇员信息

##请求
###PUT /employes/:id

```json
{
  "id": "154d4534a48e475",
  "userID": "15423d4a578e475",
  "shopID": "154ac44a578e475",
  "status": "active",
  "phone": "15155522244",
  "name": "张良",
  "idcard": "320123199005123210"
}
```


##响应
###`200` - 成功返回
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##雇员离职

##请求
###PUT /employes/:id

```json
{
  "id": "154d4534a48e475",
  "status": "leave"
}
```
###必要项目
* `status`  


##响应
###`200` - 成功返回
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
