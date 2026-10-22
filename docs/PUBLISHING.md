# Public distribution and submission checklist / 公开发布检查清单

## What is already public
- [x] Public source repository: https://github.com/zwjst/medical-client-briefs
- [x] Portable `plugin.json`
- [x] `SKILL.md`, bilingual README, anonymized examples
- [x] MIT license
- [x] Installation instructions
- [x] Suggested reviewer prompts and release notes

## Public ChatGPT plugin-directory submission — remaining
- [ ] Identify **verified individual or organization publisher**. Do not assume a GitHub username is the verified developer name.
- [ ] Confirm target countries or worldwide availability, subject to the platform's rules.
- [ ] Confirm whether this skill involves any **commerce/payment flow**. It currently specifies none, but the publisher must validate that assertion.
- [ ] Create and verify a public website/about page, support page, privacy policy and terms of service. Policies must reflect actual behavior and the publisher's commitments.
- [ ] Add and validate real square PNG listing logo (>= 256x256) and composer icon (>= 48x48), both <= 5 MiB, with file paths in `plugin.json`.
- [ ] Set all four exact HTTPS URLs in the manifest's `extensions.com.openai.interface`: `websiteURL`, `supportURL`, `privacyPolicyURL`, `termsOfServiceURL`.
- [ ] Align `developerName` with the verified publisher identity.
- [ ] Specify actual distribution/country settings if desired.
- [ ] Prepare, inspect and validate a separate public-submission ZIP with no personal app bindings.
- [ ] Authorized developer uploads ZIP in the developer submission portal, reviews imported metadata and completes applicable legal/policy attestations.
- [ ] Complete review and, **after approval**, explicitly publish the approved release.

**Skills-only plugins:** The publishing guidance does not require an MCP server, MCP test cases, demo recording or reviewer credentials for this project. Public policy links, verification and a real icon remain necessary.

## Proposed natural review prompts
1. 请将以下海外医生 WhatsApp 对话整理成单段落 CRM 开发总结。
2. 对方表示自己手术中不用 C 臂，但未说明医院设备配置。请按统一模板总结，不要推断医院没有相关设备。
3. 我已经向医院工作人员询问生物医学工程部门联系方式，尚未回复。请记录实际进度。
4. 我尚未向对方询问采购计划，请在摘要中正确体现下一步。
5. 请总结以下哥伦比亚医生开发记录，正文不要出现医生和医院名称。

## Release notes

`0.1.0` — Initial open-source CRM summary skill, privacy-conscious one-paragraph Chinese output, truthful outreach-state tracking, examples and bilingual documentation.

## 中文注意事项

仓库公开、私人插件创建、插件目录提交审核和正式发布，是四个**不同状态**。不能因为 `plugin.json` 已在 GitHub 上就声称完成上架。
