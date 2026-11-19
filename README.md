# ZJOOC Automation Skills (在浙学自动化工具集)

A set of browser-automation skills for the Zhejiang online course platform **zjooc.cn（在浙学 / 浙江省高等学校在线开放课程共享平台）**. They drive a built-in virtual browser to finish routine coursework: watching lecture videos, replying to discussion posts, submitting homework, and exporting a graded-result screenshot report.

面向「在浙学」(zjooc.cn) 的一组浏览器自动化 Skill，在自带的虚拟浏览器里完成日常课程任务：刷章节视频、回讨论帖、提交作业、把作业完成情况截图汇总成 Word。

## What's inside / 包含的工具

| Skill (zip) | 作用 | What it does |
| --- | --- | --- |
| `在浙学视频刷课Skill.zip` | 自动连播章节未看视频，并到学习进度页核对观看时长 | Auto-plays unwatched chapter videos and verifies watch progress |
| `在浙学讨论回帖Skill.zip` | 按同学姓名定位主帖，拟好回复草稿，确认后在详情页评论区提交 | Locates a student's discussion post, drafts a reply, and submits it after your approval |
| `在浙学作业Skill.zip` | 读取作业题目，按单选/多选/填空作答并逐份提交，回列表核验 | Reads homework questions, answers single/multiple-choice and fill-in items, submits and verifies |
| `在浙学作业截图汇总Skill.zip` | 逐份打开作业结果详情页，整页截图（题干、我的答案、每题得分），按 `姓名_班级_学号_作业名` 命名并汇总成一份 Word | Opens each graded-result page, captures a full-page screenshot (question, my answer, score), names files `Name_Class_ID_Homework`, and bundles them into one Word document |

## How to use / 怎么操作

1. 打开 AI 工作模式，直接说要做什么：做作业、刷视频、回讨论帖，还是把作业完成情况截图汇总；回帖就说明要回复哪位同学，不知道课程就把在浙学链接贴给它。
   Open AI work mode and just say what you want: do homework, watch videos, reply to a post, or collect homework screenshots. For replies, name the student; if unsure about the course, paste the zjooc link.
2. 剩下的 AI 自己在虚拟浏览器里完成，不用手动开浏览器、不用提前登录。
   The AI handles the rest in its virtual browser; no manual browser setup or pre-login needed.
3. 遇到登录、验证码或扫码时，AI 会把窗口交给你；登录好、交回控制权，它接着做。
   At login / CAPTCHA / QR code, the AI hands the window to you; after you sign in and return control, it continues.
4. 回帖前 AI 会先把草稿给你看，你确认后它才发出去。
   Discussion replies are drafted first and only sent after your confirmation.
5. 做完 AI 会自己核对一遍，把结果告诉你。
   After finishing, the AI verifies the result before reporting back.

## Where each task opens / AI 进到课程的哪个位置

| 任务 Task | 打开的位置 Page |
| --- | --- |
| 做作业 Do homework | 课程「作业」列表页：每行一份作业、带"去作业"按钮；逐份点进去答题，提交后回列表看是否变成"已提交" |
| 刷视频 Watch videos | 课程「章节内容」列表页：章节树标着已看/未看；点进视频自动连播下一节，最后到「学习进度」页核对观看时长 |
| 回讨论帖 Reply to post | 课程内「讨论」列表页：按同学姓名找主帖，点进详情读案例和问题，在评论框回复（回复常在评论最后一页） |
| 作业截图汇总 Screenshot report | 课程「作业」列表页：逐份进结果详情页，把整页（题目、我的答案、每题得分）截成长图，汇总成 Word |

## Example prompts / 可以直接这样说

- 做作业："把这门课的作业都做了并提交。" — Do and submit all homework for this course.
- 刷视频："把章节内容里没看的视频都看完。" — Watch all unwatched chapter videos.
- 回讨论帖："帮我回复讨论区里 ××× 发的帖子，先把草稿给我看一下。" — Reply to ×××'s post; show me the draft first.
- 作业截图汇总："把每份作业的结果详情页都截图，要能看到每道题的答案和得分，汇总成一个 Word 给我。" — Screenshot every graded-result page with answers and scores, and bundle them into one Word file.

## Notes / 提醒

- 涉及个人情况的内容（专业、岗位、实习经历等）AI 不会编造，需要你如实告诉它。 Personal details are never invented; provide them yourself.
- 讨论回复发出后别人就能看到，先看草稿再确认发送。 Replies are public; review the draft before sending.
- 作业截图是逐份结果详情页的整页长图；待批作业显示 0 分多是老师还没批阅，不等于答错。 Screenshots are full-page captures of each result page; a pending 0 score usually means the teacher has not graded it yet, not that it is wrong.
- 单选、多选由系统自动判分；填空由老师人工批阅。 Single/multiple-choice are auto-graded; fill-in items are graded manually.
- **做填空前最好先准备本课程题库/标准答案**（PDF、往届答卷或截图），统一放到 `答案文件\` 目录（`E:\Doubao_AI_Output\在浙学\答案文件\`），AI 从这里读取。填空是教材原文措辞，联网搜不到答案；没有题库时 AI 不编造填空，会先做单选/多选，等你把答案放进该目录。仓库 `答案文件\` 下的 PDF 为已脱敏副本（页眉姓名、截止时间已遮挡）；原始含个人信息的答卷仅留在本地，不推公开仓库。 Fill-in items need a provided answer bank placed in the `答案文件\` folder; AI does not invent textbook wording without one. The PDF in the repo is a sanitized copy (name/deadline redacted); originals with personal info stay local only.

## Files / 文件

- `在浙学AI工具使用说明.md` — 中文详细使用说明 / Detailed Chinese usage guide
- Four `.zip` packages above — each is an installable Skill (`SKILL.md` + `references/browser-recipes.md`)
