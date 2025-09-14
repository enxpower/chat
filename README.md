# Chat – 中文聊天室（单房间 · 无后端函数）

## 快速开始
1. Firebase 控制台：
   - Authentication → 启用 **Anonymous**。
   - Firestore Database → **Create**（Production 模式）→ **Rules** 粘贴 `firestore.rules` 并 **Publish**。
   - Project Settings → Web App → 复制配置，填入仓库根目录 `firebaseConfig.json`。

2. 推送到 `main`：
   - 方式 A：Settings → Pages → Deploy from branch（`main` / root）。
   - 方式 B：使用 `.github/workflows/deploy.yml` 自动部署。

3. 打开 Pages 地址，首次进入会提示设置 **昵称** 与 **性别**。

## 功能
- 匿名进入（静默）+ 昵称唯一
- 单房间公聊、@某人、Emoji
- 私聊（勾选“私聊打勾”= 仅双方可见；不勾选= 公屏并 @）
- 撤回/删除：作者在 120s 内可操作（规则校验）
