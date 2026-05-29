# Desktop Countdown Widget

这是一个 Windows 桌面倒计时浮窗项目，配套一个可部署到 Cloudflare 的下载页。

## 目录结构

- `public/`：Cloudflare 静态网页目录
- `public/downloads/DesktopCountdownWidgetSetup-v1.0.0.exe`：Windows 安装版
- `public/downloads/DesktopCountdownWidget-v1.0.0.zip`：Windows 便携版
- `app/`：桌面浮窗源码和启动脚本

## 本地使用

推荐下载 `DesktopCountdownWidgetSetup-v1.0.0.exe`，双击安装后会创建桌面和开始菜单入口。

如果使用便携版，下载并解压 `DesktopCountdownWidget-v1.0.0.zip` 后：

1. 双击 `Start-DesktopCalendar.cmd` 启动浮窗
2. 如需开机自启动，双击 `Enable-Startup.cmd`

## Cloudflare

连接 GitHub 仓库后，Cloudflare 设置：

- Build command: 留空
- Deploy command: `npx wrangler deploy`

`wrangler.toml` 已经配置了：

```toml
[assets]
directory = "./public"
```

自定义域名建议同时绑定：

- `chanping.de`
- `www.chanping.de`

如果只绑定其中一个，另一个地址不会自动可用。
