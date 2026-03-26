# Agent Fleet Status

> Check the health of multiple machines via SSH. Get a unified dashboard for distributed systems.

## Description

Agent Fleet Status monitors the health of a fleet of machines — servers, Mac Minis, cloud instances, Raspberry Pis, or any SSH-accessible host. It checks uptime, disk, memory, CPU, running processes, cron jobs, and service health, then outputs a unified dashboard. Built for operators running distributed agent swarms, home labs, or multi-server deployments.

## Activation

This skill activates when:
- The user asks about the status of their servers or machines
- The user wants to check if a service is running on a remote host
- The user mentions fleet health, server status, or system monitoring
- The user asks "are my agents running?" or "what's the status of my machines?"

**Trigger phrases**: "fleet status", "check my servers", "machine health", "are my agents running", "server dashboard", "system status", "check uptime", "what's running on"

## Health Check Dimensions

### 1. Connectivity
- Can we reach the host via SSH?
- Latency (ms)
- Last successful connection

### 2. System Resources
| Check | Warning | Critical |
|-------|---------|----------|
| Disk usage | >80% | >95% |
| Memory usage | >85% | >95% |
| CPU load (5min avg) | >70% | >90% |
| Uptime | <1 day (recent reboot) | N/A |
| Swap usage | >50% | >80% |

### 3. Process Health
- Are expected processes running? (by name or PID file)
- Zombie processes count
- Top 5 processes by CPU/memory

### 4. Service Health
- HTTP endpoints responding? (status code + latency)
- Port checks (is the port open and accepting connections?)
- Cron job status (last run time, exit codes from logs)

### 5. Agent-Specific
- OpenClaw gateway status
- Ollama model loaded
- Custom agent processes
- Log file freshness (is the agent producing output?)

## Instructions

When asked to check fleet status, generate commands and/or output in this format:

```
# Fleet Status Dashboard
## Checked at: [timestamp]

---

### [HOSTNAME] — [IP] — [STATUS EMOJI removed: OK / WARN / CRITICAL / OFFLINE]

| Check | Value | Status |
|-------|-------|--------|
| SSH | Connected (XXms) | OK |
| Uptime | XX days | OK |
| Disk | XX% of XXG used | [OK/WARN/CRIT] |
| Memory | XX% of XXG used | [OK/WARN/CRIT] |
| CPU Load | X.XX (5m avg) | [OK/WARN/CRIT] |
| Swap | XX% used | [OK/WARN/CRIT] |

**Running Services**:
- [service]: PID XXXX, up Xh, CPU X%, MEM X%
- [service]: PID XXXX, up Xh, CPU X%, MEM X%

**Cron Jobs**: XX active, last run [time], [X failures in 24h]

**Alerts**:
- [Any warnings or critical issues]

---

### Fleet Summary

| Host | Status | Disk | Mem | CPU | Services | Alerts |
|------|--------|------|-----|-----|----------|--------|
| [host1] | OK | 45% | 62% | 0.8 | 5/5 | 0 |
| [host2] | WARN | 82% | 71% | 1.2 | 4/5 | 1 |
| [host3] | OFFLINE | — | — | — | — | SSH FAIL |
```

## SSH Commands Used

The skill generates and executes these commands per host:

```bash
# Connectivity
ssh -o ConnectTimeout=5 -o BatchMode=yes user@host "echo ok"

# System resources
ssh user@host "
  uptime;
  df -h / | tail -1;
  free -m | grep Mem;
  cat /proc/loadavg;
  swapon --show --bytes 2>/dev/null
"

# Process health
ssh user@host "
  ps aux --sort=-%mem | head -6;
  ps aux | grep -c Z  # zombie count
"

# Service checks
ssh user@host "
  pgrep -la ollama;
  pgrep -la openclaw;
  pgrep -la node;
  systemctl is-active [service] 2>/dev/null
"

# Cron status
ssh user@host "crontab -l 2>/dev/null | grep -v '^#' | wc -l"

# Log freshness
ssh user@host "find /var/log -name '*.log' -mmin -60 | head -5"
```

For macOS hosts, adjust commands:
```bash
# macOS disk
ssh user@host "df -h / | tail -1"

# macOS memory (no free command)
ssh user@host "vm_stat | head -5; sysctl hw.memsize"

# macOS processes
ssh user@host "ps aux -r | head -6"
```

## Fleet Configuration

Define your fleet as a simple list:

```yaml
fleet:
  - name: Omni
    host: localhost
    type: linux
    expected_services: [ollama, node]

  - name: BMO
    host: 192.168.1.98
    user: operator
    type: macos
    expected_services: [openclaw, ollama, node, n8n]

  - name: OCI
    host: 192.168.1.92
    user: macmini
    type: macos
    expected_services: [openclaw]

  - name: SailorsBot1
    host: 192.168.1.99
    user: operator
    type: macos
    expected_services: [repflow]
```

## Alerting Logic

Severity escalation:

1. **INFO**: All systems green. No action needed.
2. **WARN**: One or more hosts have warnings (disk >80%, high memory, service restart detected). Review within 24 hours.
3. **CRITICAL**: A host has critical resource usage or a key service is down. Act within 1 hour.
4. **OFFLINE**: A host is unreachable via SSH. Investigate immediately — could be network, crash, or power.

## Example

### Input
> Check status of BMO (192.168.1.98, operator, macOS) and OCI (192.168.1.92, macmini, macOS).

### Output
*(Generates SSH commands, executes them, and produces the dashboard table showing both machines' disk, memory, CPU, running services, cron job count, and any alerts.)*

---

*Built by [KOINO Capital](https://koino.capital) — Agentic growth systems that run while you sleep.*
*Want this running autonomously 24/7? [Deploy with KOINO](https://koino.capital/deploy)*
