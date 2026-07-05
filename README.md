# Calon Gloria 印尼产品定价系统

这是可部署到 GitHub Pages 的静态发布目录。

- `index.html`: 前端市场价格页
- `admin.html`: 后台定价矩阵
- `CNAME`: 默认自定义域名 `pricing.calongloria.id`

## DNS 设置

在 `calongloria.id` 的 DNS 后台增加一条 CNAME：

- Host/Name: `pricing`
- Type: `CNAME`
- Value/Target: `<GitHub用户名或组织名>.github.io`

GitHub Pages 仓库需要把 Pages Source 设置为 `main` 分支根目录，并在 Custom domain 填写 `pricing.calongloria.id`。
