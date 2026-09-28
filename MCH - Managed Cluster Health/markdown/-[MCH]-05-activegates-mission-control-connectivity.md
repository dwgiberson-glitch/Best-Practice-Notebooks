# MCH-05: Cluster ActiveGates and Mission Control Connectivity

> **Series:** MCH — Managed Cluster Health | **Notebook:** 5 of 8 | **Created:** September 2026 | **Last Updated:** 09/25/2026

## Overview

> **Status:** Outline — this notebook's content is in development. The sections below list what it will cover.

Layer 4 of the health model — whether agents can reach the cluster and the cluster can reach Mission Control. Read MCH-01 first for the cluster architecture and the five-layer health model this notebook builds on.

---

## Table of Contents

1. [The Agent Traffic Path](#agent-path)
2. [The Mission Control Link](#mc-link)
3. [What Breaks When Mission Control Is Unreachable](#mc-outage)
4. [Connectivity Events](#events)
5. [Summary and Next Steps](#summary)

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Dynatrace deployment** | A self-hosted **Dynatrace Managed** cluster. Nothing in this series applies to Dynatrace SaaS. |
| **Access** | Cluster Management Console (CMC) administrator access; for the Cluster API, a cluster API token with the `ServiceProviderAPI` permission |
| **Query language** | None. Managed has no Grail, so this series has **no DQL cells** — every check is a CMC view, a cluster event, or a Cluster API call |
| **Version basis** | Written against the Managed documentation read 09/25/2026, when 1.342 – 1.346 were the generally supported releases |

<a id="agent-path"></a>
## 1. The Agent Traffic Path

**Planned content:**

- NGINX redirection, embedded vs. separate cluster ActiveGates, load balancers

<a id="mc-link"></a>
## 2. The Mission Control Link

**Planned content:**

- Ports and hosts (HTTPS/WSS on 443), *Check Mission Control connection*

<a id="mc-outage"></a>
## 3. What Breaks When Mission Control Is Unreachable

**Planned content:**

- The 14-day overage rule, updates, DPS usage reporting, offline licenses

<a id="events"></a>
## 4. Connectivity Events

**Planned content:**

- *Lack of connection to Dynatrace Mission Control*, *node can't receive OneAgent traffic*

<a id="summary"></a>
## 5. Summary and Next Steps

Content in development. For the health model and the full series lineup, see MCH-01.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official [Dynatrace documentation](https://docs.dynatrace.com/managed).*</sub>
