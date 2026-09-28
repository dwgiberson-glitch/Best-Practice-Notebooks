# MCH-99: Best Practice Summary and Health-Check Checklist

> **Series:** MCH — Managed Cluster Health | **Notebook:** 8 of 8 | **Created:** September 2026 | **Last Updated:** 09/25/2026

## Overview

> **Status:** Outline — this notebook's content is in development. The sections below list what it will cover.

The series in one page — the five-layer checklist, the day-one events, and the recurring health review. Read MCH-01 first for the cluster architecture and the five-layer health model this notebook builds on.

---

## Table of Contents

1. [Five-Layer Health-Check Checklist](#checklist)
2. [Daily, Weekly and Monthly Reviews](#cadence)
3. [Anti-Patterns](#anti-patterns)
4. [Summary and Next Steps](#summary)

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Dynatrace deployment** | A self-hosted **Dynatrace Managed** cluster. Nothing in this series applies to Dynatrace SaaS. |
| **Access** | Cluster Management Console (CMC) administrator access; for the Cluster API, a cluster API token with the `ServiceProviderAPI` permission |
| **Query language** | None. Managed has no Grail, so this series has **no DQL cells** — every check is a CMC view, a cluster event, or a Cluster API call |
| **Version basis** | Written against the Managed documentation read 09/25/2026, when 1.342 – 1.346 were the generally supported releases |

<a id="checklist"></a>
## 1. Five-Layer Health-Check Checklist

**Planned content:**

- One checklist item per signal, grouped by layer

<a id="cadence"></a>
## 2. Daily, Weekly and Monthly Reviews

**Planned content:**

- What to look at, and how often

<a id="anti-patterns"></a>
## 3. Anti-Patterns

**Planned content:**

- Unread notification mailboxes, uneven node disks, NFS for live data, running at capacity

<a id="summary"></a>
## 4. Summary and Next Steps

Content in development. For the health model and the full series lineup, see MCH-01.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official [Dynatrace documentation](https://docs.dynatrace.com/managed).*</sub>
