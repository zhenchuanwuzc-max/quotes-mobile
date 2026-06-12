# quotes-mobile

[quotes-app](https://github.com/zhenchuanwuzc-max/quotes-app-data) 金句库的手机端只读页面（GitHub Pages 托管）。

- **本页面是空壳**：不含任何金句数据、不含任何密钥。数据需输入 GitHub fine-grained PAT 后经 Contents API 实时读取私有仓 `quotes-app-data/quotes.json`。
- PAT 仅存浏览器 localStorage，仅发往 `api.github.com`（HTTPS）。
- 只读：加金句 / pin / 删除请在桌面端操作。

## ⚠️ 安全锚点（给未来的维护者）

PAT 存储的 localStorage 作用域 = **整个 `zhenchuanwuzc-max.github.io` origin**（不按 `/quotes-mobile/` 路径隔离）。
**未来在同一 GitHub 账号下新建任何 Pages 站点之前，必须复评此 PAT 的泄露风险**——同 origin 的任何页面 JS 都能读到它。届时可改用 Cloudflare Worker 代理或换只读 PAT。

（plan-reviewer 双盲审查必改项 #2，2026-06-12；方案见 iCloud `工具/quotes-app/PLAN_mobile_readonly_draft.md`）
