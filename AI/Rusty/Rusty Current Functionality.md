## Core Runtime

- REPL-based local runtime via `cargo run`
- Multi-agent routing based on agent config and keywords
- Named agents with `display_name` and `role`
- Manual agent pinning with `/agent <name>`
- Model switching with `/model <name>`
- Tool execution for shell, browser, file, scaffold, start, and delegation flows

## Agent System

- Agent definitions live in `agents/*.toml`
- Role instructions live in `prompts/*_prompt.toml`
- Named agents can share role prompts
- Built-in named/role agents:
    - `default` / `Rusty`
    - `developer` / `Jack`
    - `researcher` / `Researcher`
    - `coder` / `Coder`
    - `cindy` / `Cindy`

## Agent Creation

- `/agent create <role> <name> [extra]`
- Creates a named agent from an existing role template
- Supports a custom prompt overlay when extra instructions are provided

## AgentMail

- `.env`-based API key loading
- `/mail status`
- `/mail unread [limit]`
- `/mail get <id|n>`
- `/mail read <id|n>`
- `/mail reply <id|n> <text>`
- `/mail assist <id|n>` — routes the email through the agent system, returns `Summary`, `Action`, and `Reply Draft`
- `/mail handle <id|n>` — routes mail to an agent; replies directly if sender is the owner, otherwise creates a draft and emails owner for approval
- `/mail approvals sync` — processes approval emails from owner; supports:
    - `send`
    - `no`
    - `update to say ... then send`

## Mail Routing & Reply Rules

- Owner email configured in `config.toml`
- Owner emails answered directly
- Non-owner emails go through draft + approval flow
- Mail routing prints the selected agent

## Service Mode

- `cargo run -- service`
- Polls mail on an interval
- Auto-processes approval emails and handles owner emails
- External mail auto-handling is disabled by default

## Evaluation & Tests

- `cargo nextest run`
- Unit tests for parser, agent runtime, and tool runtime
- Integration tests for config loading, routing, and mocked turn flows

## Known Gaps

- Outbound email formatting needs refinement in some markdown-heavy cases
- External sender security policy needs to be stricter and more explicit
- Service activity logging is basic
- No control center UI
- No Telegram connector