---
description: Local Api常见问题以及注意事项。
---

# API常见问题

### 接口参数使用不规范而导致程序出错甚至闪退

请注意，使用Local Api创建或修改窗口，或是其他操作时，接口参数一定要符合规范，不要随意删改参数，不要传递未知意义的值或类型。

### 使用按键精灵等工具调试接口时，提示传参格式不对

Local Api的所有接口的参数传递方式为body传参，json格式，不接受request url、formdata、string等类型传参方式。建议使用postman调试接口，调通后，再进行脚本开发调用。postman调试示例如下：

![](<../.gitbook/assets/image (8).png>)

