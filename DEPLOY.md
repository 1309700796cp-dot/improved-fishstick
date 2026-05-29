# 部署步骤

## 1. 上传到 GitHub

1. 在 GitHub 新建仓库，例如 `desktop-countdown-widget`
2. 把 `cloudflare-github-ready-v1` 文件夹里的所有内容上传到仓库根目录
3. 确认仓库根目录能看到：
   - `README.md`
   - `DEPLOY.md`
   - `public/`
   - `app/`

## 2. 连接 Cloudflare

1. 进入 Cloudflare Dashboard
2. 打开 `Workers & Pages`
3. 创建项目并选择 GitHub 仓库
4. 选择 `Connect to Git`
5. 选择刚才的 GitHub 仓库
6. 部署设置：
   - Project name: 可保持默认，也可以改成 `desktop-countdown-widget`
   - Build command: 留空
   - Deploy command: `npx wrangler deploy`
7. 点击部署

## 3. 绑定域名

在 Pages 项目的 `Custom domains` 中添加：

- `www.chanping.de`
- `chanping.de`

如果 Cloudflare 提示域名已被其他 Pages 项目使用，需要先到旧项目的 `Custom domains` 里移除该域名。

## 4. 测试

部署完成后访问：

- `https://www.chanping.de`
- `https://chanping.de`

下载链接：

- `https://www.chanping.de/downloads/DesktopCountdownWidget-v1.0.0.zip`
- `https://chanping.de/downloads/DesktopCountdownWidget-v1.0.0.zip`
