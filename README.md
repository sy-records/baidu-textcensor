# 百度文本内容审核

[百度文本内容审核](https://ai.baidu.com/tech/textcensoring)能一站式检测文本中夹杂的色情、推广、辱骂、违禁、涉政、灌水等垃圾内容，净化网络环境，为您的应用提供更可靠的内容安全保障，运用业界领先的深度学习技术，判断一段文本内容是否符合网络发文规范，实现自动化、智能化的文本审核，大幅节省内容审核的人力成本，为您的产品体验保驾护航

## 能力介绍

* 文本色情：对文本中的色情行为描述、色情资源链接、低俗交友、污秽文爱等内容进行识别
* 暴恐违禁：对暴力行为、恐怖描述、赌博、毒品、枪支弹药等违禁内容进行识别
* 政治敏感：对文本中的敏感事件、涉政人物、散布谣言、反动宣传等内容进行识别
* 恶意推广：对文本中带有售卖意向的软文广告，微信、QQ等个人联系方式等违规内容及变体进行识别
* 低俗辱骂：对文本中的侮辱谩骂、人身攻击、消极宣泄等内容进行识别
* 低质灌水：对网络社区常见的乱码、水帖、刷屏等无意义的灌水信息进行识别

## 安装

```bash
composer require sy-records/baidu-textcensor
```

## 使用

```php
$appId = "";
$apiKey = "";
$secretKey = "";

$client = new \Luffy\TextCensor\Core($appId, $apiKey, $secretKey);
$res = $client->textCensorUserDefined("沈唁志博客：https://qq52o.me"); //待审核文本字符串

//具体参数说明见：https://ai.baidu.com/ai-doc/ANTIPORN/Nk3h6xbb2
var_dump($res);
```

## 说明

1. AppID、API Key、Secret Key在百度Ai控制台的 [产品服务 / 内容审核 - 应用列表](https://console.bce.baidu.com/ai/?fromai=1#/ai/antiporn/app/list) 创建应用后获取；
2. 百度有默认审核策略，如果误杀严重，请进入 [内容审核平台创建自定义规则](https://ai.baidu.com/censoring#/strategylist) 进行修改策略；

## 其他系统

* WordPress 插件

项目地址：https://github.com/sy-records/wp-baidu-textcensor

* Typecho 插件

项目地址：https://github.com/sy-records/BaiduTextcensor

## License

Apache-2.0
