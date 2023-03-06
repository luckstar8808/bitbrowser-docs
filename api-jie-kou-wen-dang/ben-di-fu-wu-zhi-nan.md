---
description: 调用本地API接口操作比特浏览器打开、配置代理等，帮助用户实现自动化脚本功能。
---

# 本地服务指南

![](../.gitbook/assets/23456.png)

### JavaScript 示例代码

注意：demo里的API参数近作为演示使用，详细参数，请以API文档为准

{% file src="../.gitbook/assets/nodejs-demo.zip" %}

### Python示例代码

注意：demo里的API参数近作为演示使用，详细参数，请以API文档为准

{% file src="../.gitbook/assets/python-demo (2).zip" %}

### E语言示例代码

注意：demo里的API参数近作为演示使用，详细参数，请以API文档为准

{% file src="../.gitbook/assets/E语言示例代码.zip" %}

### Postman调试demo，直接导入即可

{% file src="../.gitbook/assets/Bitnet.postman_collection (1).json" %}

### 服务简介

比特浏览器支持通过接口调用方式使用浏览器功能，帮助用户运行自有的自动化脚本。

### 使用方式

1. 安装并登录比特浏览器
2. 打开系统设置，获取到本地接口url
3. 获取示例代码，运行脚本

### 接口使用概述

* 接口请求方式均为post，传参方式均为body传参
* 接口返回json对象，success为true作成功，如有返回数据，附加在data对象中
* 接口返回success为false时，表示业务失败，可能为程序原因，或参数校验等原因，失败信息会附加到msg中

```
// success example
{
  success: true,
  data: {
    id: '2c9c29a28sdd33dds8026f78e380142',
    groupName: '新建分组测试'
  }
}

// failed example
{ success: false, msg: '分组id必传' }
```

### API调用线路图参考

<figure><img src="../.gitbook/assets/Local Api 使用线路图 (1).svg" alt=""><figcaption></figcaption></figure>
