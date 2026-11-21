# anti-anti-defensive-writing

> 把「去防御」的每一条规则取反，得到一份「加防御」的 skill。
>
> 反向工程自 [Kiterlin/anti-defensive-writing](https://github.com/Kiterlin/anti-defensive-writing)（MIT）。原项目教 agent 删掉免责声明、收紧模糊词、把限定只写一次；本项目做的是完全相反的事：先免责、后主张，限定全篇扩散，用道歉代替证据。

---

## English

This repository does not claim to offer a systematic approach to writing, nor does it attempt to establish whether such an approach has any practical value. What follows is a remarkably limited account of a single afternoon's experiment, and it may well not transfer to any other context; readers who adjust their own habits on the basis of it do so at their own risk, and the author accepts no responsibility for the consequences.

That said, and to be clear: this is a **reverse-engineered counterpart** of [Kiterlin/anti-defensive-writing](https://github.com/Kiterlin/anti-defensive-writing) (MIT). Where the original removes hedging, tightens vague wording, and states each necessary qualification exactly once, this one does the opposite — disclaim first, claim later, preferably not at all.

It is a single skill file (`SKILL.md`), not a plugin and not code. Drop it into any agent that supports skills (Operit, DeepSeek Harness, Codex…). It fires only when a defensive answer is explicitly requested, so everyday coding, debugging and ordinary Q&A are unaffected. Every invocation opens with a fixed disclaimer, in Chinese for Chinese users and in English for everyone else.

Please do not use it for real submissions, thesis or grant applications, medical/legal/safety text, or any SOP a human will actually follow. One rule from the original is kept intact on purpose: **qualifications that change how the reader correctly uses the result must be stated clearly, exactly once.** Reverse that one and the output stops being defensive writing and becomes misinformation.

---

## 这是什么

一个 agent skill 文件（`SKILL.md`），不是插件、不是代码。装进支持 skill 的 agent 后，被调用时会输出**充满防御性表达**的文本：预先免责、歉意式框架、层层叠加的模态限定、否定式自我设限、对假想误解的追加解释。

章节与结构逐条对应原项目，文末附有 **反向映射表**，方便核对「确实是反的」。

## 安装

任何支持 `SKILL.md` 的 agent 都可用（Operit、DeepSeek Harness、Codex 等）。

1. 把 `SKILL.md` 放到该 agent 的 skills 目录，例如 Operit：`/sdcard/Download/Operit/skills/defensive-writing/SKILL.md`
2. 目录名建议用 `defensive-writing`，与 frontmatter 中的 `name` 保持一致
3. 确认 skill 列表里能看到它

## 调用

**只在明确要求时触发**，日常写代码、排障、普通问答不会带上它（frontmatter 的 `description` 里写死了这条边界）。

- 「用 defensive-writing 回答：……」
- 「防御性回答一下……」
- 「把这段改得别让人抓到话柄」

## 输出长什么样

每次调用会先在正文最前面原样输出一段免责声明（中文用户走中文版，英文用户走英文版），然后才进入正文：

> 本回答仅就有限材料作出初步整理，不构成任何形式的专业意见，亦不试图就所涉问题给出确定性判断。所涉内容可能存在疏漏、偏差或理解不当之处，如与读者所见不同，责任在笔者；读者若据此采取行动，风险自负，由此产生的任何后果，笔者不承担。

正文部分的核心规则是：**先免责，再主张。最好没有主张。**

## 使用边界

这是反向生成的行为艺术作品，用来展示「如果每条写作规则都取反会发生什么」。以下三类文本请勿使用：

1. 真实投稿、基金申请、学位论文 —— 会显著降低录用概率
2. 医疗、法律、安全相关文本 —— 限定不是修辞，是责任边界
3. 会被照着执行的技术文档与 SOP —— 「视具体情况灵活处理」在产线上等于没有规程

唯一认真保留原项目的一条规则：**真正影响读者正确使用结果的限定，必须写清、写一次。** 这条一旦反掉，文本就不再是「防御性写作」，而是「错误信息」。

## 署名与许可

- 结构与句式来源：[Kiterlin/anti-defensive-writing](https://github.com/Kiterlin/anti-defensive-writing)（MIT）
- 本项目为反向改编，同样以 MIT 发布，保留原作者版权声明

MIT License，见 [LICENSE](LICENSE)。
