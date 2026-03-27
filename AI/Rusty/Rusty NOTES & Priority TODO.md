

3/26/2026 & 3/27/2026

- Workflow improvements
	- [x] add task from epic -> prepop project+epic in task ✅ 2026-03-26
- Tweaks
	- [x] header on list view still not right color ✅ 2026-03-26
	- [ ] limit next step to single line with... when more text, hover should tooltip the value (desktop only)
	- [ ] collapse queued in board by default to allow other lane cards to be larger
		- should show QUEUED vertically with a count
- Mobile
	- [x] have menu collapse to hamburger ✅ 2026-03-26
	- [ ] listing card 
		- should go full width, no rounding
		- no padding top/bottom - bar should sit flush with above/below bar
- Tasks
	- [ ] date/time attachment added, sort desc
	- [ ] go back to task detail ux mockup, overview looks lit, update to match
- QOL
	- [x] make it so the project-id, task-id, any-id gets copied to clipboard when you click on it in the breadcrumb ✅ 2026-03-26
	- [ ] put 'refresh' button with project/epic so lists update 
		- this is helpful when say I start creating a new task and realize I need a new epic
- Security
	- start lockdown
		- [ ]  set a pin, encrypt local
		- [ ]  require pin when access memory tab
- Chat
	- [ ] make my text in gray bkgagent response text no bkg
- Re-UX
	- [x] Dashboard ✅ 2026-03-27
	- [x] Board ✅ 2026-03-27
	- [x] Main Mission ✅ 2026-03-27
	- [x] Scheduled.. ✅ 2026-03-27
	- [ ] Memory
	- [ ] Activity
	- [ ] Logs
	- [ ] Forms
		- ensure memory changes to form, currently is a window prompt (gross)
- Need way to 'wake' up pc with 3090 to process scheduled tasks

---

3/20/2026
- ugh it got all fucked up trying to change workflow
- next tickets
	- remove mission/success from Teams

3/19/2026
Current Issues that need resolved
- Project/Task workflow & UI need reworked
- Its tedious to create tasks for a project, have to create project then go create tasks and select that project. Ability to add n number of tasks easily for a given project.
- Fix non-alignment for Project / Task -> Project can have a team but we select Assignee for a Task (since project is not required)
	- Don't show completed projects in task assignment dropdown or this will get unwieldy quick. Maybe this is for easy quick assign but hidden by default? That makes sense if no project and/or we drive it by project - so that could work as a assign/re-assign project
- 

---
3/17/2026
- I need better project/task, a bit closer to Jira
	- I thought I needed Epic but I DO NOT
		- Project -> task (epic) -> subtasks (already on Task as deliverables)
- I asked Rusty 'what was that bread recipe' thinking it would have no idea...
	- it returned: "Here’s the full “Five Dutch‑oven sandwich‑bread family recipes” that were saved in the task “task‑1773678821817”:" -- with the actual results!!! that was surprising.


---
TODO
- [x] Compare Rusty NOTES & Priority TODO vs. whats currently tasked and see if anything from here is missing. 📅 📅 2026-03-19 ✅ 2026-03-23


Most of the below items are now tasks in Rusty, but lets review and cleanup.

---

Notes
- model evaluations
	- https://www.canirun.ai/
	- check that against avail gpu
- specialized agent for updating Rusty
	- uses design system
	- uses architecture
	- can sandbox and validate changes
	- can put up PR with proofs
	- noticed Codex is open source -- see about using this
- agent 1:1's
	- agent asks what its done well, where it could use improvement
	- agent updates its LTM

## Later

7. **Control Center**
    - Inbox
    - Tasks
    - Activity feed
    - Agent status
    - Cron/jobs
    - Connectors
8. **Telegram integration**
    - Mobile command path
    - Approval actions from phone
    - Status summaries and notifications
9. **Team orchestration**
    - Multiple researchers/developers on one mission
    - Explicit team files/config
    - Delegation and comparison workflows

## Not Now

10. **Deep self-modifying agents** — no silent prompt drift, no opaque "learning" that changes behavior without review
11. **Broad external automation for arbitrary senders** — keep automation conservative until the security model is explicit