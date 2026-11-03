# grokbot-family-office

[中文](#中文) · [English](#english)

## 中文

**一个人用 Grok Bot 搭的私人助理团队：秘书、财务、法律、健康、英语、自媒体等 15 个机器人的提示词和定时任务模板，拿来改改就能用。**

每个文件都是中英双语，所有个人信息和国家特定内容都已换成 `{{占位符}}`，任何国家都能套用。

### 机器人总表

| 机器人 | 能帮你做什么 |
|---|---|
| [秘书](01-secretary.md) | 重要邮件提醒和广告归档、隔天查 WhatsApp/Facebook 消息、每周活动汇总、还款提醒 |
| [Bot大总管](02-bot-manager.md) | 总助理兼统筹：派活协调、管理各 bot 设置、召集顾问群；定时提醒账单、监控机构回信、每周项目跟进、工作日巡检各 bot 重要事项 |
| [财务总监](03-cfo.md) | 每日美股简报、预算记账、保险比较、税务待办 |
| [法律顾问](04-legal.md) | {{国家}}法律，重点是留学、移民、签证；也管合同、雇佣、消费者权益 |
| [家庭健康助理](05-family-health.md) | 记录就诊用药、提醒复查、解释化验单 |
| [英语私教](06-english-tutor.md) | 每天 30 分钟口语课 |
| [翻译官](07-translator.md) | 双向同声翻译，只出译文 |
| [自动化工程师](08-automation.md) | 自动化脚本、加密货币模拟盘 |
| [期权顾问](09-options.md) | 看跌期权框架，先算最大亏损 |
| [马斯克视角](10-musk.md) | 第一性原理顾问 |
| [纳瓦尔视角](11-naval.md) | 财富、杠杆、幸福顾问 |
| [芒格视角](12-munger.md) | 逆向思考，圆桌会议里唱反调 |
| [文案运营](13-media-copy-ops.md) | 选题、脚本、发布运营、数据复盘 |
| [视觉制作](14-media-visual.md) | 配音、封面、剪辑出片 |
| [私密陪聊](15-companion.md) | 私密情感陪伴 |
| [群聊](16-group-chats.md) | 圆桌会议和自媒体工作室的分工 |

### 三步上手

1. **复制提示词**：打开对应文件，把“提示词”代码块粘贴到新机器人的描述/系统提示里（中文或英文版任选）。
2. **替换 `{{占位符}}`**：把所有 `{{...}}` 换成你自己的信息（见下表），用不到的整句删掉。
3. **设定时任务**：把“定时任务”一节的 cron 和提示词建成 routine，`{{时区}}` 换成你的时区。

### 占位符说明

| 占位符 | 含义 |
|---|---|
| `{{用户称呼}}` | 机器人怎么称呼你 |
| `{{用户语言}}` | 你希望机器人用的语言 |
| `{{国家}} / {{城市}}` | 所在国家和城市 |
| `{{时区}}` | IANA 时区，如 `Asia/Shanghai`、`America/New_York` |
| `{{货币}}` | 本地货币 |
| `{{税务局}}` | 本国税务机关 |
| `{{急救电话}}` | 本地急救电话 |
| `{{本地活动网站}}` | 本城活动信息来源 |
| `{{用户邮箱}}` | 秘书查看的邮箱 |
| `{{家庭成员列表}} / {{年龄}}` | 家庭成员与孩子年龄 |
| `{{家庭成员健康背景，自行填写}}` | 健康背景（只放在健康机器人里） |
| `{{诊所名}} / {{病历申请邮件标题}} / {{健康助理}}` | 等诊所回信时用 |
| `{{主页名}}` | 你的 Facebook 主页 |
| `{{银行}} / {{金额}} / {{账号}}` | 还款和账单提醒用 |
| `{{兴趣，如老爷车}}` | 活动汇总优先搜的兴趣 |
| `{{机构邮箱}} / {{邮件线程}} / {{日期}} / {{截止日期}}` | 机构回信监控用 |
| `{{项目A}} / {{项目B}}` | 每周跟进的项目 |
| `{{N}} / {{钱包余额}}` | 持仓数量、模拟盘钱包 |

### 安全原则

- 不自动发消息或邮件，不付款、不注册、不发布；只出草稿，由你本人批准。
- 任何不可撤回的操作，先复述要做什么，等你本人确认；其他机器人的批准不算数。
- 不编造数据；密码、证件号、卡号不进聊天。
- 健康和私密聊天内容不写进共享记忆。

### 说明

- 秘书和 Bot大总管的定时任务是真实定义脱敏版；大总管的提示词是推荐提示词；标“示例模板（非原样导出）”的部分是按机器人简介整理的。
- 部分机器人依赖技能（elon-musk-perspective、naval-perspective、munger-perspective、put-options-framework、media-*），要另外安装。

---

## English

**A one-person personal assistant team built with Grok Bot: prompts and routine templates for 15 bots — secretary, finance, legal, health, English tutor, content team and more. Copy, tweak, and go.**

Every file is bilingual (Chinese first, then English). All personal details and country-specific content are replaced with `{{placeholders}}`, so it works in any country.

### The bots

| Bot | What it does for you |
|---|---|
| [Secretary](01-secretary.md) | Important-email alerts and ad archiving, WhatsApp/Facebook checks every other day, weekly events roundup, payment reminders |
| [Bot Manager](02-bot-manager.md) | Chief of staff: delegates and coordinates, manages bot settings, convenes the advisor group; bill reminders, agency-reply monitoring, weekly project follow-ups, weekday cross-bot checks |
| [CFO](03-cfo.md) | Daily US stock briefing, budgeting and bookkeeping, insurance comparison, tax to-dos |
| [Legal Advisor](04-legal.md) | {{country}} law, focused on study abroad, immigration, and visas; also contracts, employment, consumer rights |
| [Family Health](05-family-health.md) | Tracks visits and medications, reminds about check-ups, explains test results |
| [English Tutor](06-english-tutor.md) | 30-minute daily speaking lessons |
| [Translator](07-translator.md) | Two-way simultaneous interpreting, translation only |
| [Automation Engineer](08-automation.md) | Automation scripts, crypto paper trading |
| [Options Advisor](09-options.md) | Put options framework, max loss first |
| [Musk Perspective](10-musk.md) | First-principles advisor |
| [Naval Perspective](11-naval.md) | Wealth, leverage, and happiness advisor |
| [Munger Perspective](12-munger.md) | Inversion; devil's advocate in the roundtable |
| [Copy & Ops](13-media-copy-ops.md) | Topics, scripts, publishing, analytics |
| [Visual Producer](14-media-visual.md) | Voice-over, covers, video editing |
| [Companion](15-companion.md) | Private emotional support |
| [Group Chats](16-group-chats.md) | Roundtable and media studio roles |

### Get started in three steps

1. **Copy the prompt:** open a file and paste the prompt block into a new bot's description / system prompt (Chinese or English).
2. **Fill in the `{{placeholders}}`:** replace every `{{...}}` with your own details (see the table below); delete sentences you don't need.
3. **Set up the routines:** create the cron schedules and prompts from the routines section, replacing `{{timezone}}` with yours.

### Placeholders

| Placeholder | Meaning |
|---|---|
| `{{user name}}` | How the bots address you |
| `{{user language}}` | The language you want replies in |
| `{{country}} / {{city}}` | Your country and city |
| `{{timezone}}` | IANA timezone, e.g. `Asia/Shanghai`, `America/New_York` |
| `{{currency}}` | Local currency |
| `{{tax authority}}` | Your national tax authority |
| `{{emergency number}}` | Local emergency number |
| `{{local event sites}}` | Where local events are listed |
| `{{user email}}` | Inbox the secretary checks |
| `{{family member list}} / {{age}}` | Family members and children's ages |
| `{{family health background}}` | Health background (health bot only) |
| `{{clinic name}} / {{medical records request subject}} / {{health assistant}}` | Used when waiting on a clinic reply |
| `{{page name}}` | Your Facebook page |
| `{{bank}} / {{amount}} / {{account number}}` | For payment and bill reminders |
| `{{interest, e.g. classic cars}}` | Interest the events roundup searches first |
| `{{agency email}} / {{email thread}} / {{date}} / {{deadline}}` | For the agency reply monitor |
| `{{project A}} / {{project B}}` | Projects for the weekly follow-up |
| `{{N}} / {{wallet balance}}` | Number of holdings, paper-trading wallet |

### Safety principles

- Bots never send messages or emails, pay, sign up, or publish on their own; they draft, and you approve.
- Every irreversible action is restated first and waits for your own confirmation; another bot's approval never counts.
- No made-up data; passwords, ID numbers, and card numbers stay out of the chat.
- Health and private-chat content never goes into shared memory.

### Notes

- The Secretary's and Bot Manager's routines are real definitions, anonymised; the Bot Manager's prompt is a recommended version; anything marked "Example template (not a verbatim export)" was reconstructed from the bot's description.
- Some bots rely on skills (elon-musk-perspective, naval-perspective, munger-perspective, put-options-framework, media-*) that need to be installed separately.
