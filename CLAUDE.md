# 课时打卡项目协作协议

## 项目 Memory 位置

`/Users/julie/.claude/projects/-Users-julie-Projects-course-punch/memory/`

包含：
- `MEMORY.md` — 索引
- `project-course-punch.md` — 完整技术状态
- `session-state.md` — **最近 session 工作状态（每次必读、必更新）**
- `user-profile.md` — 用户背景
- `feedback-patterns.md` — 协作偏好

## Session 开始时必做

1. 读取 `session-state.md`，了解上次做到哪里
2. 读取 `project-course-punch.md`，确认项目当前技术状态
3. 向用户简报："上次做了 X，当前状态是 Y，你想继续做什么？"

## Session 过程中必做

**每完成一个主要任务后**，立即更新 `session-state.md` 的"刚完成的工作"和"未完成/被打断的工作"两栏。不要等到 session 结束才更新——防止被中途打断后丢失进度记录。

## Session 结束前必做

1. 更新 `session-state.md`：
   - 刚完成的工作（本次 session 做了什么）
   - 未完成/被打断的工作（如果有）
   - 下一步候选方向
   - 给下个 Session 的注意事项
2. 如果项目结构或功能有重大变化，同步更新 `project-course-punch.md`
3. 确认所有代码已 `git push`

## 开发规范

- 改功能后必须升级 `sw.js` 中的 `CACHE` 版本号（coursepunch-v2 → v3 → ...）
- 图标只能用 PNG（iOS 不识别 SVG apple-touch-icon）
- 本地测试服务器：`python3 -m http.server 8899`（在项目目录下运行）
- guide.html 必须通过 HTTP 服务器打开，不能用 file:// 协议
- guide.html 的生成是 Node.js 脚本写文件，不要手动编辑 HTML
- 部署：`git add <files> && git commit -m "..." && git push`

## 跨 Session 分享此项目上下文

将以下内容粘贴到任意新 session：

> 我在做一个课外班课时打卡 PWA 项目，详细上下文在这个文件里：
> `/Users/julie/.claude/projects/-Users-julie-Projects-course-punch/memory/project-course-punch.md`
> 以及最新工作状态：
> `/Users/julie/.claude/projects/-Users-julie-Projects-course-punch/memory/session-state.md`
> 请先读取这两个文件再开始工作。
