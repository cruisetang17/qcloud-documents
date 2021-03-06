### 1. 接口描述
本接口 (GetCreateMultiDevTask) 用于查询批量创建设备任务的执行状态。

接口请求域名：`iotcloud.api.qcloud.com`


### 2. 输入参数

以下请求参数列表仅列出了接口请求参数，其它参数见[公共请求参数](https://cloud.tencent.com/doc/api/229/6976)页面。

| 参数名称   | 必选   | 类型     | 描述               |
| ------ | ---- | ------ | ---------------- |
| taskID | 是    | String | 任务ID，由批量创建设备接口返回 |



### 3. 输出参数

| 参数名称       | 类型     | 描述                                       |
| ---------- | ------ | ---------------------------------------- |
| code       | Int    | 公共错误码。0 表示成功，其他值表示失败，详见[公共错误码](https://cloud.tencent.com/document/product/634/12279)页面 |
| message    | String | 模块错误信息描述，格式为 "（模块错误码）模块错误信息" ，详见本页面的[模块错误码](#module_error_info) |
| codeDesc   | String | 模块错误码的英文描述                               |
| taskStatus | Int    | 任务是否完成。1代表完成，0代表未完成                      |
| taskID     | String | 任务ID                                     |



### 4. 示例

输入

<pre>
  https://iotcloud.qcloud.com/index.php?Action=GetCreateMultiDevTask
  &taskID=abcdedf123456789
  &<<a href="https://cloud.tencent.com/doc/api/229/6976">公共请求参数</a>>
</pre>

输出

```
{       
    "message": "",
    "codeDesc": "Success",
    "code": 0,
    "taskStatus":1,
    "taskID":"abcdedf123456789"
}
```
<span id = "module_error_info"></span>
### 5. 模块错误码

| 模块错误码 | 描述              |
| ----- | --------------- |
| 2006  | 任务不存在           |
| 2100  | 内部服务器错误，请联系技术人员 |





