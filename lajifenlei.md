# 垃圾分类查询

> 查询垃圾分类信息



## 接口参数

请求地址： `/api/lajifenlei`

请求方式：`get`  `post`

请求参数：

| 参数名称 | 必选 | 类型     | 说明             |
| -------- | ---- | -------- | ---------------- |
| `name`   | 是   | `string` | 要查询的垃圾名称 |
| `num`    | 否   | `int`    | 数量，默认 `10`  |
| `page`   | 否   | `int`    | 页码，默认 `1`   |



## 返回数据：

测试参数：`name=电池`

```json
{
    "code": 200,
    "msg": "success",
    "data": [
        {
            "name": "充电电池",
            "type": 1,
            "aipre": 0,
            "explain": "有毒有害垃圾是指存有对人体健康有害的重金属、有毒的物质或者对环境造成现实危害或者潜在危害的废弃物。",
            "contain": "常见包括废电池、废荧光灯管、废灯泡、废水银温度计、废油漆桶、过期药品、农药、杀虫剂等。",
            "tip": "分类投放有害垃圾时，应注意轻放。其中：废灯管等易破损的有害垃圾应连带包装或包裹后投放；废弃药品宜连带包装一并投放；杀虫剂等压力罐装容器，应排空内容物后投放；在公共场所产生有害垃圾且未发现对应收集容器时，应携带至有害垃圾投放点妥善投放。"
        },
        {
            "name": "干电池",
            "type": 1,
            "aipre": 0,
            "explain": "有毒有害垃圾是指存有对人体健康有害的重金属、有毒的物质或者对环境造成现实危害或者潜在危害的废弃物。",
            "contain": "常见包括废电池、废荧光灯管、废灯泡、废水银温度计、废油漆桶、过期药品、农药、杀虫剂等。",
            "tip": "分类投放有害垃圾时，应注意轻放。其中：废灯管等易破损的有害垃圾应连带包装或包裹后投放；废弃药品宜连带包装一并投放；杀虫剂等压力罐装容器，应排空内容物后投放；在公共场所产生有害垃圾且未发现对应收集容器时，应携带至有害垃圾投放点妥善投放。"
        },
        ...
    ],
    "Author": {
        "name": "Alone88",
        "desc": "由Alone88提供的免费API 服务，官方文档：www.alapi.cn"
    }
}
```

### 返回参数说明

| 参数      | 说明                                                       |
| --------- | ---------------------------------------------------------- |
| `name`    | 废弃物名称                                                 |
| `type`    | 垃圾分类，0 为可回收、1 为有害、2 为厨余(湿)、3 为其他(干) |
| `aipre`   | 智能预判，0为正常结果，1为预判结果                         |
| `explain` | 分类解释                                                   |
| `contain` | 包含类型                                                   |
| `tip`     | 投放提示                                                   |