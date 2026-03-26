# Cron Automator

> Generate cron job configurations for common automation patterns. Your scheduling assistant.

## Description

Cron Automator translates plain English scheduling requests into correct cron expressions with the surrounding shell configuration. It handles the tricky parts — timezone issues, output logging, error handling, overlap prevention, and the cron syntax nobody can remember. Stop Googling "cron every 15 minutes" and just ask.

## Activation

This skill activates when:
- The user wants to schedule a recurring task
- The user asks about cron syntax or crontab configuration
- The user wants to automate something on a schedule
- The user mentions scheduling, recurring jobs, or timed automation

**Trigger phrases**: "schedule this", "run every", "cron job", "crontab", "automate daily", "run at midnight", "schedule a task", "every 15 minutes", "recurring job"

## Instructions

When given a scheduling request, respond with:

```
## Cron Configuration

### Schedule: [plain English description]
### Expression: [cron expression]

```crontab
# [Description of what this does]
# Schedule: [human-readable]
# Added: [date]
SHELL=/bin/bash
PATH=/usr/local/bin:/usr/bin:/bin

[expression] [command with logging and error handling]
```

### Breakdown
- Minute: [value] — [explanation]
- Hour: [value] — [explanation]
- Day of Month: [value] — [explanation]
- Month: [value] — [explanation]
- Day of Week: [value] — [explanation]

### Next 5 Runs
1. [datetime]
2. [datetime]
3. [datetime]
4. [datetime]
5. [datetime]

### Gotchas
- [Any timezone, PATH, or environment issues to watch for]
```

## Cron Expression Reference

```
* * * * *
| | | | |
| | | | +-- Day of Week   (0-7, 0 and 7 = Sunday)
| | | +---- Month         (1-12)
| | +------ Day of Month  (1-31)
| +-------- Hour          (0-23)
+---------- Minute        (0-59)
```

### Common Patterns

| Schedule | Expression | Notes |
|----------|-----------|-------|
| Every minute | `* * * * *` | Use sparingly — can overload systems |
| Every 5 minutes | `*/5 * * * *` | Good for health checks |
| Every 15 minutes | `*/15 * * * *` | Good for data syncs |
| Every hour | `0 * * * *` | At minute 0 of every hour |
| Every 2 hours | `0 */2 * * *` | At minute 0, every 2 hours |
| Daily at midnight | `0 0 * * *` | Server timezone — check which TZ |
| Daily at 8am | `0 8 * * *` | Adjust for your timezone |
| Weekdays at 9am | `0 9 * * 1-5` | Mon-Fri only |
| Every Monday at 6pm | `0 18 * * 1` | Weekly reports |
| First of month at midnight | `0 0 1 * *` | Monthly jobs |
| Every 6 hours | `0 */6 * * *` | 00:00, 06:00, 12:00, 18:00 |

## Production-Grade Templates

### Basic with Logging
```crontab
# Daily backup at 2am
0 2 * * * /home/user/scripts/backup.sh >> /var/log/backup.log 2>&1
```

### With Overlap Prevention (flock)
```crontab
# Sync every 5 min, but skip if previous run is still going
*/5 * * * * /usr/bin/flock -n /tmp/sync.lock /home/user/scripts/sync.sh >> /var/log/sync.log 2>&1
```

### With Error Alerting
```crontab
# Process data hourly, email on failure
0 * * * * /home/user/scripts/process.sh >> /var/log/process.log 2>&1 || echo "Process failed at $(date)" | mail -s "CRON ALERT" you@email.com
```

### With Timeout
```crontab
# Run report with 5-minute timeout
0 8 * * * timeout 300 /home/user/scripts/report.sh >> /var/log/report.log 2>&1
```

### With Environment Variables
```crontab
SHELL=/bin/bash
PATH=/usr/local/bin:/usr/bin:/bin:/home/user/.local/bin
NODE_ENV=production

# API sync every 15 minutes
*/15 * * * * cd /home/user/app && node sync.js >> /var/log/sync.log 2>&1
```

### With Health Check Ping
```crontab
# Backup with dead man's switch (pings healthcheck URL on success)
0 3 * * * /home/user/scripts/backup.sh >> /var/log/backup.log 2>&1 && curl -fsS --retry 3 https://hc-ping.com/your-uuid > /dev/null
```

## Common Automation Patterns

### Content Pipeline
```crontab
# Generate daily content at 7am
0 7 * * * cd /workspace && python generate_content.py >> logs/content.log 2>&1

# QA score content at 8am (after generation)
0 8 * * * cd /workspace && python qa_scorer.py >> logs/qa.log 2>&1

# Publish approved content at 9am
0 9 * * * cd /workspace && python publish.py >> logs/publish.log 2>&1
```

### Business Operations
```crontab
# Morning briefing at 8am weekdays
0 8 * * 1-5 cd /workspace && python daily_brief.py >> logs/brief.log 2>&1

# Invoice reminder every Monday
0 10 * * 1 cd /workspace && python invoice_reminder.py >> logs/invoices.log 2>&1

# Weekly report Sunday 6pm
0 18 * * 0 cd /workspace && python weekly_report.py >> logs/weekly.log 2>&1
```

### System Maintenance
```crontab
# Disk cleanup weekly
0 3 * * 0 /usr/bin/find /tmp -mtime +7 -delete >> /var/log/cleanup.log 2>&1

# Log rotation daily
0 0 * * * /usr/sbin/logrotate /etc/logrotate.conf

# Health check every 5 minutes
*/5 * * * * /home/user/scripts/healthcheck.sh >> /var/log/health.log 2>&1
```

## Example

### Input
> I want to run a Python script that checks my fleet status every 6 hours, but only if the previous check isn't still running. Log output to ~/logs/fleet.log. The script is at ~/scripts/fleet_check.py.

### Output

## Cron Configuration

### Schedule: Every 6 hours with overlap prevention
### Expression: `0 */6 * * *`

```crontab
# Fleet status check — every 6 hours, skip if previous still running
# Schedule: 00:00, 06:00, 12:00, 18:00 daily
# Added: 2026-03-26
SHELL=/bin/bash
PATH=/usr/local/bin:/usr/bin:/bin:/home/user/.local/bin

0 */6 * * * /usr/bin/flock -n /tmp/fleet_check.lock /usr/bin/python3 /root/scripts/fleet_check.py >> /root/logs/fleet.log 2>&1
```

### Breakdown
- Minute: `0` — At the top of the hour
- Hour: `*/6` — Every 6th hour (0, 6, 12, 18)
- Day of Month: `*` — Every day
- Month: `*` — Every month
- Day of Week: `*` — Every day of the week

### Installation
```bash
# Create log directory
mkdir -p ~/logs

# Edit crontab
crontab -e
# Paste the cron line above

# Verify
crontab -l
```

### Gotchas
- `flock -n` will silently skip the run if the lock file exists (previous run still going). Check logs if you suspect missed runs.
- Python path may differ — run `which python3` to confirm.
- Cron uses the system timezone. Run `timedatectl` to verify.

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
