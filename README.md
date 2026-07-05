# Calon Gloria 印尼产品价格页

这是可部署到 GitHub Pages 的静态发布目录。

- `index.html`: 前端市场价格页，需使用后台账号管理中启用的账号登录
- `admin.html`: 远程后台登录页，编辑权限由 Supabase RLS 控制
- `supabase-config.js`: Supabase 项目 URL 与 anon key 配置
- `CNAME`: 默认自定义域名 `pricing.calongloria.id`

## 远程后台

1. 在 Supabase 创建项目，并启用 Email/Password Auth。
2. 在 Supabase SQL Editor 执行本地文件 `../docs/supabase-remote-backend.sql`。
3. 创建第一个 Auth 用户后，按 SQL 文件底部的 bootstrap 语句把该用户设为 `owner`。
4. 执行本地文件 `../docs/supabase-seed-pricing.sql` 导入当前后台模型和已发布价格。
5. 把 `supabase-config.js` 中的 `url` 和 `anonKey` 填成 Supabase 项目的 Project URL 与 publishable/anon key。
6. 推送 GitHub Pages 后访问 `/admin.html`。

## DNS 设置

在 `calongloria.id` 的 DNS 后台增加一条 CNAME：

- Host/Name: `pricing`
- Type: `CNAME`
- Value/Target: `fangwj0105.github.io`

GitHub Pages 仓库需要把 Pages Source 设置为 `main` 分支根目录，并在 Custom domain 填写 `pricing.calongloria.id`。
