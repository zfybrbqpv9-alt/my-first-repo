# my-first-repo

我的第一个 Git 仓库，用来练习 Git 和 GitHub 的基本操作。

## 学习进度

- [x] 在本机初始化 Git 仓库（`git init -b main`）
- [x] 创建 `README.md` 和 `.gitignore`
- [ ] 配置提交身份（`user.name` / `user.email`）
- [ ] 完成第一次提交（`git commit`）
- [ ] 注册 GitHub 账号
- [ ] 在 GitHub 上新建远程仓库 `my-first-repo`
- [ ] 关联远程仓库并推送（`git remote add` + `git push`）

## 常用命令速查

```bash
git status                 # 查看当前状态
git add .                  # 暂存所有改动
git commit -m "说明"        # 提交一个版本
git log --oneline          # 查看提交历史
git push                   # 推送到远程仓库
git pull                   # 拉取远程更新
```

## 接下来要执行的命令

```bash
# 1. 配置提交身份（只对当前仓库生效，不会污染全局设置）
git config user.name "你的名字"
git config user.email "你的邮箱"

# 2. 第一次提交
git commit -m "chore: 初始化仓库"

# 3. 关联远程仓库（换成你自己的地址）
git remote add origin https://github.com/你的用户名/my-first-repo.git

# 4. 推送
git push -u origin main
```

## 关于推送认证

用 Apple 账号登录 GitHub 不会提供可用于 `git push` 的密码。
推送代码需要使用 **SSH 密钥** 或 **Personal Access Token（个人访问令牌）**。
推荐使用 SSH：私钥保存在本机，公钥粘贴到 GitHub 即可，一次配置长期有效。
