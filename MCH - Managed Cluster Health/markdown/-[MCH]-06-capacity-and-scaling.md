# MCH-06: Capacity and Scaling

> **Series:** MCH — Managed Cluster Health | **Notebook:** 6 of 8 | **Created:** September 2026 | **Last Updated:** 09/25/2026

## Overview

> **Status:** Outline — this notebook's content is in development. The sections below list what it will cover.

Layer 3 of the health model — whether the cluster can keep up, including with a node gone. Read MCH-01 first for the cluster architecture and the five-layer health model this notebook builds on.

---

## Table of Contents

1. [Node Sizing](#sizing)
2. [Headroom for Failure](#headroom)
3. [Capacity Signals](#signals)
4. [Adding Nodes](#scale)
5. [Summary and Next Steps](#summary)

---

## Prerequisites

| Requirement | Details |
|-------------|---------|
| **Dynatrace deployment** | A self-hosted **Dynatrace Managed** cluster. Nothing in this series applies to Dynatrace SaaS. |
| **Access** | Cluster Management Console (CMC) administrator access; for the Cluster API, a cluster API token with the `ServiceProviderAPI` permission |
| **Query language** | None. Managed has no Grail, so this series has **no DQL cells** — every check is a CMC view, a cluster event, or a Cluster API call |
| **Version basis** | Written against the Managed documentation read 09/25/2026, when 1.342 – 1.346 were the generally supported releases |

<a id="sizing"></a>
## 1. Node Sizing

**Planned content:**

- The Micro–XLarge sizing table: vCPUs, RAM, host units, storage per store

<a id="headroom"></a>
## 2. Headroom for Failure

**Planned content:**

- The one-third-above-typical rule and what it means for 3, 5 and 7 nodes

<a id="signals"></a>
## 3. Capacity Signals

**Planned content:**

- *Adaptive Load Reduction activity*, the *Cluster health self-monitoring* dashboard, `dsfm:` metrics

<a id="scale"></a>
## 4. Adding Nodes

**Planned content:**

- Scale-out rules: same hardware, ≤10 ms inter-node latency, 30-node maximum

<a id="summary"></a>
## 5. Summary and Next Steps

Content in development. For the health model and the full series lineup, see MCH-01.

---

<sub>*This notebook was AI-generated from community-submitted and publicly available sources. This notebook series is not officially supported by Dynatrace. Always verify information against official [Dynatrace documentation](https://docs.dynatrace.com/managed).*</sub>
