# SolarBrain 原型页面路径

原型已按页面拆分为独立目录。每个目录都包含一个可直接打开的 `index.html`，适合通过静态服务器或 GitHub Pages 访问。

## 入口与 Requirement 配置

- `/`：原有 Rebate End-to-End 总入口（兼容原有交互）
- `/document-requirements/`：Sales / Configuration / Document Requirements 列表
- `/document-requirements/new/`：New Requirement
- `/document-requirements/edit/`：Edit Requirement（使用示例配置打开）
- `/document-requirements/detail/`：Requirement Details
- `/document-requirements/order/`：Sales Order 运行时展示
- `/document-requirements/order-pdf/`：Sales Order PDF 预览
- `/document-requirements/invoice/`：Invoice 运行时展示
- `/document-requirements/invoice-pdf/`：Invoice PDF 预览
- `/document-requirements/preview/`：Order 输出预览
- `/order-invoice-requirement-configuration/`：旧路径，保留用于兼容

## Rebate 与结算页面

- `/rebate-rules/`：Rebate Rules 列表
- `/rebate-rules/new/`：New Rebate Rule
- `/rebate-rules/edit/`：Edit Rebate Rule（使用示例配置打开）
- `/rebate-rules/detail/`：Rebate Rule Details
- `/rebate-achievement/`：Rebate Achievement
- `/credit-memo-requests/`：Credit Memo Requests 列表
- `/credit-memo-requests/detail/`：Credit Memo Request Details
- `/credit-memo-detail/`：Credit Memo Detail

页面内部仍保留原型中的按钮交互；独立路径用于直接打开指定页面，避免必须从一个 SPA 页面逐层点击进入。

## Axure Embed 模式

任意页面 URL 增加 `?embed=true` 后，会隐藏 SolarBrain 顶部栏、侧边栏和全局导航，主内容自动扩展到可用视口宽高。例如：

```text
/rebate-rules/?embed=true
/document-requirements/detail/?embed=true
```

不带 `embed=true` 时，页面保持原有布局。
