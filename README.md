# CCC 效率平台 — Android 客户端

一个轻量的 Android WebView 壳子，加载部署好的 CCC 效率平台。

## 使用方式

### 1️⃣ 推送到 GitHub

```bash
cd ~/Desktop/ccc-android
git init
git add .
git commit -m "init: Android WebView wrapper"
```

去 GitHub.com 新建一个仓库（比如 `ccc-android`），然后：

```bash
git remote add origin https://github.com/你的用户名/ccc-android.git
git push -u origin main
```

### 2️⃣ 自动编译

推送后，前往 GitHub 仓库页面 → **Actions** 标签页，会看到一个名为 **Build APK** 的工作流正在运行。

等待几分钟，完成后点击这个 workflow → 在 **Artifacts** 区域下载 `CCC效率平台-APK.zip`。

### 3️⃣ 安装到手机

解压 zip，把里面的 `.apk` 文件传到手机上，点击安装即可。

> 首次安装需要在手机上开启「允许安装未知来源应用」。
> 如果提示「风险提醒」，点「仍然安装」即可（自己的 App 自己负责 😎）。

## 自定义网址

如果要改成你自己的网址，修改 `app/src/main/java/com/ccc/webview/MainActivity.java` 里的：

```java
private static final String HOME_URL = "https://你的网址.com";
```

## 技术栈

- Android SDK 34 (minSdk 24)
- WebView + AppCompat
- 纯原生，无第三方 WebView 框架
- APK 体积约 **3MB**
