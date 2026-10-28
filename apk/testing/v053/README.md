# v053 Android 远程测试包

## 版本对齐测试版 0.5.3（4005）

[下载 0.5.3 测试版](https://assets.debug-anywhere.com/apk/testing/v053/DebugAnywhere-0.5.3-4005-backup-import-test-signed.apk?build=4005)

- 与 iOS 对外版本统一为 0.5.3；后续同一版本测试仅递增内部构建号。Android 按 versionCode 判断升级，4005 高于历史 4001–4004；展示版本变化不要求卸载或清数据。
- 与下方 4002–4004 使用同一测试证书，已在 Android 10 从 4.0.3（4004）覆盖安装，四项配置存储逐项一致；离线启动、Release 无 E2E 控件、顶层备份入口、真实网页及调试工具通过。测试数据已恢复。
- 功能与下方 4004 一致，支持 Android 10+，target API 36，四种 ABI，R8 Release，约 69 MB。最终包未重新验证 Android 15 / 16 或 MIUI 真机。
- 备份与导入需要 Pro；JSON 未加密，可能包含敏感 Headers、地址及脚本。历史、Cookie、购买信息和 App 设置不进入备份，导入不执行脚本或刷新网页。
- 仅供测试，无法覆盖签名不同的正式渠道版本；保留现有正式版及数据，不替换正式下载入口。
- SHA256：`13764d2ccf0cd5c7b1ba1644cd3dba4c214e06a8d397235f392b7cc3773df87c`。

## 备份与导入测试版 4.0.3（4004）

[下载 4.0.3 备份与导入测试版](https://assets.debug-anywhere.com/apk/testing/v053/DebugAnywhere-4.0.3-4004-backup-import-test-signed.apk)

- Android 10+（API 29），target API 36，约 69 MB，四种 ABI，R8 Release，自带离线 JS bundle。
- 包含环境、脚本、User-Agent 的单模块与完整 JSON 备份/导入（Pro），顶层 Backup & Import 入口，以及新的导入预览、合并/替换和固定操作栏；保留 Android 字体兼容候选改动。
- JSON 未加密，可能包含敏感 Headers、地址或脚本，需妥善保管。历史、Cookie、购买信息和 App 设置不在备份范围内；导入不会执行脚本或刷新当前网页。
- 与 4002 / 4003 使用相同测试证书，可覆盖此前测试版保留数据；签名不同的正式渠道版本不能覆盖安装，不建议卸载现有正式版。
- 最终 APK 已在 Android 10 验证覆盖安装、四项配置键保留、脱离 Metro 启动、Release 无 E2E 控件、顶层备份入口及真实网页调试。新版导入交互已另行通过 Android 10 原生验证。
- 测试资源独立发布，不替换正式下载入口；本轮最终 APK 尚未重新执行 Android 15 / 16 和 MIUI 真机验证。
- SHA256：`8a3d4ad6370258ff8cb61835488de7f9e8d11b0fd5bd16edc2ac51f8a37657a8`。

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
