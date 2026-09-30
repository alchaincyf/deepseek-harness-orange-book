**中文** | [English summary](#english-summary)

<p align="center">
  <img src="banner.png" width="44%" alt="DeepSeek Harness 橙皮书封面" />
</p>

# DeepSeek Harness：从开机到拆开

> 橙皮书系列 · 花叔 著 · v260814（2026年8月14日）

一个不写代码的人，把一个刚出厂24小时的agent框架装在自己机器上跑穿了。这本书记录它此刻的样子。

2026年8月13日，DeepSeek开源了agent框架Harness（MIT协议，发布当天开源）。官方发布稿的主语从头到尾是「它」——它怎么造的、它是什么架构。而这本书把主语换回「我」：我装上之后第一件事干什么、会不会花我的钱、会不会动我硬盘上别的文件。

## 🎬 15秒发布动画

<p align="center">
  <img src="launch-film.gif" width="80%" alt="DeepSeek Harness橙皮书 · 15秒发布动画" />
</p>

<p align="center">
  <em>使用DeepSeek官方VI · 由<a href="https://github.com/alchaincyf/huashu-design">Huashu-Design</a>设计制作</em><br/>
  <a href="launch-film.mp4">⬇ 下载1080p60 MP4（含音效）</a>
</p>

## 🎥 60秒能力演示

四段真实能力，全部对应书里的一手实测：开机装载129个插件 → 写入前的权限审批 → PTC让模型直接写程序编排工具（5次开口15次操作）→ 创造模式现场给自己造出第33个工具`count_chinese`，最后把整个终端拆成积木。

<p align="center">
  <a href="launch-film-60s.mp4"><img src="launch-film-60s-preview.jpg" width="88%" alt="60秒能力演示预览：开机 · PTC · 创造模式 · 拆开" /></a>
</p>

<p align="center">
  <a href="launch-film-60s.mp4">▶ 观看60秒完整版（1080p60 MP4，含音效）</a>
</p>

## 📑 杂志编辑风幻灯片（20页）

不想读整本书？这套20页的杂志编辑风deck是全书的浓缩版：五个章节、进门四问、成本账单、44条事件、PTC、创造模式、拆开看架构，一页一个结论，适合快速过一遍或拿去做分享。

<p align="center">
  <a href="DeepSeek-Harness-Orange-Book-Magazine-Deck.pptx"><img src="magazine-deck-preview.jpg" width="88%" alt="杂志编辑风幻灯片预览：封面 · 事件流 · 创造模式 · 结论" /></a>
</p>

<p align="center">
  <a href="DeepSeek-Harness-Orange-Book-Magazine-Deck.pptx">⬇ 下载PPTX（20页 · 11MB）</a>
</p>

## 下载

| 格式 | 文件 | 大小 |
|------|------|------|
| PDF | [**DeepSeek-Harness-Orange-Book-zh-v260814.pdf**](DeepSeek-Harness-Orange-Book-zh-v260814.pdf) | 13MB |
| EPUB（微信读书优化版） | [**DeepSeek-Harness-Orange-Book-zh-v260814.epub**](DeepSeek-Harness-Orange-Book-zh-v260814.epub) | 5.4MB |
| HTML（单文件，图片已内联） | [**DeepSeek-Harness-Orange-Book-zh-v260814.html**](DeepSeek-Harness-Orange-Book-zh-v260814.html) | 4.9MB |

> 💡 PDF建议下载后阅读，GitHub在线预览可能无法完整渲染。

## 这本书有什么官方文档里没有的

全部一手实测，跑在作者自己的电脑上：

- **完整系统提示词**——每次开口之前被灌进模型脑子里的那一大段话
- **129行出厂启动清单**——`dsh --profile web --dump-default-config`导出，一行行看它开机装了什么
- **三份原始会话日志**——标准模式、PTC、创造模式各一份，一条事件都没删
- **AI现场给自己造工具的全程**——19步，工具清单从32行变成33行，多出来的那一行是它自己写的
- **PTC实测账单**——5次开口编排15次操作，以及那笔反直觉的账：固定开销反而涨9%
- **35个不随产品安装的扩展包清单**——都在npm上，但不在安装闭包里，「仓库里有」不等于「装上就有」
- **代码库考古**——12,293次提交/约64天、683篇Agent Note、4篇事故复盘（含「100%覆盖率全绿，编辑器一连上就崩」）

## 本书结构

| 部分 | 内容 |
|------|------|
| **序章** | 探索未至之境：你装的到底是什么，以及替你做掉那道四选一 |
| **Part 1 进门** | 十分钟干成第一件活 · 它被允许碰什么 · 四种模式人话版 · 从Claude Code搬家，哪些能直接用 |
| **Part 2 主线** | 每一次运行都有迹可循 · 一次任务多少钱 · 它给自己长出一只手 · 让模型写程序及那笔反直觉的账 · 让它自己干完一件长活 |
| **Part 3 地基** | skill、MCP、插件到底谁管谁 · 两个插件都想管文件编辑谁赢 · 它出过什么事 |
| **Part 4 收** | 一个几乎全由AI写出来的代码库长什么样 · 它在赌什么，代价是什么 |
| **附录** | 数字基准表（每个数字带命令和快照时间）· 术语对照 · 命令速查 · 迁移总表 |

每节末尾有个固定小栏目：**《他们本来想这么做，后来没做》**——取自仓库里被否决的设计方案，回答「为什么这里没有X」。

## 适合谁读

- **不写代码、但用过Claude Code / Codex / OpenClaw这类工具的人**：每个概念一句技术定义+一个日常类比+类比在哪失真
- **业内工程师**：一手材料是自己跑出来的日志、被否决的方案、事故复盘的考古，不是发布稿的转译
- **想评估要不要迁移的人**：能直接用/要自己装/用不了，逐项实测（`~/.agents/skills`被零配置读走这种事，文档不会告诉你）

书里凡是卡住作者的地方都原样写下来了——顺的过程没什么可信度，卡住的地方才有。

## 关于时效

这本书写于Harness发布后的24小时内，书里凡是从网上取的数字（star数、包数量）都只是按下回车那一刻的样子，正文里标了取数时间。实测部分（系统提示词、日志、启动清单）随版本演进可能变化，复现时以你本机输出为准。

## 橙皮书系列

面向AI Native Builder的实战指南系列：

- Claude Code 从入门到精通
- Claude Code 源码解析
- Harness Engineering
- Agent Skills
- OpenClaw：养一只你自己的AI
- Polymarket 指南
- [OpenAI Codex 从入门到精通](https://github.com/alchaincyf/codex-orange-book)（中英双版）
- **DeepSeek Harness：从开机到拆开** ← 你在这里

完整合集见[huasheng.ai](https://www.huasheng.ai/)。

## 友情链接

同一个生态里的项目：

| 项目 | 简介 | 链接 |
|------|------|------|
| DeepSeek Harness Desktop | 为DSH生态做的桌面端，把Harness装进图形界面里跑。 | [GitHub](https://github.com/anywhere-labs/deepseek-harness-desktop) · [官网](https://dshdesktop.cn) |
| Awesome DeepSeek Harness | DSH终极指南：快速入门、资源推荐、精选插件与工具，中英日三语。 | [GitHub](https://github.com/libukai/awesome-deepseek-harness) |
| OrcaPromptVault | 跨产品的系统提示词与工具 schema 归档，其中 dsh 那份是另一台机器上的独立实抓，带日期与复现命令，可与本书第一章的提示词互相核对。 | [GitHub](https://github.com/Continuum-AI-Corp/OrcaPromptVault) |

## 关于作者

**花叔（HuaShu）** · AI Native Coder · 独立开发者

小猫补光灯（App Store付费榜第一）的开发者，橙皮书系列作者，全平台50万+读者。所有产品全部用AI完成，从未手写过一行代码。CCTV《焦点访谈》报道的「手搓经济」代表人物。

- X/Twitter：[@AlchainHust](https://x.com/AlchainHust)
- YouTube：[@Alchain](https://www.youtube.com/@Alchain)
- B站：[花叔v](https://space.bilibili.com/14097567)
- 微信公众号：花叔
- GitHub：[@alchaincyf](https://github.com/alchaincyf)
- 官网：[huasheng.ai](https://www.huasheng.ai/)

## English summary

**DeepSeek Harness: From First Boot to Teardown** (Chinese edition) — written within 24 hours of DeepSeek open-sourcing its agent harness (Aug 13, 2026, MIT license). The author — who has never hand-written a line of code — ran it end to end on his own machine and documented what the official docs don't show: the full system prompt, the 129-line default boot manifest, three unedited session logs, and a live recording of the AI building a new tool for itself (19 steps, tool list going from 32 to 33 lines). Chinese only for now.

## 📚 在线阅读（WorkBuddy）

本书已同步到 WorkBuddy 资料库：每章一个网页，也可以直接把链接丢给你的 Agent 当上下文。

https://www.workbuddy.cn/space/d/XABVjoKqAElOoh6PgTgjeM

全部橙皮书入口：https://www.workbuddy.cn/space/d/YcllWXknAUoMk6lFSWdfbI

## 协议

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">
  <img alt="CC BY-NC-SA 4.0" src="https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png" />
</a>

本作品基于[CC BY-NC-SA 4.0](http://creativecommons.org/licenses/by-nc-sa/4.0/)协议发布。在保留署名的前提下，可自由分享和改编（非商用）。
