# v053 Android 远程测试包

[下载 APK](https://assets.debug-anywhere.com/apk/testing/v053/DebugAnywhere-4.0.1-4002-test-signed.apk)

- 版本：4.0.1（versionCode 4002）；最低 Android 10 / API 29，target API 36。
- 构建：R8 Release，自带离线 JS bundle，包含 arm64-v8a、armeabi-v7a、x86、x86_64。
- 用途：2026-10-28 功能验收测试包，使用开发测试证书，非正式渠道更新包。
- 包名与正式版相同，但签名不同，不能覆盖安装正式版。建议使用备用设备或独立用户空间，保留现有正式版及数据。
- 此测试文件独立发布，不修改正式下载入口 `apk/debug-anywhere-latest.apk`。
- SHA256：`13bedfc95544e299acb8e448e04c57bf2fff8cc965b3c22f0e994226341f7f2b`。

已验证 Android API 29/35/36 核心流程、二维码图片解码、真实网页截图保存，以及该 Release APK 脱离 Metro 的启动与网页工具。正式签名覆盖升级、真机摄像头扫码与真实 16KB 系统运行仍待单独验证。
