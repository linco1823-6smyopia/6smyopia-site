# Printed Links Registry（印刷短链登记簿）

> 铁律：**印进书里（尤其是平装书）的短链，永不删除、永不复用、永不 404。**
> 书撒出去就收不回来。每次改书稿、改服务器、改域名前，先查这张表。
> 最后更新：2026-09 · 维护人：Linco

## 已印刷 / 待印刷短链

| 短链 | 落地去向 | 印入位置 | 状态 | 备注 |
| --- | --- | --- | --- | --- |
| `6smyopia.com/case/1` | `/case/1/` 静态案例页（Xiang：−1.50D → 0.00D） | KDP 版 + D2D 版：附录 3 Case A 章末；平装重印：QR 码 | 待印刷 | 永久案例页，不做 301 跳走；SaaS 上线后只改页尾 CTA |
| `6smyopia.com/case/2` | `/case/2/` 静态案例页（Xiaojing：六年守住 26mm） | KDP 版 + D2D 版：第 13 章 Xiaojing 案例脚注处；平装重印：QR 码 | 待印刷 | 同上 |
| `6smyopia.com/case` | `/case/` 案例库索引页 | KDP 版 + D2D 版：第 14 章工具箱或后记（可选，只印一次） | 待印刷 | 索引页，日后新增案例自动在此出现 |
| `6smyopia.com/cheat-sheet` | 邮件订阅落地页（待建） | KDP 版 + D2D 版：书尾钩子 | 待建落地页 | 永远指向自己网站 |
| `6smyopia.com/book` | 书籍落地页（待建，列全平台购买入口） | D2D 版书尾（替代一切 Amazon 链接）；KDP 版可放可不放 | 待建落地页 | Apple Books 拒审 Amazon 链接，D2D 版只放这条 |
| `6smyopia.com/review` | 301 → `https://www.amazon.com/dp/B0HJQLF784` | 仅 KDP 版书尾（评论请求）；平装重印可用 | 兜底页建成（/review/index.html），Nginx 301 规则已写入 deploy/nginx-6smyopia.conf，待服务器启用 | **不挂 Amazon Associates 联盟标签**（联盟协议禁止出现在电子书中）；ASIN 变了只改服务器端 301 + 兜底页 3 处链接 |
| `6smyopia.com/app` | 301 → `app.6smyopia.com` | 书内工具指引处 | 兜底页已建成 | Nginx 301 规则待配置（当前为 meta refresh 兜底页） |

## 变更记录

| 日期 | 变更 | 操作人 |
| --- | --- | --- |
| 2026-09 | 建立登记簿；/case/1、/case/2 落地页上线（真实随访数据） | — |

## 新增短链流程

1. 先在本表登记 → 2. 建落地页并自测 200 → 3. 才准印进书稿 → 4. 印刷后该行锁定，只允许"落地页内容进化"，不允许删除/复用/改去向（/review、/app 这类 301 型除外，其目标可随服务器配置更新）。
