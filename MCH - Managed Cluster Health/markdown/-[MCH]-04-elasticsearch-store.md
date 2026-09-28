# MCH-04: Elasticsearch Store Health

> **Series:** MCH — Managed Cluster Health | **Notebook:** 4 of 8 | **Created:** September 2026 | **Last Updated:** 09/25/2026

## Overview

> **Status:** Outline — this notebook's content is in development. The sections below list what it will cover.

Layer 2 of the health model — the Elasticsearch store. Read MCH-01 first for the cluster architecture and the five-layer health model this notebook builds on.

---

## Table of Contents

1. [What the Elasticsearch Store Holds](#role)
2. [Health Checks](#checks)
3. [Disk Space and Adaptive Retention](#disk)
4. [Snapshot Health](#backup)
5. [Summary and Next Steps](#summary)

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Dynatrace deployment** | A self-hosted **Dynatrace Managed** cluster. Nothing in this series applies to Dynatrace SaaS. |
| **Access** | Cluster Management Console (CMC) administrator access; for the Cluster API, a cluster API token with the `ServiceProviderAPI` permission |
| **Query language** | None. Managed has no Grail, so this series has **no DQL cells** — every check is a CMC view, a cluster event, or a Cluster API call |
| **Version basis** | Written against the Managed documentation read 09/25/2026, when 1.342 – 1.346 were the generally supported releases |

<a id="role"></a>
## 1. What the Elasticsearch Store Holds

**Planned content:**

- Replicated data, including Log Monitoring events (two copies)

<a id="checks"></a>
## 2. Health Checks

**Planned content:**

- `_cluster/health` — *green*, or *yellow* on a single-node setup

<a id="disk"></a>
## 3. Disk Space and Adaptive Retention

**Planned content:**

- Insufficient disk space and adaptive data retention behavior

<a id="backup"></a>
## 4. Snapshot Health

**Planned content:**

- Incremental snapshots every 2 hours; the *ElasticSearch backup problem* event

<a id="summary"></a>
## 5. Summary and Next Steps

Content in development. For the health model and the full series lineup, see MCH-01.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official [Dynatrace documentation](https://docs.dynatrace.com/managed).*</sub>
