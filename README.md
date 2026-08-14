# 網站合集（用于 GitHub Pages 部署）

此仓库将多个静态网站放在同一存储库的子目录下，已准备好直接推送到 GitHub 并启用 Pages（从 `root` 部署）。

文件：

- `index.html`：仓库根的汇总入口，链接到各子站点。
- `導航站/`, `工具區/`, `官網/`, `解綁卡密/`, `卡密管理/`, `api檢測/`：子站点目录，每个目录包含 `index.html`。
- `.nojekyll`：禁用 Jekyll，保留以便直接部署静态文件。

如何部署：

1. 在 GitHub 上新建仓库（例如 `your-username.github.io` 或任意仓库）。
2. 在本地初始化 git（若尚未）：

```powershell
git init
git add .
git commit -m "Prepare site for GitHub Pages"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
```

3. 到 GitHub 仓库的 Settings → Pages，选择 `Branch: main`、`Folder: / (root)`，保存即可。

可选：如果想使用自定义域，添加 `CNAME` 文件到根目录并在仓库 Pages 设置中配置域名。
