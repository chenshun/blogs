# 店铺：shops
***
##功能描述：业主添加新店

###请求：/shops
###请求类型：POST

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


##功能描述：业主获取所有店铺信息

###请求：/shops
###请求类型：GET

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


##功能描述：业主条件查询店铺信息

###请求：/shops?name=华仔4号店&createdAt=1364957460720&closeAt=1364957460720&status=closed
###请求类型：GET
###允许的queryKey为：name、createdAt、closeAt、status

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


##功能描述：业主更新店铺信息

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


##功能描述：雇员离职

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
