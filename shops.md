# 店铺：shops
***
## 业主开店

##请求
###POST /shops

```json
{
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": ["open", "suspend", "closed"]
}
```
###必要项目
* `name`  
* `merchantID`  

###默认项目
* `status` - "open"  


##响应
###`201` - 添加成功
```json
{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "createdAt": 1364967296480,
  "closeAt": ,
  "status": "open"
}
```
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主查询店铺信息

##请求
###GET /shops
###查询条件
`name` - 店铺名称；示例：?name=华仔4号店  
`createdAt` - 开店时间；示例：?{"createdAt":{"$gt":1000}}  
`closeAt` - 关店时间：示例：?{"closeAt":{"$gt":1000}}  
`status` - 店铺状态；示例：?status=closed  
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
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "open",
  "createdAt": 1364967296480,
  "closeAt": 
}]
```
###`204` - 无内容
###`304` - not modified
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主更新店铺信息

##请求
###PUT /shops/:id

```json
{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "open",
}
```
###必要项目
* `name`  
* `merchantID`  


##响应
###`200` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
***


##业主关店

##请求
###PUT /shops/:id

```json
{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "merchantID": "154d4534a48e475",
  "status": "closed"
}
```
###必要项目
* `name`  
* `merchantID`  
* `status`  

##响应
###`200` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
###`409` - 请求冲突
