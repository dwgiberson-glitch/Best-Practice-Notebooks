# AGENTS.md — MCH: Managed Cluster Health

Per-series routing for AI agents. Repo-wide rules: [../AGENTS.md](../AGENTS.md).
Humans: see [README.md](README.md).

8 reference notebooks on operating a self-hosted **Dynatrace Managed** cluster
day to day: node architecture, a five-layer health model (node, storage,
capacity, connectivity, lifecycle), where each health signal is surfaced, and
one notebook per layer. Managed has no Grail, so the series contains **no DQL**
and ships no importable notebook JSON — markdown and PDF only.

MCH-01 through MCH-03 are complete. MCH-04 through MCH-99 are currently outlines
that list their planned sections; for their topics, answer from MCH-01 and say the deep
dive is still in development.

## Routing table

Read only the file(s) matching the question. All paths are under `markdown/`.

| When the question is about… | Read |
|---|---|
| What runs on a Managed cluster node (NGINX, Server, Cassandra, Elasticsearch, embedded ActiveGate), where each data store lives, what a node failure costs (three copies vs. unreplicated, never-backed-up transaction storage), the five-layer health model, where health is surfaced (CMC, cluster event notifications, local / hosted / private self-monitoring and their licensing limits, Cluster API v1 `onpremise/cluster`, Mission Control), and which cluster events to route on day one | `-[MCH]-01-managed-cluster-architecture-health-model.md` |
| Whether every node and service is up: node inventory via CMC and Cluster API v1 (`operationState`, `configuration`, `configuration/status`, maintenance), `dynatrace.sh status` / `check` / `pid` and the seven systemd units, the gated service start order (firewall → Elasticsearch → Cassandra → Server → rest), the 3+ node cluster start/stop procedure vs. `dynatrace.sh` for smaller clusters, one-node-at-a-time rules for patches / updates / removals / IP changes, disabling a node's OneAgent traffic, which node and process events are emailed vs. Mission-Control-only, heap and NTP events, inter-node ports, a node triage order, and diagnostic archives | `-[MCH]-02-server-nodes-and-processes.md` |
| Health of the Cassandra metrics store (Long-term Metrics Store): replication factor 3, what else it holds (configuration, support archives), per-node size table and the 2 TB (not emailed) / 4 TB (configurable) events, why metric retention (5 years; 1-min to 14 d, 5-min to 28 d, 1-h to 400 d, 1-day after) can't be reduced, reading `cassandra-nodetool.sh status` (`UN` / `UJ`, `Load`, `Owns`), storage location and moving it, adding nodes and `cleanup`, 24 h redistribution on removal, manual vs PHA automatic repair, what the daily backup excludes (1-/5-min data, ~80% of column families) and its sizing, rack awareness, Cassandra 4.1.x by Managed release | `-[MCH]-03-cassandra-metrics-store.md` |
| Health of the Elasticsearch store: `_cluster/health`, disk space and adaptive data retention, snapshot health (outline) | `-[MCH]-04-elasticsearch-store.md` |
| Whether agents can reach the cluster and the cluster can reach Mission Control: agent traffic path, cluster ActiveGates, ports and hosts, the 14-day overage rule, offline licenses (outline) | `-[MCH]-05-activegates-mission-control-connectivity.md` |
| Whether the cluster can keep up: node sizing table, one-third failure headroom, adaptive load reduction, adding nodes (outline) | `-[MCH]-06-capacity-and-scaling.md` |
| Backups (and what they exclude), restore readiness, cluster upgrades and the version-skip rule, supported versions, Premium High Availability and data-center failover (outline) | `-[MCH]-07-backup-upgrade-disaster-recovery.md` |
| The whole series on one page: five-layer health-check checklist, review cadence, anti-patterns (outline) | `-[MCH]-99-best-practice-summary.md` |

## Related series

- Moving a Managed cluster to SaaS: `../M2S - Managed to SaaS Migration/`
- ActiveGate sizing concepts (SaaS-focused): `../FAQ - Frequently Asked Questions/`

## Rules

- Read-only; markdown only (see repo-root AGENTS.md for the full format table).
- Filenames contain literal brackets and a leading dash — quote paths in shell.
- This series applies to **Dynatrace Managed only**. Do not apply it to SaaS,
  and do not offer DQL for Managed cluster health — Managed has no Grail.
- There is no `notebooks/` JSON for this series; do not offer a tenant import.
  Cite by notebook ID (e.g. "MCH-01").
