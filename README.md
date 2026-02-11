[English](README.en.md) | **中文**

# OpenClaw Flowise Skill

这是 **OpenClaw** 的 Flowise 技能（Skill），用于通过 REST API 与 [Flowise](https://github.com/FlowiseAI/Flowise) AI 工作流交互。

## 功能

- 与 Flowise 聊天流（chatflows）对话：发送预测请求、流式响应、会话记忆
- 列出和管理可用 chatflows
- 支持在 `TOOLS.md` 中配置服务地址、API Key、Flow ID 及各 flow 的用途与参数

## 项目结构

```
.
├── SKILL.md           # 技能定义与 API 使用说明
├── scripts/
│   └── flowise.py     # Flowise API 命令行客户端
└── README.md
```

## 使用方式

- **在 OpenClaw 中**：安装本 skill 后，当用户提到 Flowise、chatflows 或想向 Flowise 机器人/代理发消息时，Agent 会使用本技能调用 Flowise API。
- **命令行**：可使用 `scripts/flowise.py` 直接调用 Flowise：

  ```bash
  # 发送预测
  python scripts/flowise.py predict --url http://localhost:3000 --flow-id <FLOW_ID> --question "你好"

  # 列出所有 chatflows
  python scripts/flowise.py list --url http://localhost:3000
  ```

## 配置

在 OpenClaw 的 `TOOLS.md` 中配置 Flowise 服务器地址、API Key、默认 Flow ID 以及各 flow 的用途与参数，详见 `SKILL.md`。

## 许可

与 OpenClaw 及 Flowise 的许可保持一致；具体以各自项目为准。
