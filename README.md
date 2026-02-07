# 📚 课时管理 PWA

一对一教培学生课时记录与续费提醒工具。

## 🚀 最快部署方式：GitHub Pages（5分钟）

### 第一步：上传到 GitHub

```bash
# 1. 新建仓库（去 github.com/new 创建，名字随意，比如 lesson-tracker）

# 2. 在本地操作
cd lesson-tracker   # 进入解压后的文件夹
git init
git add .
git commit -m "init"
git branch -M main
git remote add origin https://github.com/你的用户名/lesson-tracker.git
git push -u origin main
```

### 第二步：开启 GitHub Pages

1. 打开仓库 → **Settings** → **Pages**
2. Source 选 **Deploy from a branch**
3. Branch 选 **main**，文件夹选 **/ (root)**
4. 点 Save，等 1-2 分钟

你的地址：`https://你的用户名.github.io/lesson-tracker/`

### 第三步：iPhone 添加到主屏幕

1. 用 Safari 打开上面的地址
2. 点底部**分享按钮** (↑)
3. 选**「添加到主屏幕」**
4. 点「添加」

完成！🎉 之后从主屏幕打开就像一个原生 App。

---

## 📱 功能说明

- **记课时**：点击学生卡片展开 → 点「＋ 记一次课」
- **满10次自动提醒**：弹窗提醒你联系家长
- **续费登记**：可记录金额、日期、备注
- **续费记录**：独立 Tab 查看所有续费流水
- **搜索**：按学生姓名、科目、家长搜索
- **数据备份**：设置 → 导出/导入 JSON 文件
- **离线可用**：Service Worker 缓存，无网也能用

## 📂 文件结构

```
lesson-tracker/
├── index.html          # 主页面
├── manifest.json       # PWA 配置
├── sw.js              # Service Worker（离线支持）
├── icons/
│   ├── icon-192.png   # Android 图标
│   ├── icon-512.png   # 启动画面图标
│   └── apple-touch-icon.png  # iOS 图标
└── README.md          # 本文件
```

## 🔄 其他部署方式

### Vercel（也很快）
1. 把代码推到 GitHub
2. 去 vercel.com 一键导入仓库
3. 自动部署，还送 HTTPS

### 学校服务器
把整个文件夹丢到任何能提供 HTTP 服务的地方即可（nginx、Apache、甚至 `python -m http.server`）。

## ⚠️ 注意

- 数据存在浏览器 localStorage 中，**清除浏览器数据会丢失**
- 建议定期通过「设置 → 导出数据」备份
- 不同设备间数据不同步（如需同步可自行加后端）
