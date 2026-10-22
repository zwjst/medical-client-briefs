# Install / 安装与调用

**GitHub source:** https://github.com/zwjst/medical-client-briefs

There is no universal "install from GitHub" button across all ChatGPT clients. Choose a supported method:

## A. Copy into ChatGPT or a custom GPT

1. Open [SKILL.md](../skills/client-progress-summary/SKILL.md).
2. Copy its complete content into your GPT's **Instructions**, or supply it as instructions in a chat.
3. Ask: `请按统一模板总结以下医疗客户沟通记录：...`

For a public custom GPT, its **creator** must publish that GPT separately using ChatGPT's GPT creation/sharing features. A GitHub repository does not publish a GPT automatically.

## B. Skill-aware environments

Import the directory `skills/client-progress-summary/` following the host's supported Skills installation instructions. If your client accepts a plugin package, build/import the repository according to that client's documented plugin flow. Clients vary; this project does not guarantee every client can import the manifest.

## C. ChatGPT Plugins (public directory)

The source can be prepared for public plugin submission, but a listing only becomes available to other users following **submission, review, approval and publication** through an authorized publisher account. See [publication checklist](PUBLISHING.md). The GitHub repo is not a live tool endpoint.

## 中文说明

- **通用方法：** 打开 `SKILL.md` 并将内容复制进自定义 GPT 的 Instructions，或当作聊天中的系统化工作说明。
- **支持 Skills 的客户端：** 按客户端的官方导入流程加载 `skills/client-progress-summary/`。
- **面向所有人的可发现发布：** 在 ChatGPT 插件目录公开上架，需要完成开发者验证、元数据、合规确认、提交审核与正式发布。仅开源 GitHub 不会自动上架。
- **隐私提醒：** 粘贴客户聊天前请考虑授权、保密义务及适用的平台隐私政策。推荐先删除个人联系方式及患者相关内容。

## Starter prompt / 启动提示

```text
请按统一模板总结以下医疗客户开发沟通记录。
只输出一段中文 CRM 摘要，隐去姓名和具体机构名称。
准确区分已经询问、尚待回复与下一步计划，不推断未知设备配置。

[在此粘贴对话]
```
