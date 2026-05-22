# 读书笔记 · 静态网站

极简个人读书心得站，数据来自微信读书导出。

## 本地预览

```bash
cd weread-notes-site
python -m http.server 8080
```

浏览器打开 http://localhost:8080

## 部署到 GitHub Pages（免费）

### 1. 创建仓库

1. 登录 [GitHub](https://github.com)
2. 点击 **New repository**
3. 仓库名例如：`reading-notes`（任意）
4. 选 **Public**
5. 不要勾选 README（本地已有）
6. 创建仓库

### 2. 上传代码

在本文件夹（`weread-notes-site`）打开终端：

```bash
git init
git add .
git commit -m "Initial commit: reading notes site"
git branch -M main
git remote add origin https://github.com/你的用户名/reading-notes.git
git push -u origin main
```

### 3. 开启 GitHub Pages

1. 仓库页 → **Settings** → **Pages**
2. **Source** 选 **Deploy from a branch**
3. **Branch** 选 `main`，文件夹选 **`/ (root)`**
4. 保存后等待 1–3 分钟

站点地址：`https://你的用户名.github.io/reading-notes/`

### 4. 更新内容

重新运行导出脚本生成站点后：

```bash
git add .
git commit -m "Update notes"
git push
```

## 技术说明

- HTML + Tailwind CSS（CDN），无后端
- 封面图使用微信读书 CDN 外链（需联网显示）
- 全书内容已静态嵌入各 HTML 页面

## 目录结构

```
weread-notes-site/
├── index.html          # 首页书目
├── books/*.html        # 单本书详情
├── .nojekyll           # GitHub Pages 用
└── README.md
```
