# 店铺：shops
***
## 业主开店

###请求
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
###`400` - 请求参数错误
###`401` - 权限不够
***

##业主获取所有店铺信息

###请求
###GET /shops
###查询条件
`start` - 查询起始位置；示例：?start=0  
`end` - 查询结束位置；示例：?end=19  

###默认项目
`start` - 0  
`end` - 19  

##响应
###`201` - 请求成功
```json
[{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "open",
  "createdAt": "",
  "closeAt": ""
}]
```
###`400` - 请求参数错误
###`401` - 权限不够
***


##业主条件查询店铺信息

###请求
###GET /shops
###查询条件
`name` - 店铺名称；示例：?name=华仔4号店  
`createdAt` - 创建时间；示例：?{"createdAt":{"$gt":1000}}  
`closeAt` - 关店时间：示例：?{"closeAt":{"$gt":1000}}  
`status` - 店铺状态；示例：?status=closed  
`start` - 查询起始位置；示例：?start=0  
`end` - 查询结束位置；示例：?end=19  

###默认项目
`start` - 0  
`end` - 19  

##响应
###`201` - 请求成功
```json
[{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "open",
  "createdAt": "",
  "closeAt": ""
}]
```
###`400` - 请求参数错误
###`401` - 权限不够
***


##业主更新店铺信息

###请求
###PUT /shops/:id

```json
{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "open",
  "createdAt": "",
  "closeAt": ""
}
```
###必要项目
* `name`  
* `merchantID`  


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
***


##雇员离职

###请求
###PUT /shops/:id

```json
{
  "id": "154d4534a48e475",
  "name": "华仔4号店",
  "address": "江宁区胜太路44号",
  "telephone": "02544444444",
  "merchantID": "154d4534a48e475",
  "status": "closed",
  "createdAt": "",
  "closeAt": ""
}
```
###必要项目
* `name`  
* `merchantID`  


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
