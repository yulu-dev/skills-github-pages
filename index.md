---
title: 前后端开发顺序建议
---

不是“前端写完再写后端”，推荐这样做：

1. 先确定需求和页面清单（登录、列表、详情、提交等）。
2. 先设计接口文档（URL、请求参数、返回结构、错误码）。
3. 前后端并行开发：
   - 前端先用 Mock 数据把页面和交互跑起来；
   - 后端按接口文档实现真实 API。
4. 再做联调，按接口逐个替换 Mock 并修复问题。

如果你现在卡在 `npm run dev`，先把 Node 升级到 **22.12+**（你现在是 22.9.0，不满足 Vite 要求），然后执行：

```bash
rm -rf node_modules package-lock.json
npm install
npm run dev
```

Windows 用法：

```powershell
rmdir /s /q node_modules
del package-lock.json
npm install
npm run dev
```
