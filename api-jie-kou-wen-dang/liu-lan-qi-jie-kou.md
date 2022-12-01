---
description: 创建、修改、打开浏览器等操作接口
---

# 浏览器接口

{% swagger method="post" path="browser/update" baseUrl="/" summary="创建/修改浏览器窗口，指纹对象必传，需要随机指纹对象时，只传空对象{}即可，指纹值里，留空会随机" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" %}
浏览器窗口id，传id时为修改，不传为创建
{% endswagger-parameter %}

{% swagger-parameter in="body" name="groupId" %}
分组id，子账号创建浏览器窗口shi ，分组id必传，否则会创建到主账号下面
{% endswagger-parameter %}

{% swagger-parameter in="body" name="platform" required="true" %}
账号平台URL，如：https://www.facebook.com
{% endswagger-parameter %}

{% swagger-parameter in="body" name="platformIcon" required="true" %}
账号平台Icon，默认填写platform字段的hostname即可
{% endswagger-parameter %}

{% swagger-parameter in="body" name="url" required="true" %}
额外打开的url，多个用,分开
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" required="true" %}
浏览器窗口名称
{% endswagger-parameter %}

{% swagger-parameter in="body" name="remark" required="true" %}
备注
{% endswagger-parameter %}

{% swagger-parameter in="body" name="userName" required="true" %}
浏览器平台账号
{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" required="true" %}
浏览器平台账号密码
{% endswagger-parameter %}

{% swagger-parameter in="body" name="cookie" required="false" %}
平台账号cookie，json格式的cookie字符串，必须符合标准，

[参考示例](fu-lu.md#cookie-ge-shi-hua-shi-li)


{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyMethod" type="Int" required="true" %}
代理类型，2自定义，3提取IP，默认2

注意：由于各家供应商的提取IP结果格式不统一，所以在使用脚本方式打开窗口时，不要使用3提取IP的方式，需要更换IP时，开发者自行提取IP，然后调用设置代理接口设置下代理，然后再打开窗口
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyType" required="true" %}
自定义代理类型 ['noproxy', 'http', 'https', 'socks5', '911s5']中一个，默认noproxy
{% endswagger-parameter %}

{% swagger-parameter in="body" name="host" %}
代理主机
{% endswagger-parameter %}

{% swagger-parameter in="body" name="port" type="Int" %}
代理端口
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ipCheckService" %}
IP库，默认ip-api，选项 ip-api | ip123in | luminati，luminati为Luminati专用
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isIpv6" type="Boolean" %}
IP协议，是否是IPv6，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyUserName" %}
代理账号
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyPassword" %}
代理密账号码
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ip" %}
911 s5 ip
{% endswagger-parameter %}

{% swagger-parameter in="body" name="country" %}
911 s5 国家地区code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="province" %}
911 s5 州/省code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="city" %}
911 s5 城市code
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isIpNoChange" type="Boolean" %}
911是否不改变IP，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="workbench" type="String" %}
浏览器窗口工作台页面，chuhai2345 或  localServer，默认chuhai2345
{% endswagger-parameter %}

{% swagger-parameter in="body" name="abortImage" type="Boolean" %}
禁止加载图片，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="abortMedia" type="Boolean" %}
禁止视频自动播放，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="stopWhileNetError" type="Boolean" %}
网络不通停止打开，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="dynamicIpUrl" type="" %}
proxyMethod = 3时，提取IP链接
{% endswagger-parameter %}

{% swagger-parameter in="body" name="dynamicIpChannel" %}
提取链接服务商，rola | doveip | cloudam | common
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isDynamicIpChangeIp" type="Boolean" %}
每次打开都提取新IP，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isGlobalProxyInfo" type="Boolean" %}
是否使用全局的动态代理信息，针对iphtml，oxylabs，lumauto，ipidea动态代理
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncTabs" type="Boolean" %}
是否同步浏览器tabs ，默认true
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncCookies" type="Boolean" %}
同步Cookie，默认true
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncIndexedDb" type="Boolean" %}
同步IndexedDB，默认false，极少的情况下才需要同步
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncBookmarks" type="Boolean" %}
同步书签，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncAuthorization" type="Boolean" %}
同步已保存的密码，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncHistory" type="Boolean" %}
同步历史记录，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncExtensions" type="Boolean" %}
同步扩展应用数据，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="syncUserExtensions" type="Boolean" %}
跨窗口同步扩展应用，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isValidUsername" type="Boolean" %}
根据平台，用户名，密码，校验重复， false，创建时有效
{% endswagger-parameter %}

{% swagger-parameter in="body" name="allowedSignin" type="Boolean" %}
允许google账号登录浏览器，默认true
{% endswagger-parameter %}

{% swagger-parameter in="body" name="clearCacheFilesBeforeLaunch" type="Boolean" %}
启动前清理缓存文件
{% endswagger-parameter %}

{% swagger-parameter in="body" name="clearCookiesBeforeLaunch" type="Boolean" %}
启动前清理cookie
{% endswagger-parameter %}

{% swagger-parameter in="body" name="clearHistoriesBeforeLaunch" type="Boolean" %}
启动前清理历史记录
{% endswagger-parameter %}

{% swagger-parameter in="body" name="randomFingerprint" type="Boolean" %}
每次启动均随机指纹
{% endswagger-parameter %}

{% swagger-parameter in="body" name="disableGpu" type="Boolean" %}
是否关闭GPU硬件加速，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="enableBackgroundMode" type="Boolean" %}
关闭浏览器后继续运行应用，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="muteAudio" type="Boolean" %}
浏览器静音，默认false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="browserFingerPrint" type="Obect" required="true" %}
指纹对象，参考

[以下对象](liu-lan-qi-jie-kou.md#browserfingerprint-zhi-wen-dui-xiang)


{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/open" baseUrl="/" summary="打开浏览器窗口" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
浏览器窗口id
{% endswagger-parameter %}

{% swagger-parameter in="body" name="loadExtensions" type="Boolean" %}
是否加载扩展中心中已启用的插件
{% endswagger-parameter %}

{% swagger-parameter in="body" name="args" type="Array" %}
浏览器启动参数，注意不要传错了，数组类型，例如无头模式可以传 ["--headless"]，使用非扩展中心中上传的插件可以传 ["--load-extension=xxx/extension/path"]，多个插件使用逗号分隔
{% endswagger-parameter %}

{% swagger-parameter in="body" name="extractIp" type="Boolean" %}
是否尝试自动提取IP
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="成功时，返回浏览器ws与http连接地址" %}
```javascript
{
  success: true,
  data: {
    ws: 'ws://127.0.0.1:50106/devtools/browser/679fc16c-1b48-4112-b297-3659715876d2',
    http: '127.0.0.1:50106'
  }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="browser/close" baseUrl="/" summary="关闭浏览器窗口" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
浏览器窗口id
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/delete" baseUrl="/" summary="删除浏览器" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
浏览器窗口id
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/detail" baseUrl="/" summary="获取浏览器窗口详情" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" %}
浏览器窗口id
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="返回浏览器窗口详情示例" %}
```javascript
{
  success: true,
  data: {
    id: '2c9c2dsdsd323xceeeds24a30065',
    seq: 41,
    code: 'd3sdsddddd',
    platform: 'https://www.instagram.com/',
    platformIcon: 'instagram',
    url: 'https%3A%2F%2Fwww.facebook.com%2F,https%3A%2F%2Fwww.amazon.com%2FBest-Sellers%2Fzgbs%2Fref%3Dzg_bs_unv_hpc_0_2314207011_4_sbg_1,https%3A%2F%2Fwww.baidu.com%2F',
    name: 'ins',
    userName: '',
    password: '',
    cookie: '[{"domain":".instagram.com","expirationDate":1680060024.48996,"hostOnly":false,"httpOnly":false,"name":"ig_nrcb","path":"/","secure":true,"session":false,"storeId":null,"value":"1"}]',
    proxyMethod: 2,
    proxyType: 'noproxy',
    agentId: '',
    host: '',
    proxyUserName: '',
    proxyPassword: '',
    lastIp: '221.222.180.190',
    lastCountry: '中国',
    country: '',
    province: '',
    city: '',
    remark: '备注',
    status: 1,
    operUserId: 'sdd3ds',
    operUserName: '3ds3sdee',
    operTime: '2022-04-14 16:11:05',
    isDelete: 0,
    delReason: null,
    isMostCommon: 1,
    tempStr: null,
    createdBy: 'sdfd3ddddd',
    userId: 'sdfd33dddddd',
    createdTime: '2022-03-31 13:44:40',
    updateBy: 'sdfsdf322222',
    updateTime: '2022-04-14 16:11:05',
    mainUserId: 'dfsddded323fdddd',
    browserFingerPrint: {
      id: '2c9c29a27fda71dd017fde8124a90066',
      seq: 41,
      browserId: '2c9c29a27fda71dd017fde8124a30065',
      ostype: 'PC',
      os: 'Win64',
      version: '',
      userAgent: 'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/92.0.3887.132 Safari/537.36',
      isIpCreateTimeZone: true,
      timeZone: '',
      webRTC: '0',
      position: '1',
      isIpCreatePosition: true,
      isIpCreateLanguage: true,
      resolutionType: '0',
      resolution: '',
      fontType: '0',
      canvas: '0',
      webGL: '0',
      webGLMeta: '0',
      webGLManufacturer: 'Intel Inc.',
      webGLRender: 'ANGLE (NVIDIA GeForce GTX 960M Direct3D11 vs_5_0 ps_5_0)',
      audioContext: '0',
      mediaDevice: '0',
      clientRects: '0',
      hardwareConcurrency: '4',
      deviceMemory: '8',
      deviceNameType: '1',
      deviceName: 'DESKTOP-FZEVSE',
      doNotTrack: '1',
      flash: '',
      portScanProtect: '',
      portWhiteList: '',
      isDelete: 0,
      colorDepth: 32,
      devicePixelRatio: 1.2,
      createdBy: 'sdfsdf333',
      createdTime: '2022-03-31 13:44:40',
      updateBy: 'sdfdsfdsf33333',
      updateTime: '2022-03-31 13:45:19'
    },
    createdName: null,
    belongUserName: null,
    updateName: null,
    agentIpCount: 1,
    belongToMe: false,
    ip: ''
  }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="browser/list" baseUrl="/" summary="获取浏览器窗口列表" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="page" type="Int" required="true" %}
分页，从0开始
{% endswagger-parameter %}

{% swagger-parameter in="body" name="pageSize" type="Int" required="true" %}
分页数量
{% endswagger-parameter %}

{% swagger-parameter in="body" name="groupId" %}
分组id，非必填
{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" %}
窗口名称，模糊查询，非必填
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sortProperties" %}
排序参数，默认序号seq，非必填
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sortDirection" %}
排序顺序，desc/asc，非必填
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="windowbounds" baseUrl="/" summary="排列窗口以及调整窗口尺寸" %}
{% swagger-description %}
注意，参数除了type，其他参数类型都必须是整型数字。参考以下 windowbounds 对象。
{% endswagger-description %}

{% swagger-parameter in="body" name="type" required="true" %}
排列方式，宫格 box ， 对角线 diagonal
{% endswagger-parameter %}

{% swagger-parameter in="body" name="startX" type="Int" required="true" %}
起始X位置，默认0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="startY" type="Int" required="true" %}
起始Y位置，默认0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="width" type="Int" required="true" %}
宽度，最小500
{% endswagger-parameter %}

{% swagger-parameter in="body" name="height" type="Int" required="true" %}
高度，最小200
{% endswagger-parameter %}

{% swagger-parameter in="body" name="col" type="Int" required="true" %}
宫格排列时，每行列数
{% endswagger-parameter %}

{% swagger-parameter in="body" name="spaceX" type="Int" required="true" %}
宫格横向间距，默认0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="spaceY" type="Int" %}
宫格纵向间距，默认0
{% endswagger-parameter %}

{% swagger-parameter in="body" name="offsetX" type="Int" required="true" %}
对角线横向偏移量
{% endswagger-parameter %}

{% swagger-parameter in="body" name="offsetY" type="Int" required="true" %}
对角线纵向偏移量
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/group/update" baseUrl="/" summary="批量修改浏览器窗口分组" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="groupId" required="true" %}
分组ID，从分组管理中获取，必填
{% endswagger-parameter %}

{% swagger-parameter in="body" name="browserIds" type="Array" required="true" %}
浏览器窗口ID数组，必填
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/proxy/update" baseUrl="/" summary="批量修改窗口代理信息" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ids" type="Array" required="true" %}
浏览器窗口ID数组，必填
{% endswagger-parameter %}

{% swagger-parameter in="body" name="ipCheckService" required="true" %}
IP查询渠道，默认ip-api，选项 ip-api | ip123in | luminati，luminati为Luminati专用
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyMethod" type="int" required="true" %}
代理方式，2 自定义代理，3 提取IP，默认2
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyType" %}
代理类型 noproxy|http|https|socks5，默认noproxy
{% endswagger-parameter %}

{% swagger-parameter in="body" name="host" required="false" %}
代理主机
{% endswagger-parameter %}

{% swagger-parameter in="body" name="port" type="Int" required="false" %}
代理端口
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyUserName" %}
代理用户名
{% endswagger-parameter %}

{% swagger-parameter in="body" name="proxyPassword" %}
代理密码
{% endswagger-parameter %}

{% swagger-parameter in="body" name="dynamicIpUrl" %}
提取IPurl
{% endswagger-parameter %}

{% swagger-parameter in="body" name="dynamicIpChannel" %}
提取IP服务商 rola|ipidea|deoveip|cloudam
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isDynamicIpChangeIp" type="Boolean" %}
默认true
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isGlobalProxyInfo" type="Boolean" %}
false
{% endswagger-parameter %}

{% swagger-parameter in="body" name="isIpv6" type="Boolean" %}
是否是IPv6，默认false
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/remark/update" baseUrl="/" summary="批量修改窗口备注" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="browserIds" type="Array" required="true" %}
浏览器ID数组
{% endswagger-parameter %}

{% swagger-parameter in="body" name="remark" required="true" %}
备注
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/close/byseqs" baseUrl="/" summary="通过序号批量关闭窗口" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="seqs" type="Array" required="true" %}
要关闭的窗口序号数组，如：[101, 103, 105]
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/update/partial" baseUrl="/" summary="更新窗口与指纹指定字段值，支持批量修改" %}
{% swagger-description %}
只传需要更新的字段即可，如需要更新name，则只传name
{% endswagger-description %}

{% swagger-parameter in="body" name="ids" type="Array" required="true" %}
要更新的窗口ids集合，单个更新时，传一个id即可，如: ["abd8fd953d3641a0915865a09b8d99ba"]
{% endswagger-parameter %}

{% swagger-parameter in="body" name="browserFingerPrint" type="Object" required="true" %}
指纹对象，传入要更新的对应指纹字段即可，无调整，则放空对象{}即可
{% endswagger-parameter %}

{% swagger-parameter in="body" name="其他参数如 name" %}
更新那个，传入哪个，不更新的不需要传
{% endswagger-parameter %}
{% endswagger %}

{% swagger method="post" path="browser/pids" baseUrl="/" summary="获取已打开窗口的进程id集合，也可以用来判断窗口是否已打开，支持批量查询" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ids" type="Array" required="true" %}
窗口id集合，数组类型
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="正常200返回查询浏览器id的集合对象" %}
```javascript
{
    "success": true,
    "data": {
        "02d39dd4f9c54e40bc1ef51929d27235": 69902,
        "39dd4f4e40bc1ef51929d27232sdf3ds": 84773
    }
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="browser/delete/ids" baseUrl="/" summary="批量删除窗口，一次最多100个，彻底删除记录，包括缓存" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="ids" type="Array" required="true" %}
窗口id集合，数组类型，必传
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    // Response
}
```
{% endswagger-response %}
{% endswagger %}

#### windowbounds对象

```
{
  "type": "box", // 排列方式，宫格 box ， 对角线 diagonal
  "startX": 0, // 起始X位置
  "startY": 0, // 起始Y位置
  "width": 500, // 宽度
  "height": 300, // 高度
  "col": 4, // 宫格排列时，每行列数
  "spaceX": 0, // 宫格横向间距
  "spaceY": 0, // 宫格纵向间距
  "offsetX": 50, // 对角线横向偏移量
  "offsetY": 50 // 对角线纵向偏移量
}
```

#### browserFingerPrint指纹对象

```
{
  coreVersion: '104', // 内核版本，默认104，可选92
  ostype: 'PC', // 操作系统平台 PC|Android|IOS
  os: 'Win32', // 为navigator.platform值 Win32 | Linux i686 | Linux armv7l | MacIntel，当ostype设置为IOS时，设置os为iPhone，ostype为Android时，设置为 Linux i686 || Linux armv7l
  version: '', //浏览器版本，建议92以上，不填则会从92以上版本随机
  userAgent: '', // ua，不填则自动生成
  isIpCreateTimeZone: true, // 基于IP生成对应的时区
  timeZone: '', // 时区，isIpCreateTimeZone 为false时，参考附录中的时区列表
  timeZoneOffset: 0, // isIpCreateTimeZone 为false时设置，时区偏移量
  webRTC: '0', //webrtc 0替换|1允许|2禁止
  ignoreHttpsErrors: false, // 忽略https证书错误，true|false
  position: '1', //地理位置 0询问|1允许|2禁止
  isIpCreatePosition: true, // 是否基于IP生成对应的地理位置
  lat: '', // 经度 isIpCreatePosition 为false时设置
  lng: '', // 纬度 isIpCreatePosition 为false时设置
  precisionData: '', //精度米 isIpCreatePosition 为false时设置
  isIpCreateLanguage: true, // 是否基于IP生成对应国家的浏览器语言
  languages: '', // isIpCreateLanguage 为false时设置，值参考附录
  isIpCreateDisplayLanguage: false, // 是否基于IP生成对应国家的浏览器界面语言
  displayLanguages: '', // isIpCreateDisplayLanguage 为false时设置，默认为空，即跟随系统，值参考附录
  openWidth: 1280, // 窗口宽度
  openHeight: 720, // 窗口高度
  resolutionType: '0', // 分辨率类型 0跟随电脑 | 1自定义
  resolution: '1920 x 1080', // 自定义分辨率时，具体值
  windowSizeLimit: true, // 分辨率类型为自定义，且ostype为PC时，此项有效，约束窗口最大尺寸不超过分辨率
  devicePixelRatio: 1, // 显示缩放比例，默认1，填写时，建议 1｜1.5|2|2.5|3
  fontType: '2', // 字体生成类型 0系统默认|1自定义|2随机匹配
  font: '', // 自定义或随机匹配时，设置的字体值，值参考附录字体
  canvas: '0', //canvas 0随机｜1关闭
  canvasValue: null, // canvas为0随机时设置， 噪音值 10000 - 1000000
  webGL: '0', //webGL图像，0随机｜1关闭
  webGLValue: null, // webGL为0时，随机噪音值 10000 - 1000000
  webGLMeta: '0', //webgl元数据 0自定义｜1关闭
  webGLManufacturer: '', // webGLMeta 自定义时，webGL厂商值，建议留空会自动生成，手工改参考附录
  webGLRender: '', // webGLMeta自定义时，webGL渲染值，建议留空自动生成，手工改参考附录
  audioContext: '0', // audioContext值，0随机｜1关闭
  audioContextValue: null, // audioContext为随机时，噪音值， 1 - 100 ，关闭时默认10
  mediaDevice: '0', // 媒体设备信息，0自定义｜1关闭
  mediaDeviceValue: null, // mediaDevice 噪音值，不填则由系统生成，填值时，参考附录
  speechVoices: '0', // Speech Voices，0随机｜1关闭
  speechVoicesValue: null, // speechVoices为0时，随机时由系统自动生成，自定义时，参考附录
  hardwareConcurrency: '4', // 硬件并发数
  deviceMemory: '8', // 设备内存，1，2，4，8，不要传入大于8的值
  doNotTrack: '1', // doNotTrack 0开启｜1关闭
  clientRectNoiseEnabled: true, // ClientRects true使用相匹配的值代替您真实的ClientRects | false每个浏览器使用当前电脑默认的ClientRects
  clientRectNoiseValue: 0, // clientRectNoiseEnabled开启时随机，值 1 - 999999
  portScanProtect: '0', // 端口扫描保护 0开启｜1关闭
  portWhiteList: '', // 端口扫描保护开启时的白名单，逗号分隔
  deviceInfoEnabled: true, // 自定义设备信息，默认开启
  computerName: '', // deviceInfoEnabled 为true时，设置
  macAddr: '', // deviceInfoEnabled 为true时，设置
  disableSslCipherSuitesFlag: false, // ssl是否禁用特性，默认不禁用，注意开启后自定义设置时，有可能会导致某些网站无法访问
  disableSslCipherSuites: null, // ssl 禁用特性，序列化的ssl特性值，参考附录
  enablePlugins: false, // 是否启用插件指纹
  plugins: '' // enablePlugins为true时，序列化的插件值，插件指纹值参考附录
}
```
