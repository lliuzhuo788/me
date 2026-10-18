# 拾光计划：手机端云构建 APK 指南

这个仓库已配置 GitHub Actions 云端构建。你不需要在手机上安装 Android Studio，也不需要本地电脑；需要一个 GitHub 账号，并通过手机浏览器操作 GitHub。

## 第一步：创建 GitHub 仓库
1. 在手机浏览器打开 https://github.com/new 并登录。
2. Repository name 填 `shiguang-planner`。
3. 选择 **Public** 或 **Private** 都可以；建议 Private（私有）。
4. 点击 **Create repository**。不要勾选自动创建 README（本项目已有文件）。

## 第二步：上传项目文件
1. 解压本 ZIP。
2. 进入解压后的项目文件夹，选中里面的所有文件和文件夹（例如 `app`、`.github`、`build.gradle`、`settings.gradle`）。
3. 在 GitHub 新仓库页面使用 **Add file → Upload files**，上传这些项目内容。
4. 确认 `.github/workflows/build-apk.yml` 也上传了。若手机网页不显示隐藏的 `.github` 文件夹，可先使用 GitHub 网页的文件创建功能建立路径 `.github/workflows/build-apk.yml`，并粘贴 ZIP 内同名文件的内容；或者在电脑上上传整个文件夹。
5. 点击 **Commit changes** 保存。

## 第三步：运行构建
1. 打开仓库的 **Actions** 标签。
2. 如果页面提示启用 Actions，按提示启用。
3. 选择左侧 **Build Android APK** 工作流。
4. 点击 **Run workflow**，选择 `main` 分支，再点确认运行。上传/提交到 main 后也会自动触发。
5. 等工作流变成绿色勾号后，点进本次运行页面，向下找到 **Artifacts**。
6. 下载 `shiguang-planner-debug-apk`，再解压下载的 ZIP，里面就是 `app-debug.apk`。

## 第四步：在安卓手机安装
1. 在手机文件管理器里找到 `app-debug.apk`。
2. 点击安装。若系统提示，允许当前浏览器或文件管理器“安装未知应用”。
3. 安装后打开“拾光计划”。

## 说明
- 这是 **debug 测试版 APK**，适合个人安装试用，不是已签名发布版。
- GitHub Actions 首次构建需要几分钟；如果构建失败，请打开失败的运行记录，将红色错误日志复制给 ChatGPT，我可以继续帮你排查。
- 应用数据默认保存在本机 WebView 本地存储。卸载应用或清除应用数据可能导致数据丢失，请定期导出 JSON 备份。
- 不要把密码、访问令牌或其他密钥放进仓库。
