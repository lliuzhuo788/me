# 拾光计划 Android 项目

这是可在 Android Studio 中构建的 WebView 应用源码，内置 `app/src/main/assets/index.html`。

## 构建 APK
1. 安装 Android Studio（建议使用 JDK 17）。
2. 用 Android Studio 打开 `android-project` 文件夹。
3. 等待 Gradle 同步；首次构建需要联网下载 Android Gradle Plugin 和 SDK。
4. 选择 Build > Build Bundle(s) / APK(s) > Build APK(s)。
5. 调试 APK 通常位于 `app/build/outputs/apk/debug/app-debug.apk`。

## 功能
- 计划增删改、完成勾选、手动进度、分类、优先级、日期与截止日期
- 备忘录增删改、搜索、分类
- 日历视图、最近 7 天统计、分类统计
- 修改历史：记录创建、编辑、完成状态变化和删除前后的数据
- JSON 数据备份与恢复

## 数据说明
数据使用浏览器/WebView 的本地存储。清理应用数据或卸载应用可能导致数据丢失，请定期使用“导出备份”保存 JSON 文件。
