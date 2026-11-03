# Cambridge英汉 for Manggo

一个用于 [Manggo](https://www.yxwza.org/) 的英汉词典插件。输入英文单词或短语，可查看简体中文释义、英文定义、双语例句、词形变化及英美音标和发音。插件还提供独立的 `Cambridge-UK`、`Cambridge-US` 语音服务。

> **非官方项目。**本插件与 Cambridge Dictionary、Cambridge University Press & Assessment 及 Manggo 官方均无隶属或授权关系。词典数据通过 [chenelias/cambridge-dictionary-api](https://github.com/chenelias/cambridge-dictionary-api) 提供的第三方接口获取，并非 Cambridge 官方 API。

## 功能

- 英文词条查询简体中文释义，可同时显示英文定义和词性。
- 每个义项默认显示两组中英双语例句；数量和显示内容可在服务设置中调整。
- 显示可用的词形变化、英式和美式音标与发音链接。
- 提供 `Cambridge-UK` 与 `Cambridge-US` 两个语音服务，可分别添加到 Manggo。

接口返回的字段因词条而异。本插件目前**不提供同义词、反义词，也不支持中文词头反查英文**。

## 安装

1. 下载仓库中的 [`cambridge-dictionary.mplugin`](./cambridge-dictionary.mplugin)。
2. 在 Manggo 的“插件管理”中安装该文件。
3. 到“翻译服务”设置中添加 **Cambridge英汉**，然后查询英文单词，例如 `hold`。
4. 需要听读音时，可到“语音服务”设置中选择添加 **Cambridge-US** 或 **Cambridge-UK**。如果没有其他语音模型的 API，强烈建议添加。作者不太喜欢机器合成的读音，个人觉得 Cambridge 的发音更自然、标准。

更新插件时重新安装新版 `.mplugin`。如果仍显示旧名称或旧内容，可在 Manggo 中移除旧插件后再安装，并检查服务配置是否需要重新添加。

## 设置

“Cambridge英汉”翻译服务中的设置：

| 设置 | 默认值 | 作用 |
| --- | --- | --- |
| 接口根地址 | `https://dictionary-api.eliaschen.dev` | 可改为自行部署的兼容接口地址 |
| 显示词性、英文定义、例句、例句中文翻译 | 开启 | 控制义项展示内容 |
| 每个义项最多例句数 | 2 | 控制例句组数，范围 0–10 |
| 显示词形变化、词性标签、义项分隔线 | 开启 | 控制附加信息 |

语音服务也可以分别设置接口根地址。插件使用 Manggo 的网络权限请求词典接口和音频，不需要填写 Cambridge 官方 API Key。

## 常见问题

**为什么部分词没有例句、词形或发音？**  插件只展示上游接口实际返回的数据；不同词条的内容并不完全相同。

## 数据来源与声明

- 插件依据 [Manggo 原生插件开发指南](https://github.com/Pylogmon/manggo-plugin) 编写。
- 词典接口由 [chenelias/cambridge-dictionary-api](https://github.com/chenelias/cambridge-dictionary-api) 维护；其代码许可证不代表 Cambridge 词典内容可自由复制或再分发。使用者应自行遵守相关服务条款和内容使用要求。
- `icon.png` 使用 Cambridge Dictionary 网站的 favicon。Cambridge Dictionary 名称和图标属于其权利人；使用图标不表示本插件获得官方认可。若权利人要求移除，请通过 GitHub Issue 联系作者。
- 本插件不会要求或收集 Cambridge 官方 API Key。查询文本会发送到配置的第三方接口。

## 作者

[zyj101511](https://github.com/zyj101511)

## 支持项目

如果这个插件对你有帮助，欢迎到 [项目主页](https://github.com/zyj101511/manggo-cambridge-dictionary) 点一个 Star ⭐

![star](assets/star.webp)
