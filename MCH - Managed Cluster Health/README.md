# MCH - Managed Cluster Health

Best practices for keeping a self-hosted Dynatrace Managed cluster healthy: its nodes, data stores, capacity, connectivity to Mission Control, backups and upgrades.

> **Note:** This series has no Dynatrace notebook JSON. Dynatrace Managed has no Grail, so there are no DQL queries to run — every check is a Cluster Management Console view, a cluster event, or a Cluster API call. Read it as Markdown or PDF.

## Structure
- pdfs/ — Printable versions of each notebook
- markdown/ — Markdown exports of the notebooks

## Notebook Lineup
1. [Managed Cluster Architecture and Health Model](markdown/-[MCH]-01-managed-cluster-architecture-health-model.md) — What runs on a cluster node, what a node failure costs, the five-layer health model, and where each health signal is surfaced
2. [Server Nodes and Processes](markdown/-[MCH]-02-server-nodes-and-processes.md) — Node inventory and operation state, on-node process checks, the gated service start order, safe restarts, which node events email you, memory, time, inter-node network, and triage
3. [Cassandra Metrics Store Health](markdown/-[MCH]-03-cassandra-metrics-store.md) — The metrics repository: replication, size ceilings and their events, 5-year retention by resolution, nodetool health checks, adding and removing nodes, repair, what the daily backup restores, rack awareness, and Cassandra versions
4. [Elasticsearch Store Health](markdown/-[MCH]-04-elasticsearch-store.md) — Outline: cluster health checks, disk space and adaptive retention, snapshots
5. [Cluster ActiveGates and Mission Control Connectivity](markdown/-[MCH]-05-activegates-mission-control-connectivity.md) — Outline: agent traffic path, the Mission Control link, and what breaks when it is down
6. [Capacity and Scaling](markdown/-[MCH]-06-capacity-and-scaling.md) — Outline: node sizing, failure headroom, load-reduction signals, adding nodes
7. [Backup, Upgrade, and Disaster Recovery](markdown/-[MCH]-07-backup-upgrade-disaster-recovery.md) — Outline: backup scope, restore readiness, upgrades, version support, Premium High Availability
99. [Best Practice Summary and Health-Check Checklist](markdown/-[MCH]-99-best-practice-summary.md) — Outline: five-layer checklist, review cadence, anti-patterns

## Usage
1. Choose a format: read markdown/ for browsing or pdfs/ for print.
2. Start with MCH-01 for the health model, then use the notebook for whichever layer is failing.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official Dynatrace documentation.*</sub>
