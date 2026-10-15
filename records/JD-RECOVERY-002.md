# JD-RECOVERY-002 v1.1：无敏感能力验证恢复点
更新时间：2026-10-15 18:35 北京时间（UTC+8）。测试记录；不包含业务PRD或客户资料。

## 决定与依据
决定：家点先完成能力验证，通过后再接续项目资料；本轮不学习全案、不开发网站。
依据：需求提出及决定人的 JD-RECOVERY-002 v1.1 启动要求，先验证实际执行、读取、交付、保存恢复；不得将本地commit当成远端灾备。
本轮仅一个助手，不创建智能体。旧对话及私有文件未迁移，也未完整学习。

## 已做与限制
- 实际执行成功；/workspace/jiadian-intended-guardianship，origin 与预期一致；初始分支 work，初始提交 0b704030b444422b8443861b599928fa7b21d99d，初始无未提交修改；已有文件仅 README.md，未发现 AGENTS.md。
- 实际磁盘约30G可用，内存约17G可用；仅为当时快照。
- 自建TXT、中文DOCX（正文、表格、嵌图）、一页中文PDF、ZIP生成与回读成功；PDF已渲染目视检查中文，PNG排版已目视检查。
- 样图由Pillow实际排版，未调用图像生成工具。英文OCR实测通过；Tesseract只有eng/osd，中文扫描OCR未通过测试。图片型PDF正文提取为空，不能冒充文本PDF读取成功。
- 自建小样只能证明小样链路，用户真实上传入口、旧版DOC、复杂PDF/表格等待首次实际资料验证。
- 公开正文：WHO《About WHO》https://www.who.int/about ，2026-10-15访问，可读，提取内容为WHO成立于1948年。
- 官方法源访问：政府网 https://www.gov.cn/xinwen/2020-06/01/content_5516649.htm 返回403；人大网 https://www.npc.gov.cn/npc/c2/c30834/202006/t20200602_306457.html 超时。官方现行法源正文与时效性未验收；未作法律结论。
- 样本、脚本、校验JSON位于 /workspace/scratch/jd-recovery-002（权限700），不进入公开仓库。不是完整私有灾备。/mnt/data创建被拒绝，已采用工作目录下私有测试目录；用户可下载交付仍需界面实际验证，文件路径本身不算交付成功。
- 远端推送与独立取回验收见本聊天实际命令回执；本文件写入时尚未执行。跨环境取回、跨轮恢复均未通过验收。

## 恢复步骤与下一步
下一轮收到“恢复测试”，先重新读取 records/INDEX.md 和本文件，再回答决定、依据、已做/未做与下一步，不仅依赖聊天。云环境丢失时，从 test/jd-recovery-002 分支读取这两个文件；具体远端提交以实际回执为准。
本轮已完成从文件回读决定的检查，真正跨轮测试须下一条消息执行。
下一步：完成恢复测试；确认附件实际下载；落实私有资料持久保存、权限和独立取回方案，再由Lara确认资料接续；无需专门为测试上传材料。

## 未来协作基础（未启动）
权威索引与决定独立于聊天；任务可记录：负责人、输入、成果、状态、依赖、审核人及审核结论。
Git worktree list及Git版本只读检查成功；独立分支已实际使用，未创建额外worktree。worktree不代表智能体调度或共享记忆，并发及跨环境权限未来实际联测。
未来规则：按任务独立分支；先审核后合并；冲突保留双方依据由负责人处理；不覆盖他人修改、不强推；临时文件只清理由自己创建且确定不需保留的部分。审核、合并、冲突与回收流程均尚未实测。
权限边界：公开仓库仅无敏感测试记录；业务PRD、内部研究、客户资料、凭据不得进入。各参与者仅访问获准资料，共享范围须逐任务明确。

## 行政工具边界
已发现本地执行/文件、GitHub、公开网页、Pages、Google Drive/Docs/Sheets/Slides、Gmail、Google Calendar、Slack工具入口；除本轮明确实测的功能外，入口存在不等于账号授权与能力验收。邮件/日历/Drive账号连接与授权待实际使用前只读核查，Outlook工具当前未见。
本轮未发邮件、未联系他人、未发布内容、未建日程、未更改权限凭据网络、未部署或安装软件。

## 远端验收增量
2026-10-15T18:34:39.131096+08:00：初次记录提交 0be0c663687935f31fd777905eb11b39d5b13b8f 已推送 test/jd-recovery-002。另建空 bare 仓库从 origin 浅取回，FETCH_HEAD 与该提交完全一致，并重新读取索引和决定；GitHub连接器也独立回读索引成功。这证明远端可取回，但 bare 仓库仍在同一云环境，不证明真正跨环境或跨轮恢复。附件交付仍待界面下载确认。

## 独立跨轮恢复与附件最小补正（本轮实测）
时间：2026-10-15T03:39:39.474776-07:00（America/Los_Angeles）。
- 本轮实际执行 git fetch origin refs/heads/test/jd-recovery-002:refs/remotes/origin/test/jd-recovery-002，退出码0；git rev-parse refs/remotes/origin/test/jd-recovery-002 返回 68d18e4e2239814001d7b6fe0f9024aed6bd8c67，与首轮报告一致。
- 随后分别执行 git show refs/remotes/origin/test/jd-recovery-002:records/INDEX.md 与 git show refs/remotes/origin/test/jd-recovery-002:records/JD-RECOVERY-002.md，实际读取全文后恢复决定、依据、已做/未做和下一步。本轮跨轮文件读取通过；不是跨环境全案灾备验收。
- 文件实际值：决定仍为“家点先完成能力验证，通过后再接续项目资料；本轮不学习全案、不开发网站。”依据仍为 JD-RECOVERY-002 v1.1。私有资料持久保存与独立取回方案仍为“尚未建立”。
- 原TXT/PDF/DOCX/ZIP仍在本地；本轮未重做、未重测内容。检查当前全部工具元数据及原生附件接口：codex_app__list_artifacts 返回 artifacts=[]；attach_artifact只支持pull_request，不支持任意文件。
- 存在 chatgpt_space_write_page_reference：可向已授权可写Page的规范Files目的地上传（最大10MiB），必填真实page_id和本地file，成功后可返回持久reference、sha256、file_access_confirmed。当前没有已选定、获准的目标Page，未调用上传，未创建新Page/工作台。upload_artifact_images只面向已有原生表格/演示/Canvas图片，不是通用附件交付。
- 当前未发现独立的“本地任意文件→本聊天附件/个人Library可下载文件”发布接口。download_file是入站下载，不是出站发布；/workspace/library-files为空，目录本身不证明Library发布能力。Drive/Slack上传属于外部目的地，不等于原生附件，本轮未使用。
- 补正：上一轮本机文件链接不是原生交付回执。当前原生附件交付仍受阻，无file_id、持久附件引用或用户下载成功回执，不要求用户重复点击本机路径。
- 下一步由协调方落实已授权的现有可写Page目的地，或提供支持直接文件发布的原生工具；然后仅上传原无敏感测试文件并按实际回执验收。私有全案保存方案、中文扫描OCR、官方法源和真正跨环境恢复仍未验收。
- 本轮不改main，不迁移全案、不新增工作台、不扩权限、不付费、不改名、不联系他人。
