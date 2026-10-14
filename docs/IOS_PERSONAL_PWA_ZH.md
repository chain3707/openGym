# iPhone 个人版（无需自建服务器）

这版基于 [DuarteSantos8/openGym](https://github.com/DuarteSantos8/openGym)。它通过 GitHub Pages 提供 HTTPS 页面，在 iPhone 的 Safari 中可添加到主屏幕。首次打开是空白个人档案，不会灌入演示训练记录。界面会优先使用手机语言；也可以在设置中改成简体中文。

## 发布

1. 在 GitHub 打开本仓库的 **Settings → Pages**。
2. 在 **Build and deployment → Source** 中选 **GitHub Actions**。若 GitHub 提示启用 Fork 的 Actions，也在 **Actions** 页面启用。
3. 将 `ios-personal-pwa` 分支的改动合并到 `main`。`Deploy personal openGym to GitHub Pages` 工作流会构建并发布页面。
4. 等待 Actions 显示成功，然后在 Pages 设置页打开给出的 HTTPS 地址。默认地址通常是 `https://chain3707.github.io/openGym/`。

## 安装到 iPhone 主屏幕

1. 用 **Safari** 打开 Pages 地址，确认可以进入空白档案。
2. 点 Safari 的 **分享** → **添加到主屏幕** → **添加**。
3. 从新图标打开一次，让页面和离线缓存完成首次加载。之后可以开飞行模式，关闭应用再从图标启动，检查离线进入。

## 数据与备份

训练、体重和设置仅保存在这部 iPhone 的这个网页 App 中。GitHub Pages 只提供程序文件，不保存个人训练记录；这版没有账号、Face ID 登录、跨设备同步，也没有原生 iOS 通知。删除主屏幕 App、清除网站数据、系统回收浏览器存储或更换手机，都可能让本地记录消失。

请定期到 **设置 → 数据与备份 → 导出** 保存 JSON 备份到“文件”或 iCloud Drive。恢复时从同一页面导入备份。若自定义动作包含照片或视频，请选择包含媒体文件的 ZIP 导出选项；普通 JSON 不包含这些文件。

主屏幕 App 和 Safari 标签页可能使用不同的本地存储。开始记录训练后，尽量始终从主屏幕图标打开，并在迁移前先导出备份。

## 版本与来源

Pages 构建沿用 openGym 的前端和运动素材；本分支只改变静态个人版的启动方式、相关界面和发布工作流。原项目采用 AGPL-3.0，参见仓库中的 `LICENSE` 与 `NOTICE.md`。
