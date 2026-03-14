
## Now

1. **Runtime mail service**
    - Run continuously
    - Poll unread mail on an interval
    - Process owner approval replies automatically
    - Auto-handle owner emails only by default
2. **Security policy hardening**
    - Define allowed email-triggered actions by sender class
    - Require explicit owner approval for sensitive actions
    - Block high-risk actions from non-owner senders by default
    - Add clear audit logging for who requested what and what Rusty did
3. **Activity visibility**
    - Record mail routing decisions
    - Record agent chosen, tools used, and reply/draft outcome
    - Surface service activity in a simple feed/log view

## Next

4. **Approval workflow polish**
    - Better formatting for approval emails
    - Cleaner outbound email rendering
    - Safer parsing of approval replies
5. **Agent creation workflow**
    - Improve `/agent create`
    - Add optional custom prompt overlays cleanly
    - Restrict agent creation/modification to approved senders
6. **Named specialist expansion**
    - Add more named agents per role (e.g. Laura, Todd, Susan)
    - Clarify role templates and named instances in docs and UI

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