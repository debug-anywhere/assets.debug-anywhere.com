# v053 Android 远程测试包

## 小米字体兼容候选 4.0.2（4003）

[下载 4.0.2 字体兼容候选](https://assets.debug-anywhere.com/apk/testing/v053/DebugAnywhere-4.0.2-4003-font-fix-test-signed.apk)

Android 10+，约 69 MB。Android 按钮标签显式指定系统字体族，并允许大字号时自适应高度。AOSP API 29/35/36 的 11 组字号/粗体场景通过；尚需 Redmi Note 7 / MIUI / 小米兰亭 Pro 真机确认，不宣称已在该真机修复。

与下方 4.0.1 测试包使用相同证书，可直接覆盖当前测试版保留数据，无需卸载；不能覆盖签名不同的正式版。

SHA256：`70b7c37909b57bd788b1bb78b16df2fe7e7ba91af7a71fc251991857885cc7ce`。

## 4.0.1（4002）对照包

[下载 APK](https://assets.debug-anywhere.com/apk/testing/v053/DebugAnywhere-4.0.1-4002-test-signed.apk)

- 版本：4.0.1（versionCode 4002）；最低 Android 10 / API 29，target API 36。
- 构建：R8 Release，自带离线 JS bundle，包含 arm64-v8a、armeabi-v7a、x86、x86_64。
- 用途：2026-10-28 功能验收测试包，使用开发测试证书，非正式渠道更新包。
- 包名与正式版相同，但签名不同，不能覆盖安装正式版。建议使用备用设备或独立用户空间，保留现有正式版及数据。
- 此测试文件独立发布，不修改正式下载入口 `apk/debug-anywhere-latest.apk`。
- SHA256：`13bedfc95544e299acb8e448e04c57bf2fff8cc965b3c22f0e994226341f7f2b`。

已验证 Android API 29/35/36 核心流程、二维码图片解码、真实网页截图保存，以及该 Release APK 脱离 Metro 的启动与网页工具。正式签名覆盖升级、真机摄像头扫码与真实 16KB 系统运行仍待单独验证。
