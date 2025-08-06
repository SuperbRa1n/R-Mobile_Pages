# GitHub Pages 部署说明

## 配置步骤

### 1. 在GitHub上创建新仓库
- 创建一个新的GitHub仓库（比如：`your-username.github.io`）
- 或者创建一个普通仓库，稍后配置GitHub Pages

### 2. 初始化Git仓库并推送代码
```bash
cd unpackage/dist/build/web
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/your-repo-name.git
git push -u origin main
```

### 3. 配置GitHub Pages
1. 进入你的GitHub仓库
2. 点击 `Settings` 标签页
3. 在左侧菜单中找到 `Pages`
4. 在 `Source` 部分选择 `Deploy from a branch`
5. 选择 `gh-pages` 分支和 `/ (root)` 文件夹
6. 点击 `Save`

### 4. 自动部署
- 每次推送到 `main` 或 `museum` 分支时，GitHub Actions会自动构建并部署到GitHub Pages
- 部署完成后，你的网站将在 `https://your-username.github.io/your-repo-name` 可用

## 注意事项
- 确保仓库是公开的（public）
- 如果使用自定义域名，需要在仓库设置中配置
- 首次部署可能需要几分钟时间

## 更新部署
每次重新打包后，运行以下命令更新部署：
```bash
./scripts/setup-deploy.sh
```
