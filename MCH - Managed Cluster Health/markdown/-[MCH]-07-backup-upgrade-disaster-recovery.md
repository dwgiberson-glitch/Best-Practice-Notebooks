# MCH-07: Backup, Upgrade, and Disaster Recovery

> **Series:** MCH — Managed Cluster Health | **Notebook:** 7 of 8 | **Created:** September 2026 | **Last Updated:** 09/25/2026

## Overview

> **Status:** Outline — this notebook's content is in development. The sections below list what it will cover.

Layer 5 of the health model — backups, version currency, and surviving a site loss. Read MCH-01 first for the cluster architecture and the five-layer health model this notebook builds on.

---

## Table of Contents

1. [Backup Scope and Schedule](#backup)
2. [Restore Readiness](#restore)
3. [Upgrades](#upgrade)
4. [Version Support](#support)
5. [Premium High Availability and Failover](#pha)
6. [Summary and Next Steps](#summary)

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Dynatrace deployment** | A self-hosted **Dynatrace Managed** cluster. Nothing in this series applies to Dynatrace SaaS. |
| **Access** | Cluster Management Console (CMC) administrator access; for the Cluster API, a cluster API token with the `ServiceProviderAPI` permission |
| **Query language** | None. Managed has no Grail, so this series has **no DQL cells** — every check is a CMC view, a cluster event, or a Cluster API call |
| **Version basis** | Written against the Managed documentation read 09/25/2026, when 1.342 – 1.346 were the generally supported releases |

<a id="backup"></a>
## 1. Backup Scope and Schedule

**Planned content:**

- What is and isn't backed up — transaction storage is not
- Daily Cassandra snapshot, incremental Elasticsearch snapshots

<a id="restore"></a>
## 2. Restore Readiness

**Planned content:**

- Testing a restore before you need one

<a id="upgrade"></a>
## 3. Upgrades

**Planned content:**

- Automatic downloads, the 24-hour wait, one node at a time, the divisible-by-4 skip rule, <3-node downtime

<a id="support"></a>
## 4. Version Support

**Planned content:**

- Reading the Managed release table and the four-week cadence

<a id="pha"></a>
## 5. Premium High Availability and Failover

**Planned content:**

- Two data centers, six-node minimum, automatic DC failover

<a id="summary"></a>
## 6. Summary and Next Steps

Content in development. For the health model and the full series lineup, see MCH-01.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official [Dynatrace documentation](https://docs.dynatrace.com/managed).*</sub>
