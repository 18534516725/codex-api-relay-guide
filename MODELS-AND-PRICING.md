# 会员型号、价格和适用范围

核对日期：2026-11-02；只覆盖会员分组，单位为**平台虚拟美元 / 百万 Token**。这些是销售目录，不是 Claude Code 或 Codex 的兼容列表。目录共 20 个型号条目，包含版本和别名；不是20种独立能力。GPT、Claude、Grok 属于平台不同家族，客户端选择需另做协议与任务验收。

| 模型 ID | 展示名称 | 未缓存输入 | 输出 | 缓存读取 | 缓存写入 |
|---|---|---:|---:|---:|---:|
| claude-fable-5 | Claude Fable 5 | 10 | 50 | 1 | 12.5 |
| claude-fable-5-1 | Claude Fable 5.1 | 10 | 50 | 0.25 | 12.5 |
| claude-haiku-4-5-20251001 | Claude Haiku 4.5 | 1 | 5 | 0.1 | 1.25 |
| claude-opus-4-6 | Claude Opus 4.6 | 5 | 25 | 0.5 | 6.25 |
| claude-opus-4-7 | Claude Opus 4.7 | 5 | 25 | 0.5 | 6.25 |
| claude-opus-4-8 | Claude Opus 4.8 | 5 | 25 | 0.5 | 6.25 |
| claude-opus-5 | Claude Opus 5 | 5 | 25 | 0.5 | 6.25 |
| claude-opus-5-5 | Claude Opus 5.5 | 4 | 20 | 0.2 | 5 |
| claude-sonnet-4-6 | Claude Sonnet 4.6 | 3 | 15 | 0.3 | 3.75 |
| claude-sonnet-5 | Claude Sonnet 5 | 2 | 10 | 0.2 | 2.5 |
| claude-sonnet-5-5 | Claude Sonnet 5.5 | 2 | 10 | 0.1 | 2.5 |
| gpt-5.6-sol | GPT-5.6 Sol | 4 | 20 | 0.4 | 5 |
| gpt-5.6-terra | GPT-5.6 Terra | 2 | 12 | 0.2 | 2.5 |
| gpt-6-astra | gpt-6-astra | 10 | 50 | 1 | 12.5 |
| gpt-6-sol | GPT-6 Sol | 2 | 10 | 0.2 | 2.5 |
| gpt-6.1-sol | GPT-6.1 Sol | 2 | 10 | 0.1 | 2.5 |
| gpt-6.1-terra | GPT-6.1 Terra | 1 | 5 | 0.05 | 1.25 |
| grok-4.5 | Grok 4.5 | 2 | 6 | 0.3 | 未提供 |
| grok-4.6 | Grok 4.6 | 2 | 6 | 0.5 | 未提供 |
| grok-4.7 | Grok 4.7 | 2 | 6 | 0.5 | 未提供 |

平台虚拟美元不是现金美元，不能提现，也不应与其他平台额度按1:1比较。型号名称来自平台目录，不是对外部版本的独立认证。未提供价格不等于免费；缓存写入时效、长上下文分档及额外收费应另核对。

会员只覆盖对应分组的指定文本模型，不含图片、视频、音频；普通分组和历史周期不能直接套表。套餐、有效期、并发与重购规则见 [README](README.md)。

机器可读来源见 [pricing-snapshot.json](pricing-snapshot.json)，销售积分字段按100积分/平台虚拟美元换算。[公开会员模型配置](https://www.nexotoken.net/api/models/config?channel=membership)是事实核对来源，未使用获客参数。
