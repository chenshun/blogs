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
*`name`  
*`merchantID`  
###默认项目
*`status` - "open"  


##响应
###`201` - 添加成功
###`400` - 请求参数错误
###`401` - 权限不够
***

##业主获取所有店铺信息

###请求
###GET /shops

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
`createdAt` - 创建时间；示例：?createdAt=1364957460720
`status` - 店铺状态；示例：?status=closed

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

###请求：/shops/:id
###请求类型：PUT

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
*`name`  
*`merchantID`  


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
***


##雇员离职

###请求：/shops/:id
###请求类型：PUT

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
*`name`  
*`merchantID`  


##响应
###`201` - 更新成功
###`400` - 请求参数错误
###`401` - 权限不够
