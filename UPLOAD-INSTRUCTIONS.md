# 上传到 GitHub 的步骤

## 🎯 目标仓库
https://github.com/qianjianshui/SSD-website

---

## 🚀 方法一：命令行（推荐）

### 第一次上传（仓库是空的）

在你的本地电脑终端（Mac 打开 Terminal，Windows 打开 Git Bash 或 PowerShell），运行：

```bash
# 1. 进入你下载的 SSD-website 文件夹
cd ~/Downloads/SSD-website

# 2. 初始化 git 仓库
git init

# 3. 添加远程仓库
git remote add origin https://github.com/qianjianshui/SSD-website.git

# 4. 主分支改名为 main（GitHub 新仓库默认）
git branch -M main

# 5. 添加所有文件
git add .

# 6. 第一次提交
git commit -m "feat: VaultDrive official website v5 — 14 sections, 3 languages (EN/JA/DE)"

# 7. 推送到 GitHub
git push -u origin main
```

推送时会要求 GitHub 身份验证：
- 如果设置了 SSH Key 或 Personal Access Token，会自动走
- 如果没有，会弹出浏览器登录窗口（Git Credential Manager）
- 用户名：`qianjianshui`
- 密码：**不是你的 GitHub 密码**，而是 Personal Access Token（见下文）

---

### 以后更新（仓库已经有东西）

每次你改了 `index.html`，只要跑三行：

```bash
cd ~/Downloads/SSD-website
git add index.html
git commit -m "update: [简单描述改了什么]"
git push
```

---

## 🔑 GitHub Personal Access Token 设置（如果推送时报错）

如果你之前没配过，推送时会报 `Authentication failed`。解决方法：

1. 访问 https://github.com/settings/tokens
2. 点 **Generate new token → classic**
3. Note 填 `SSD-website push`，Expiration 选 `No expiration`
4. Scope 勾选 `repo`（全部仓库权限）
5. 点最底部 **Generate token**
6. **立刻复制** 出来（只显示这一次）
7. 推送时粘贴这个 token 作为"密码"

Mac 用户：token 会被自动存到 Keychain，以后不用再输入。

---

## 🌐 方法二：GitHub 网页上传（最简单，不需要命令行）

1. 访问 https://github.com/qianjianshui/SSD-website
2. 点 **Add file → Upload files**
3. 把本文件夹里的以下文件拖进浏览器：
   - `index.html`
   - `README.md`
   - `.gitignore`
4. 最下方 Commit message 填：`feat: VaultDrive official website v5`
5. 点 **Commit changes**

## 🚨 注意
网页上传方式每次更新都得重复整个过程，效率较低。建议还是花 5 分钟配好命令行，后续一行命令搞定所有更新。

---

## 🎁 开启 GitHub Pages（免费托管，自动部署）

上传后做一件事：

1. 访问 https://github.com/qianjianshui/SSD-website/settings/pages
2. **Source** 选 `Deploy from a branch`
3. **Branch** 选 `main` / `(root)` → **Save**
4. 等 30 秒后刷新，顶部会显示：
   ```
   Your site is live at https://qianjianshui.github.io/SSD-website/
   ```
5. 这就是你的网站地址！

以后每次 `git push`，GitHub 会自动重新部署，大概 30-60 秒生效。

---

## 📦 文件包说明

| 文件 | 作用 |
|------|------|
| `index.html` | 主页（原 vaultdrive-v5.html，改名因为 GitHub Pages 默认找 index.html） |
| `README.md` | 项目说明，在仓库首页自动显示 |
| `.gitignore` | 告诉 git 忽略哪些临时文件 |
| `UPLOAD-INSTRUCTIONS.md` | 这份文件（上传完可以删） |

---

## ✅ 成功标志

- GitHub 仓库里能看到 `index.html`、`README.md`
- 仓库首页显示 README 的项目介绍
- GitHub Pages 开启后，能访问 `qianjianshui.github.io/SSD-website/` 看到完整网站

---

## 💬 遇到问题？

最常见的三个问题：

1. **"Permission denied"** → 没配 Personal Access Token，见上文
2. **"fatal: not a git repository"** → 没在正确的文件夹里，先 `cd` 进来
3. **"remote origin already exists"** → 重复添加了，跳过 `git remote add` 那步即可

其他问题随时问我。
