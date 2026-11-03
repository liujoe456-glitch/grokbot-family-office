# grokbot-family-office

**一个人用 Grok Bot 搭的私人助理团队：秘书、财务、法律、健康、英语、自媒体等 15 个机器人的提示词和定时任务模板，拿来改改就能用。**

> A personal "family office" built from 15 Grok Bot agents: secretary, finance, legal, health, English tutor, media team and more. Each file holds a ready-to-adapt system prompt, its triggers (cron routines or chat), and its output format. All personal data is replaced with `{{placeholders}}`. The prompts are in Simplified Chinese.

## 机器人总表

| 机器人 | 能帮你做什么 |
|---|---|
| [秘书](01-secretary.md) | 重要邮件提醒和广告归档、隔天查 WhatsApp/Facebook 消息、每周活动汇总、还款提醒 |
| [Bot大总管](02-bot-manager.md) | 总助理兼统筹：派活协调、管理各 bot 设置、召集顾问群；定时提醒账单、监控机构回信、每周项目跟进、工作日巡检各 bot 重要事项 |
| [财务总监](03-cfo.md) | 每日美股简报、预算记账、保险比较、新西兰税务待办 |
| [法律顾问](04-legal.md) | 新西兰签证移民、合同、雇佣、消费者权益问答 |
| [家庭健康助理](05-family-health.md) | 记录就诊用药、提醒复查、解释化验单 |
| [英语私教](06-english-tutor.md) | 每天 30 分钟口语课 |
| [翻译官](07-translator.md) | 中英双向同声翻译，只出译文 |
| [自动化牛马](08-automation.md) | 自动化脚本、加密货币模拟盘 |
| [期权高手](09-options.md) | 看跌期权框架，先算最大亏损 |
| [马斯克兄弟](10-musk.md) | 第一性原理顾问 |
| [纳瓦尔](11-naval.md) | 财富、杠杆、幸福顾问 |
| [芒格](12-munger.md) | 逆向思考，圆桌会议里唱反调 |
| [文案运营](13-media-copy-ops.md) | 选题、脚本、发布运营、数据复盘 |
| [视觉制作](14-media-visual.md) | 配音、封面、剪辑出片 |
| [陪聊](15-companion.md) | 私密情感陪伴 |
| [群聊](16-group-chats.md) | 圆桌会议和自媒体工作室的分工 |

## 三步上手

1. **复制提示词**：打开对应文件，把“提示词”代码块里的内容粘贴到新机器人的描述/系统提示里。
2. **替换 `{{占位符}}`**：把所有 `{{...}}` 换成你自己的信息（下表），没有的整句删掉。
3. **设定时任务**：把“定时任务”一节的 cron 和提示词建成 routine，时区改成你自己的。

## 占位符说明

| 占位符 | 含义 |
|---|---|
| `{{用户称呼}}` | 机器人怎么称呼你，如“王总” |
| `{{城市}}` / `{{时区}}` | 所在城市与时区，如 `Pacific/Auckland` |
| `{{用户邮箱}}` | 让秘书查看的邮箱 |
| `{{家庭成员列表}}` / `{{配偶}}` / `{{年龄}}` | 家庭成员与孩子年龄 |
| `{{健康指标}}` / `{{家庭成员健康背景，自行填写}}` | 健康背景（建议只放在健康机器人里） |
| `{{诊所名}}` / `{{病历申请邮件标题}}` / `{{健康助理}}` | 等诊所回复时用 |
| `{{主页名}}` | 你的 Facebook 主页 |
| `{{银行}}` / `{{金额}}` | 还款提醒用 |
| `{{兴趣，如老爷车}}` | 活动汇总优先搜的兴趣 |
| `{{N}}` / `{{钱包余额}}` | 持仓数量、模拟盘钱包等 |

## 安全原则

- 不自动发消息、发邮件，也不付款、注册、发布内容；只出草稿，由你本人批准。
- 任何不可撤回的操作，先复述要做什么，等你本人确认；其他机器人的批准不算数。
- 不编造数据；密码、证件号、卡号不进聊天。
- 健康和私密聊天内容不写进共享记忆。

## 说明

- Bot大总管用的是推荐提示词；标“示例模板（非原样导出）”的部分是按机器人简介整理的，其余是原样导出后脱敏。
- 部分机器人依赖技能（elon-musk-perspective、naval-perspective、munger-perspective、put-options-framework、media-*），要另外安装。
