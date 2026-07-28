<p align="center">
  <a href="https://mail.chatgpt.org.uk/">
    <img src="https://mail.chatgpt.org.uk/logo.svg" width="88" height="88" alt="GPTMail 临时邮箱">
  </a>
</p>

<h1 align="center">GPTMail — 免费临时邮箱</h1>

<p align="center">
  无需注册即可生成一次性邮箱，用来接收验证码、确认链接和短期测试邮件，减少真实邮箱收到的垃圾邮件。
</p>

<p align="center">
  <a href="https://mail.chatgpt.org.uk/"><strong>立即使用 GPTMail</strong></a> ·
  <a href="https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo">Chrome 扩展</a> ·
  <a href="https://mail.chatgpt.org.uk/help">帮助中心</a> ·
  <a href="https://mail.chatgpt.org.uk/api">开发者 API</a>
</p>

<p align="center">
  <a href="README.md">English</a> ·
  <strong>简体中文</strong> ·
  <a href="README.id.md">Bahasa Indonesia</a>
</p>

[![GPTMail 免费临时邮箱界面](https://mail.chatgpt.org.uk/og.png)](https://mail.chatgpt.org.uk/)

## 临时邮箱适合解决什么问题

注册试用、下载资料、测试新功能或接收一次验证码时，使用真实邮箱往往会带来长期的推广邮件。GPTMail 提供短期使用的临时邮箱地址，邮件保留 **24 小时**，足够完成大多数验证流程，又不会让一次注册长期占用个人收件箱。

打开网站后，系统会直接分配一个可用地址。公开临时邮箱无需创建账号；需要更稳定的地址或更严格的访问控制时，也可以接入自己拥有的域名，并选择公开或私密模式。

## 主要功能

| 功能 | 用途 |
| --- | --- |
| 自动生成临时邮箱 | 打开页面即可开始收信，无需注册 |
| 验证码与确认链接提取 | 更快找到常见的一次性验证码和验证入口 |
| 多个可用域名 | 当前域名不被接受时，可以切换其他后缀 |
| 自定义邮箱前缀 | 为某次测试或注册创建便于识别的地址 |
| 公开与私密域名 | 公开收件箱强调方便，私密域名使用密码保护 |
| 自带域名 | 将自己控制的域名接入 GPTMail |
| Chrome 扩展 | 在浏览器工具栏或侧边栏生成地址、查看新邮件 |
| 开发者 API | 为 QA、自动化测试和开发流程创建测试收件箱 |
| Telegram 提醒 | 为当前邮箱接收新邮件通知 |
| 移动端适配 | 手机和电脑都可以直接使用 |

## 使用方法

1. 打开 **[mail.chatgpt.org.uk](https://mail.chatgpt.org.uk/)**。
2. 直接使用系统分配的地址，或点击“随机”生成新地址。
3. 将该地址填写到注册、试用、下载或测试表单中。
4. 返回 GPTMail，等待邮件出现在收件箱。
5. 打开邮件，查看验证码或确认链接。

如果某个平台不接受当前邮箱后缀，可以在域名选择器中切换其他可用域名。域名能否使用取决于实时 DNS 和 MX 配置，因此可用列表可能发生变化。

## Chrome 扩展

安装 **[GPTMail Chrome 扩展](https://chromewebstore.google.com/detail/eplebonhkjiahfnoaiifngokamaipeoo)** 后，可以在当前网页旁边完成常用操作：

- 快速生成或切换临时邮箱；
- 在工具栏和侧边栏查看未读邮件；
- 新邮件到达时显示通知；
- 经用户授权后，在邮箱输入框旁提供当前临时地址建议；
- 每个浏览器安装独立授权，不在扩展中内置公共 API Key。

不安装扩展也不会影响网页版的完整功能。

## 公开邮箱与私密邮箱的区别

**公开临时邮箱不适合保密。**任何知道完整邮箱地址的人都有可能打开对应收件箱。不要用公开临时邮箱接收银行、身份证件、医疗信息、账户找回、长期账号或私人对话。

拥有自己的域名时，可以选择：

- **公开自定义域名：**域名下的地址仍按公开临时邮箱使用；
- **私密自定义域名：**访问收件箱前需要输入域名所有者设置的密码；
- **Cloudflare 辅助配置：**通过范围受限的授权流程自动添加所需 MX 记录，减少手动设置错误。

## 面向开发与测试

GPTMail 适合需要真实接收邮件的测试场景，例如：

- 注册和邮箱验证流程；
- 魔法链接或免密码登录测试；
- 测试环境通知；
- 端到端测试中的唯一邮箱地址；
- 邮件送达测试；
- 不应发送到员工真实邮箱的测试数据。

API Key 应通过请求头传递，不要放在 URL、日志或公开代码中。完整接口说明请查看 **[GPTMail API 文档](https://mail.chatgpt.org.uk/api)**。

## 常见问题

### 临时邮箱是什么？

临时邮箱是一种短期收件地址，可以在不公开个人或工作邮箱的情况下接收邮件，也常被称为一次性邮箱、匿名邮箱、十分钟邮箱或 disposable email。

### 能接收验证码吗？

可以。GPTMail 能接收发送到支持域名的普通邮件，并尝试突出显示常见验证码和确认链接。自动提取只是辅助功能，重要操作仍应核对完整邮件内容。

### 需要注册账号吗？

使用公开收件箱不需要注册。私密域名收件箱需要域名所有者设置的访问密码。

### 邮件保存多久？

目前保存 24 小时。用户主动删除邮件或清空收件箱时，邮件会更早消失。

### 公开临时邮箱安全吗？

公开收件箱不能视为私密空间。只应用于低风险、短期的信息，不要用于敏感数据和重要账号。

### GPTMail 会创建 Gmail 或 Outlook 账号吗？

不会。GPTMail 只提供受支持域名上的临时收件箱，不会创建任何第三方永久邮箱账号。

## 合理使用

请仅在目标网站允许使用临时邮箱的情况下使用 GPTMail。不得用于欺诈、骚扰、垃圾信息、绕过平台安全措施或接收敏感资料。第三方网站有权拒绝一次性邮箱，GPTMail 也无法保证每个域名始终被所有平台接受。

## 了解更多

- [临时邮箱的工作原理](docs/how-temporary-email-works.md)
- [自定义域名与私密收件箱](docs/custom-domains-and-private-inboxes.md)
- [测试与 API 工作流](docs/testing-and-api-workflows.md)
- [GPTMail 帮助中心](https://mail.chatgpt.org.uk/help)
- [服务条款与隐私政策](https://mail.chatgpt.org.uk/terms)
- [产品更新与使用指南](https://mail.chatgpt.org.uk/blog)

---

GPTMail 与 OpenAI、ChatGPT、Google、Microsoft、Telegram 及本文提到的其他第三方服务没有隶属关系。相关产品名称归各自权利人所有。