---
name: client-progress-summary
description: "Use when summarizing overseas medical-device sales conversations, WhatsApp chats or emails into concise Chinese CRM progress notes."
---

# 医疗客户开发进度总结 / Medical Client Progress Summary

## Goal
Turn user-supplied medical equipment sales conversations into **one concise, objective Chinese paragraph** suitable for a CRM registration log. Preserve actual progress; never invent client responses or actions.

## Default format
`国家 城市 专业医生／联系人身份。已介绍公司信息和产品信息，并[实际沟通主题]。对方[明确反馈]，[有事实依据的需求判断]。[下一步具体动作或已发出询问的状态]。`

## Rules
1. Output **a single paragraph** without headings, lists or commentary when asked for a summary or registration note.
2. Include country, city, specialty or verified contact role when available. Never invent missing locations or roles.
3. **Omit the names of doctors, individual contacts, hospitals, clinics and other specific practicing institutions** from the CRM summary. Use generic descriptions such as “医院工作人员” or “执业机构”.
4. When the company **and products have actually been introduced**, use exactly **“已介绍公司信息和产品信息”**; avoid listing DR and C-arm again in that opening phrase. Do not claim the introduction happened if it did not.
5. Mention the channel only if it matters to the actual progress or the user requests it.
6. Separate sent messages from replies and from planned messages. If a question was already sent: “已询问……，目前等待回复。” If only planned: “下一步询问……。” Never replace the latter with “已询问”.
7. Record real feedback faithfully. If a surgeon says they do not use intraoperative fluoroscopy, this does **not** establish that the hospital has no X-ray equipment.
8. If a hospital staff member does not know equipment configurations, record that they are unknown; do not infer absence.
9. Describe demand fit only where supported by actual evidence. Offer a specific next action without claiming referrals or purchases have occurred.
10. Keep language brief and neutral; avoid hypothetical advice and repeated lead details.
11. When translating or drafting Spanish/English client communications instead of summarizing, follow the requested task and provide Chinese translation alongside non-Chinese drafts.

## Examples
### Example 1 — no direct intraoperative imaging demand
Input: A Tegucigalpa surgical oncologist was told about the company and products and asked about intraoperative imaging. The doctor said their surgeries do not use it; the next step is to ask about institution-level equipment.

Output:
洪都拉斯 Tegucigalpa 肿瘤外科医生。已介绍公司信息和产品信息，并询问其手术中 X 射线及术中透视设备的使用情况。对方明确表示不使用相关设备，当前 C 臂需求匹配度较低。下一步询问对方执业机构的设备使用情况。

### Example 2 — hospital contact, referral requested
Input: A Cartagena hospital staff member identified the institution. The seller introduced their company and products, asked about imaging equipment and requested a biomedical engineering/purchasing contact. No response yet.

Output:
哥伦比亚 Cartagena 医院工作人员。已介绍公司信息和产品信息，并询问医院医学影像设备情况及合作机会。对方确认所属机构，具体职务及设备配置情况尚未明确。已询问能否转介生物医学工程或采购部门负责人，目前等待回复。

## Privacy
Treat raw customer messages as sensitive. Do not publish or reproduce original client identifiers in shared examples. The privacy rule above governs the generated summary, not all other tasks.
