# Codex 自定义 provider：配置模板与回滚

以下是依据 2026-11-02 [官方配置参考](https://learn.chatgpt.com/docs/config-file/config-reference)整理的字段模板；不是已完成 NexoToken 调用验收的安装脚本。真实端点和模型需按当前平台说明替换。

## TOML 模板

```toml
model = "REPLACE_WITH_CURRENT_MODEL_ID"
model_provider = "relay_example"

[model_providers.relay_example]
name = "Relay example"
base_url = "https://gateway.example.invalid/v1"
env_key = "NEXOTOKEN_API_KEY"
wire_api = "responses"
requires_openai_auth = false
```

`gateway.example.invalid` 是保留的无效示例域名。`REPLACE_WITH_CURRENT_MODEL_ID` 明确表示待由读者填写的真实目录 ID，不是一个可调用模型。不要把 Key 写进 TOML 或仓库；`env_key` 这里只填环境变量名称。

当前官方参考为自定义 provider 的 `wire_api` 列出 `responses`；名称使用自定义 ID，避免覆盖保留的内置 ID。`requires_openai_auth = false` 用于对应网关自己的 Key 鉴权，并不保证该服务已实现协议所需的全部功能。

修改实际使用的配置文件前先备份，把 provider、model 和来源逐项对应。不要直接用本片段替换整份配置。CLI、编辑器入口和桌面入口有不同运行环境，终端设置的变量是否传入目标进程需要自己确认。

## 第一次启动要验证的内容

1. 记录版本和当前选择的模型。
2. 在没有敏感信息的测试目录执行小任务。
3. 检查完整响应、工具调用和测试结果。
4. 核对 usage 与平台对应分组的扣额。

不要为了连通而关闭本机权限限制、扩大工具执行权限或反复增加重试次数。模型入口问题和本地工具权限问题应分别排查。

## 回滚

恢复修改前的配置副本，或只移除本次新增 provider 及相关选择项；不要删除整个配置目录、所有凭证或历史会话。若环境变量原先不存在，只撤销本次新增的变量；原有变量恢复原值。

NexoToken 的具体接入说明见[现有 Codex CLI 教程](https://github.com/18534516725/llm-api-setup-guides/blob/main/guides/coding-tools/codex-cli.md)。本页不保存或读取读者的实际 Key。
