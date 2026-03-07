### Simple Test / Validation
```markdown
Create a folder called MOMMY_MIA
In that folder create a readme.txt with the contents:
Hello, you are reading me.
Verify the file exists, then report back with the file path.
```


### Coder Agent Setup
```markdown
Create a new Agent called coder.  He should be a software developer.  Give him the proper tools and model so that he can write software. Report back when complete including what you set up for him.
```


These were fed into OpenAi Codex
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

## Mission Control
```markdown
Programming task. Follow ROUTER.md exactly (Sarah spec → Johnny implement → Sarah verify → Jess notify → final response).

Goal: Create “Mission Control” running locally on the OpenClaw machine.

Hard constraints:
- Johnny must create the project under: ~/openclaw-sandbox/mission-control
- Use Next.js (App Router) + TypeScript.
- Port: 3010 (do not use 3000).
- Deliverable must be runnable immediately after creation.

UI requirements (MVP):
- Home page at / with title “Mission Control”
- 3 cards: Tools, Agents, Jobs
- Each card links to /tools, /agents, /jobs
- /tools page: list placeholder “No tools yet”
- /agents page: list placeholder for Jess/Sarah/Johnny
- /jobs page: list placeholder “No jobs yet”
- Simple clean styling (basic CSS or Tailwind if you want, but keep it minimal).

Pipeline requirements:
1) Sarah: produce a spec + acceptance criteria checklist.
2) Johnny: implement, install deps, start dev server in background, write server.pid and server.log in the project root.
   - Must prove it’s up with: curl -s http://127.0.0.1:3010/ | head
3) Sarah: verify by running commands (ls, cat server.pid, curl) and return PASS/FAIL with evidence.
4) Jess: send a Telegraph message “✅ Mission Control MVP complete” including PATH and URL.
5) Jess: final reply to me must be ONLY:
   PATH=<absolute path>
   URL=http://127.0.0.1:3010/
No other text.
```