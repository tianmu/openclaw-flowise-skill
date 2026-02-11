[中文](README.md) | **English**

# OpenClaw Flowise Skill

A **Flowise** skill for **OpenClaw** that interacts with [Flowise](https://github.com/FlowiseAI/Flowise) AI workflows via REST API.

## Features

- Talk to Flowise chatflows: send prediction requests, streaming responses, and conversation memory
- List and manage available chatflows
- Configure server URL, API key, flow IDs, and per-flow usage/parameters in `TOOLS.md`

## Project Structure

```
.
├── SKILL.md           # Skill definition and API usage
├── scripts/
│   └── flowise.py     # Flowise API CLI client
└── README.md
```

## Usage

- **In OpenClaw**: After installing this skill, when users mention Flowise, chatflows, or want to send messages to Flowise bots/agents, the agent will use this skill to call the Flowise API.
- **Command line**: Use `scripts/flowise.py` to call Flowise directly:

  ```bash
  # Send a prediction
  python scripts/flowise.py predict --url http://localhost:3000 --flow-id <FLOW_ID> --question "Hello"

  # List all chatflows
  python scripts/flowise.py list --url http://localhost:3000
  ```

## Configuration

Configure Flowise server URL, API key, default flow ID, and per-flow usage/parameters in OpenClaw’s `TOOLS.md`. See `SKILL.md` for details.

## License

Follow the licenses of OpenClaw and Flowise respectively.
