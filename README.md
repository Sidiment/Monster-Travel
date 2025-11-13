# Monster Travel Privacy Policy Site

## 项目概述

- 提供 `Monster Travel` 的隐私政策静态页面，方便直接部署到 GitHub Pages 或任意静态托管平台  
- `index.html` 是经过美化的单页应用，包含导航、目录、数据表格等完整内容  
- 原始政策文本来源于 `privacy policy.html`（未修改，仅作为备份参考）

## 本地预览

```bash
# 进入项目目录
cd "/Users/tobyzhao/Desktop/公司文件/website/Legal Setting/Privacy Policy"

# 使用系统浏览器打开
open index.html
```

或使用任何 HTTP 服务器，例如 Python：

```bash
python3 -m http.server 8000
# 浏览器访问 http://localhost:8000/index.html
```

## 部署到 GitHub Pages

1. 在 GitHub 创建仓库（例如 `Sidiment/Monster-Travel`）  
2. 初始化 git 并推送：

```bash
git init
git remote add origin git@github.com:Sidiment/Monster-Travel.git
git add README.md index.html "privacy policy.html"
git commit -m "Add privacy policy site"
git push -u origin main
```

3. 在仓库 `Settings → Pages` 选择 `Deploy from a branch`，分支选 `main`，目录选 `/ (root)`  
4. 等待 GitHub Pages 构建完成，访问提示中的链接即可

## 结构说明

- `index.html`：主站点文件（含 CSS 和注释，便于二次维护）  
- `privacy policy.html`：原始导出的隐私政策，仅作为参考，不参与页面渲染  
- `README.md`：当前说明文档

## 维护建议

- 更新政策内容时，先修改 `privacy policy.html` 或直接在 `index.html` 中替换对应段落  
- 需要重新生成目录或表格时，保持锚点 ID 不变，方便已有外链继续使用  
- 建议在每次修改后本地打开页面核对排版，再推送到远端

