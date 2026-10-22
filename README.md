# Medical Client Briefs

**Open-source ChatGPT skill for turning overseas medical-device sales chats into clear, concise Chinese CRM progress summaries.**

[中文说明](#中文说明) · [Skill](skills/client-progress-summary/SKILL.md) · [Examples](examples/README.md) · [MIT License](LICENSE)

## Features

- Converts WhatsApp, email and other sales conversation logs to a **single, CRM-ready Chinese paragraph**.
- Preserves country, city, clinical specialty/contact type, communication status, customer feedback, opportunity fit and next actions.
- Uses a consistent introduction phrase: **已介绍公司信息和产品信息** (only when the introduction actually happened).
- Distinguishes **asked / awaiting reply / planned to ask**.
- Avoids unwarranted conclusions (e.g., a surgeon not using a C-arm does not mean a hospital lacks one).
- Suppresses personal names and specific healthcare institution names in the resulting CRM summary.

## Quick start

1. Open [SKILL.md](skills/client-progress-summary/SKILL.md) and review the instructions.
2. In a ChatGPT environment that supports skills, install or import this skill according to that environment's instructions. Alternatively, copy the skill instructions into a custom GPT's instructions or a chat.
3. Paste a sales conversation and ask: **“请按统一模板总结以下医疗客户沟通记录。”**
4. Review the output against the original conversation before saving it to your CRM.

> A public GitHub repository does **not** automatically register a callable ChatGPT tool or publish a GPT in the GPT Store. Others must import the skill/instructions or install a compatible plugin. The included `plugin.json` is a portable plugin manifest, not a remotely hosted MCP endpoint.

## Default format

```text
国家 城市 专业医生／联系人身份。已介绍公司信息和产品信息，并[实际沟通主题]。对方[明确反馈]，[有事实依据的需求判断]。[下一步具体动作或已发出询问的状态]。
```

Only include claims supported by the source conversation. Omit segments that are not applicable; do not invent data.

## Repository

```text
medical-client-briefs/
├── README.md
├── LICENSE
├── plugin.json
├── skills/
│   └── client-progress-summary/
│       └── SKILL.md
└── examples/
    └── README.md
```

## Privacy

The repository contains **fictionalized or anonymized examples only**. Do not commit raw WhatsApp conversations, customer phone numbers, customer emails, patient information, or confidential sales information.

## 中文说明

这是一个面向海外医疗设备销售开发的开源 ChatGPT Skill，用于将 WhatsApp、邮件等沟通记录总结为**简洁、准确、可直接复制到 CRM 的中文单段落摘要**。

默认结构：

```text
国家 城市 专业医生／联系人身份。已介绍公司信息和产品信息，并[实际沟通主题]。对方[明确反馈]，[需求判断]。[下一步实际跟进动作]。
```

### 核心要求

- 摘要中不出现医生姓名、个人联系人姓名或具体医院/诊所名称。
- 只有确实完成公司和产品介绍后，才能使用“已介绍公司信息和产品信息”。
- 严格区分“已询问、等待回复”和“下一步询问”，不可将计划写成已执行。
- 不臆测设备配置、医生身份、客户购买意愿或转介结果。
- 联系渠道只有在影响沟通进度时才需要注明。
- 用户要求翻译、分析或草拟外语客户信息时，不强制输出 CRM 摘要；西语、英语草稿应附中文参考。

### 使用方法

在支持 Skills 的 ChatGPT 客户端中导入 [SKILL.md](skills/client-progress-summary/SKILL.md)，或将其内容放入自定义 GPT 指令。粘贴对话并要求“按统一模板总结”。请在保存至 CRM 前核对摘要与原对话一致。

**注意：** GitHub 公开不意味着其他 ChatGPT 账号能够直接通过链接自动调用该 Skill。实际使用需要各自安装、导入或配置。

## License

MIT — see [LICENSE](LICENSE).
