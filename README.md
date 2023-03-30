## 对话机器人接口

#### 1. 文件上传状态接口

调用地址
>POST > [域名]:5888/shiyou/upload_file

参数

| 参数名称         | 参数类型        |  必填与否       | 样例取值                             | 参数说明                          |
|:----------------:|:---------------:|:---------------:|:------------------------------------:|:---------------------------------:|
| user_id         | string          | 必选            |  "11122"                               | 用户名                    |
| file      | .docx          | 必选            |   xxx.docx                              | 文件                    |


返回值：
```
{
    "code": 200,//返回码 200成功，其他失败
    "data":解析完成
}
```

#### 2. 用户问答接口

调用地址
>POST > [域名]:5888/shiyou/chat

参数

| 参数名称         | 参数类型        |  必填与否       | 样例取值                             | 参数说明                          |
|:----------------:|:---------------:|:---------------:|:------------------------------------:|:---------------------------------:|
| user_id         | string          | 必选            |  "11122"                               | 用户名                    |
| text      | string          | 必选            |  "你叫什么？"                               | 用户问题                    |
| history      | string          | 可选            |  "用户：我叫张三，你叫什么？机器人：我叫小优"...                               | 历史记录(保留最近5段对话)                    |

返回值：
```
{
    "code": 200,//返回码 200成功，其他失败
    "data":"我是企业介绍机器人小优",
}
```

#### 3. 用户修改接口

调用地址
>POST > [域名]:5888/shiyou/update

参数

| 参数名称         | 参数类型        |  必填与否       | 样例取值                             | 参数说明                          |
|:----------------:|:---------------:|:---------------:|:------------------------------------:|:---------------------------------:|
| user_id         | string          | 必选            |  "11122"                               | 用户名                    |
| update_Q      | string          | 必选            |  "我是修改测试问题"                               | 修改问题                    |
| update_A      | string          | 必选            |  "我是修改测试答案"                               | 修改答案                    |

返回值：
```
{
    "data": "修改完成",
    "code": 200//返回码 200成功，其他失败
}
```
