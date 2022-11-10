---
description: Local Api常见问题以及注意事项。
---

# API常见问题

### 为什么本地服务端口不固定？

为了防止固定端口被占用而导致本地服务API无法使用，比特浏览器每次启动时会自动寻找空闲端口，随机使用一个。

读取端口可以通过默认配置文件读取，具体请参考：[https://doc.bitbrowser.cn/api-jie-kou-wen-dang/ben-di-fu-wu-zhi-nan](https://doc.bitbrowser.cn/api-jie-kou-wen-dang/ben-di-fu-wu-zhi-nan)

### 接口参数使用不规范而导致程序出错甚至闪退

请注意，使用Local Api创建或修改窗口，或是其他操作时，接口参数一定要符合规范，不要随意删改参数，不要传递未知意义的值或类型，最好使用demo提供的示例代码，直接在示例代码基础上修改，没有用到的参数，使用默认值即可，不要删掉字段。

### 使用按键精灵等工具调试接口时，提示传参格式不对

Local Api的所有接口的参数传递方式为body传参，json格式，不接受request url、formdata、string等类型传参方式。建议使用postman调试接口，调通后，再进行脚本开发调用。postman调试示例如下：

![](<../.gitbook/assets/image (8).png>)

