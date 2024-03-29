# 操作指南（图文教程）

## 重要提示

讲解比特浏览器群控系统基础操作，进一步了解请参考：[操作指南（视频教程）](help2.md)、[常见问题](question.md)

## 系统简介

比特浏览器群控系统，为方便广大比特浏览器用户的窗口群控同步操作而生，主要功能如下：

1、通过设置一个主控浏览器窗口，实现同步主控窗口中所有鼠标键盘事件到多个被控窗口中，起到一举多得的作用。

2、可以对所有浏览器窗口进行批量群控同步操作，包括：窗口基础操作、窗口排列操作、标签页操作、仿真输入相同文本、仿真输入差异文本、一键识别验证码打码等！

## 添加/删除/打开/关闭被控窗口

### 添加被控窗口

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

如上图所示，点击箭头1处“添加窗口”按钮，在红框2处列表中，勾选需要添加到被控列表的窗口，勾选完成后，点击箭头3处的“添加”按钮，会将勾选窗口添加到**下图中红框1处**的被控列表中。

<figure><img src="../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

如上图所示：\
红框1处展示所有被控窗口列表**（注：仅群控同步操作勾选的窗口，需要群控同步操作的窗口务必要勾选）**\
红框2代表窗口的在线状态，窗口是打开状态则标记为蓝色，窗口是关闭状态则标记为灰色。\
红框3处“×图标”为关闭窗口快捷按钮，点击后会立即关闭对应的窗口。

### 删除被控窗口

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

如上图所示，使用鼠标右键点击“被控列表”后，会弹出菜单。点击“删除勾选窗口”，会从被控列表中删除掉当前正在勾选的窗口，点击“删除全部窗口”会从被控列表中删除掉全部窗口。

### 打开被控窗口

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

如上图所示，打开被控窗口有3种方式：

1\. 通过比特浏览器客户端直接打开被控窗口，打开状态将自动更新到被控列表中。\
2\. 如图中红框1所示，鼠标双击被控列表中指定窗口，即可打开指定的窗口。\
3\. 如图中红框2所示，通过鼠标右键弹出菜单，可以打开被控列表中勾选的窗口及全部窗口！

**注：**_一次性打开多个窗口，可以通过“设置”界面，设置“批量打开窗口时间间隔”。为确保群控系统稳定性，请根据电脑性能进行合理的设定！电脑性能好，间隔数值可以小一些，电脑性能差，间隔数值请设置大一些！_

### 关闭被控窗口

<figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

如上图所示，关闭被控窗口有3种方式：

1\.  直接手动将打开的浏览器窗口关闭，打开状态将自动更新到被控列表中。\
2\. 如图中红框1所示，点击指定窗口后边的“×”图标，将关闭指定的窗口。\
3\. 如图中红框2所示，通过鼠标右键弹出菜单，可以关闭被控列表中勾选的窗口及全部窗口！

## 同步操作

### 设置主控被控

<figure><img src="../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

**设置主控窗口：**大部分群控同步操作，都需要设置主控以后方可正常进行（因为很多群控同步操作需要以主控为参照对象）。如上图中 箭头1 所示，在被控列表中选中某个窗口后，点击鼠标右键，在弹出菜单中选择“将选中窗口设置为主控”，主控窗口的右侧会有箭头2所示的图标！

**设置被控窗口：**<mark style="color:red;">该被控窗口列表中，仅勾选的窗口会被执行群控同步操作，未勾选的窗口不会被执行群控同步操作！需要进行群控同步操作的窗口，一定记得勾选哦！！！</mark>

### 鼠标键盘同步操作

<figure><img src="../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

如上图所示，点击箭头所示的“开始同步”按钮，就会开始鼠标键盘的同步操作，被控列表中所有被勾选的窗口均会同步主控窗口的鼠标键盘操作；点击“关闭同步”按钮，会停止上述的同步操作！

注：开始同步操作以后，为防止同步操作稳定性被打乱，被控列表不可以进行任何操作，包括：增加/删除/勾选/反勾选/打开/关闭 窗口！

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

如上图所示，红框1部分代表想要执行的具体鼠标键盘同步项，勾选或者反勾选以后，务必点击箭头处的“保存”按钮，点击后会立即生效！ 红框2部分是“开启同步”、“关闭同步”两个按钮的快捷键。

### 窗口同步操作

<figure><img src="../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

如上图所示，点击主界面的“群控操作”，再点击“窗口同步”：

窗口操作 - 激活所有：将所有被控窗口，激活到最上层并显示

窗口操作 - 统一大小：将所被控窗口的长度、高度统一为和主控窗口一样大小

窗口操作 - 重叠所有：将所有被控窗口，无论坐标还是窗口大小，统一和主控窗口一致

宫格排列、对角线排列：按照宫格、对角线方式，排列所有被控窗口

标签页操作 - 统一标签：将所有被控窗口的标签页网址，统一为和主控窗口一模一样

标签页操作 - 关闭所有：将所有被控窗口的全部标签页，统一关闭掉

标签页操作 - 刷新当前：刷新所有被控窗口的当前标签页

标签页操作 - 强制刷新当前：强制刷新所有被控窗口的当前标签页（相当于按Ctrl+F5）

标签页操作 - 当前打开：所有被控窗口中，在当前标签页打开您设定的网址

标签页操作 - 新建打开：所有被控窗口中，新建标签页打开您设定的网址

### 文本同步操作

<figure><img src="../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

如上图所示，点击主界面的“群控操作”，再点击“文本同步”。该功能为：全自动向浏览器发送文本输入指令，全自动按照你设置的输入速度，仿真输入文本内容。该功能分为：相同文本输入（红框1部分）、差异文本输入（红框2部分），相同文本输入：即输入一段内容固定不变的文本，差异文本输入：主要用于网站账号注册等需求，可以为每个被控窗口生成不同内容的左文本、右文本内容，每个窗口可输入不同的左文本、右文本！

#### 相同文本输入

相同文本输入 - 粘贴到浏览器：将系统剪切板里面的内容，粘贴到所有被控窗口里面

相同文本输入 - 清空浏览器输入框：在所有被控窗口中，将当前输入焦点所在的输入框内容清空

相同文本输入 - 输入：将该按钮前面输入框里的内容，仿真输入到所有被控窗口里面

#### 差异文本输入

1. 支持按照模板格式导入左右文本、导出左右文本、生成左文本、生成右文本、输入左文本、输入右文本
2.  如下图所示，在窗口列表中点击鼠标右键弹出菜单，点击“导出左右文本”，可以将当前窗口列表中的左右文本导出。（该导出文件也支持导入）

    <figure><img src="../.gitbook/assets/image (12) (1).png" alt=""><figcaption></figcaption></figure>

#### 仿真输入速度

可以在主界面“设置”界面，进行文本仿真输入速度的设置，设置完毕后需要点击“保存”按钮，方可生效，如下图所示：

<figure><img src="../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

### 一键打码同步操作

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>



如上图所示，点击主界面的“群控操作”，再点击“一键打码”：

1. 首先在“指定窗口”处，选择一个用于定位验证码区域的窗口，选择主控窗口即可。如图箭头1所示，击“定位范围”按钮，在弹出的定位窗口中，用鼠标划区选择验证码所在的位置区域，然后点击“√”图标，确定验证码区域。
2. 如图箭头2所示，点击“测试”按钮，系统会按照您上面定位好的区域在各个被控窗口中截图，然后将截图保存到指定文件夹中，并弹出文件夹。用于参考验证码区域是否定位合理，若合理请进行下一步，若不合理重新进行定位。
3. 如图箭头3所示，选择验证码答题平台，输入答题平台的账号、密码，“验证码类型”默认填写：1010，1010适合1-10位英文和数字，若是不满足您的需求请点击“更多类型”按钮，会弹出验证码类型介绍页面，根据需求自行填写即可！
4. 设置完毕答题平台以后，如图箭头4所示，点击“一键获取验证码”按钮，系统会在各个被控窗口中按照您定位的区域通过答题平台全自动识别验证码，并将答题结果返回到“返回结果”列表中。
5. 返回结果全部执行完毕以后，如图箭头5所示，点击“一键输入验证码”按钮，会将“返回结果”列表中识别到的验证码，输入到所有被控窗口中！**（务必确保各个窗口的验证码输入框处于：有输入焦点状态）**

## 预览和保存窗口画面

### 预览窗口最新画面

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

如上图所示，通过箭头1处，可以设置每行显示的预览窗口缩略图个数，点击箭头2处“预览勾选窗口最新画面”按钮，可以预览到所有被控窗口最新画面！ 双击缩略图，可以弹出放大图片。

### 保存窗口画面

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

如上图所示，点击箭头所示“保存预览画面”按钮，会将当前预览窗口的所有画面，保存到指定文件夹下，并弹出该文件夹！
