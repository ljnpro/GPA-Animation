# GPA Animation

静态网页入口：`index.html`

## GitHub Pages 部署

仓库已经包含 GitHub Actions 自动部署配置：

- 工作流文件：`.github/workflows/deploy-pages.yml`
- 触发分支：`main` / `master` / `work`

### 启用步骤

1. 把此仓库推送到你的 GitHub 仓库。
2. 在 GitHub 仓库中进入 **Settings → Pages**。
3. 在 **Build and deployment** 中选择 **Source: GitHub Actions**。
4. 等待工作流 `Deploy static page to GitHub Pages` 跑完。

### 访问地址

部署成功后地址为：

- `https://<你的GitHub用户名>.github.io/<你的仓库名>/`

例如仓库名是 `GPA-Animation`，用户名是 `alice`，则地址是：

- `https://alice.github.io/GPA-Animation/`

### 如果 workflow run 被删除，如何重新创建并发布

1. 确保你已经在 `Settings -> Pages` 中把 Source 设为 **GitHub Actions**。
2. 在本地提交一次新变更（哪怕是很小的文档更新）并 push 到 `main` / `master` / `work`。
3. 或者到 `Actions` 页面手动运行 `Deploy static page to GitHub Pages`（`workflow_dispatch`）。
4. 等待 `Deploy to GitHub Pages` 步骤成功后，站点会自动更新。
