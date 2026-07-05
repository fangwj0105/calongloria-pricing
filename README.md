# Calon Gloria 印尼产品价格页

这是可部署到 GitHub Pages 的静态发布目录，仅包含公开前端价格表，避免公开后台成本、毛利率和佣金数据。

- `index.html`: 前端市场价格页
- `CNAME`: 默认自定义域名 `pricing.calongloria.id`

## DNS 设置

在 `calongloria.id` 的 DNS 后台增加一条 CNAME：

- Host/Name: `pricing`
- Type: `CNAME`
- Value/Target: `fangwj0105.github.io`

GitHub Pages 仓库需要把 Pages Source 设置为 `main` 分支根目录，并在 Custom domain 填写 `pricing.calongloria.id`。
