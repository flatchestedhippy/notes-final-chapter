
### Agent Mail
https://x.com/_sean_matthew/status/2028902126005653889
```markdown
Set up AgentMail for my OpenClaw agent.

The AgentMail skill docs and reference are at:
https://clawhub.ai/adboio/agentmail

Make sure to:
1. The AgentMail skill is already installed via clawhub (if not installed, please do so)
2. Configure the AGENTMAIL_API_KEY in my openclaw.json.  My key is: am_us_6aad9363dd2a84b2171b7b19988121e55081679248dae49cdd0b6497eb0d088c
   under skills.entries.agentmail
3. My agent's inbox is: jess-nexy@agentmail.to
4. Install the Python SDK (pip install agentmail python-dotenv)
5. Test sending and receiving an email
```

### QMD (Memory Recall)
https://x.com/_sean_matthew/status/2028902126005653889
```markdown
Set up QMD as the memory backend for my OpenClaw agent.
Follow the official docs here:
https://docs.openclaw.ai/concepts/memory#qmd-backend-experimental

Make sure to:
1. Install the QMD CLI
2. Install SQLite with extension support if needed
3. Configure memory.backend = "qmd" in my openclaw.json
4. Add my workspace memory files as a QMD collection
5. Run the initial embed so models are downloaded and
   the index is built
6. Verify it works by running a test query
```


### Agent Browser
https://x.com/_sean_matthew/status/2028902126005653889
```markdown
Install the agent-browser skill for my OpenClaw agent.

The agent-browser SKILL.md and reference docs are at:
https://github.com/vercel-labs/agent-browser/tree/main/skills/agent-browser

Follow the OpenClaw skills docs here:
https://docs.openclaw.ai/tools/skills

Make sure to:
1. Install the agent-browser skill into ~/.openclaw/skills/agent-browser/
   so it's available to all my agents
2. Include the SKILL.md and any reference docs from the repo
3. Verify the skill shows up as eligible
4. Whenever my agent needs to access the internet or browse a
   web page, it should use agent-browser
```

