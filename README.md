# my-first-repo

我的第一个 Git 仓库，用来练习 Git 和 GitHub 的基本操作。

## 学习进度

- [x] 在本机初始化 Git 仓库（`git init -b main`）
- [x] 创建 `README.md` 和 `.gitignore`
- [x] 配置提交身份（`user.name` / `user.email`）
- [x] 完成第一次提交（`git commit` → `f79bd1d`）
- [x] 注册 GitHub 账号（`zfybrbqpv9-alt`）
- [x] 生成 SSH 密钥并关联远程仓库
- [x] 在 GitHub 上新建远程仓库 `my-first-repo`
- [x] 把公钥添加到 GitHub，然后推送（`git push -u origin main`）

🎉 **全部完成！** 仓库地址：https://github.com/zfybrbqpv9-alt/my-first-repo

## 日常使用（以后每次改完代码）

```bash
git status                    # 先看看改了什么
git add .                     # 暂存改动
git commit -m "说明改了什么"   # 保存成一个版本
git push                      # 推送到 GitHub
```

## 常用命令速查

```bash
git status                 # 查看当前状态
git add .                  # 暂存所有改动
git commit -m "说明"        # 提交一个版本
git log --oneline          # 查看提交历史（简洁模式）
git push                   # 推送到远程仓库
git pull                   # 拉取远程更新
git diff                   # 查看还没暂存的具体改动
git restore <文件>          # 撤销某个文件的修改
git remote -v              # 查看远程仓库地址
```

## 关于推送认证

用 Apple 账号登录 GitHub 不会提供可用于 `git push` 的密码。
推送代码需要使用 **SSH 密钥** 或 **Personal Access Token（个人访问令牌）**。
本仓库使用 SSH：私钥保存在本机（`~/.ssh/id_ed25519`），公钥已粘贴到 GitHub，一次配置长期有效。

## 踩过的坑

- **`git add .` 会连本地杂项文件一起加进来**：每次 add 之后先 `git status` 确认一遍，发现不想提交的文件就写进 `.gitignore`。
- **在 GitHub 创建远程仓库时不要勾选 "Add a README file"**：本地已经有 README，两边都有会导致历史冲突、推送被拒。
- **GitHub 用户名大小写**：用户名不区分大小写，但规范形式是小写。远程地址用大写会收到 "repository moved" 警告。
