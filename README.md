# 小遇 Xiaoyu

**简体中文** | [English](README.en.md)

一款使用 Flutter 开发的数字人陪伴 App，支持定制形象、人设和声音，进行实时语音与视频互动。

支持 **iOS / Android** · 当前版本 `0.1.0+1` · **内测中** · 接入 Vidu S2-Avatar 实时版

## 界面预览

深色背景搭配淡紫色强调色，包含品牌启动图、浮动双 Tab 导航、横向角色列表、全屏通话和文字／动作输入面板。

以下为 iOS 界面截图，展示首页、我的、角色创建和通话界面。

| 首页 | 我的 | 创建角色 |
| --- | --- | --- |
| ![iOS 首页](docs/images/ios-home.png) | ![iOS 我的](docs/images/ios-me.png) | ![iOS 创建角色](docs/images/ios-edit.png) |

| 通话画面一 | 通话画面二 | 通话画面三 | 通话画面四 |
| --- | --- | --- | --- |
| ![iOS 通话画面一](docs/images/ios-live1.png) | ![iOS 通话画面二](docs/images/ios-live2.png) | ![iOS 通话画面三](docs/images/ios-live3.png) | ![iOS 通话画面四](docs/images/ios-live4.png) |

## 核心功能

- **角色定制**：选择官方形象或上传照片，设置人设，支持编辑和保存草稿。
- **音色选择**：提供千问与豆包音色，支持分类选择和试听。
- **实时通话**：全屏数字人互动，支持麦克风静音、播放开关、输出路由和挂断。
- **文字与动作**：千问支持文字对话；千问与豆包均支持分类快捷动作。
- **历史记录**：本地保存角色、通话及消息，支持查看详情和核对平台结束状态。

## 快速开始

[下载 Android APK](https://github.com/hsuehly/xiaoyu/releases) · [自动发布说明](docs/ANDROID_RELEASE.md)

[iOS 未签名 IPA](https://github.com/hsuehly/xiaoyu/releases) · [构建与重签说明](docs/IOS_RELEASE.md)（需要自行重签后安装）

开发环境使用 Flutter `3.50.0` / Dart `3.14.0`；支持 Android 8.0+、iOS 15+。平台 SDK 与签名配置见[开发指南](docs/DEVELOPMENT.md)。

```sh
git clone https://github.com/hsuehly/xiaoyu.git
cd xiaoyu
flutter pub get
flutter devices
flutter run -d DEVICE_ID
```

将 `DEVICE_ID` 替换为设备列表中的 ID。运行后：

1. 在“我的 → 右上角设置 → 账号设置”配置并检查 Vidu API Key。
2. 选择官方形象或上传照片，填写人设、选择音色，等待形象就绪。
3. 点击“我的数字人”中的角色图片，确认计费并允许麦克风访问后开始通话。

真实通话需要 [Vidu](https://platform.vidu.cn/) 实时调用权限及余额，费用和结束状态以平台记录为准。出现“待核对”时，请到历史记录继续核对。

豆包国内版支持语音与快捷动作，暂不支持文字对话及通话中换音色。通话需保持 App 在前台。

当前处于内测阶段，组件版、知识库导入、记忆管理及 App 内声音克隆尚未开放，完整范围见[使用说明](docs/USAGE.md)。

## 详细文档

| 文档 | 内容 |
| --- | --- |
| [使用说明](docs/USAGE.md) | 账号配置、创建角色、通话操作、功能限制与数据说明 |
| [开发指南](docs/DEVELOPMENT.md) | 开发环境、iOS 签名、生成代码、构建与项目结构 |
| [工程约束](AGENTS.md) · [Harness](docs/HARNESS.md) | 开发流程、测试、覆盖率及设备验收 |
| [产品需求](docs/PRD.md) · [技术架构](docs/TECHNICAL_ARCHITECTURE.md) · [实施决策](docs/DECISIONS.md) | 产品行为、分层设计与技术选型 |
| [音色目录](docs/VOICE_CATALOG.md) · [快捷动作](docs/QUICK_ACTIONS.md) | 供应商能力、目录映射与维护 |
| [设计参考](design.html) · [设计说明](DESIGN.md) · [玻璃组件迁移](docs/LIQUID_GLASS_EASY_MIGRATION.md) | 页面外观与组件约定 |

## 相关链接

[Vidu 开发平台](https://platform.vidu.cn/) · [Flutter 官网](https://flutter.dev/) · [LINUX DO 社区](https://linux.do/)

## 许可证

Copyright (c) 2026 hsuehly. 原创代码采用 [AGPL-3.0-only](LICENSE)，使用、修改及分发须遵守协议中的源码提供义务。

品牌标识和第三方素材不包含在上述代码授权中；第三方依赖与 SDK 遵循各自许可证及服务条款。
