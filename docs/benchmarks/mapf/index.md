# Conflict-free Routing for Multi-Agent Path Finding

## :material-file-document-outline: Description
A benchmark suite for multi-agent path finding (MAPF) focusing on alternative approaches to routing
and scheduling in Answer Set Programming. It utilizes partial orders instead of fixed time steps to
avoid collisions (vertex, edge, and follow conflicts) while optimizing for flowtime or makespan.

This benchmark suit consist of a collection of different Md-Domain instances.
More instances can be created using the [asprilo](../asprilo/index.md) generator and
subsequently converted to the Md-Domain using the `convert-md.sh` script.

```bash
convert-md.sh --[m2md|md2m|am2md|amd2m] <instance>
```

Basic clingo-dl encodings are provided. More encodings and scripts can be found here.

Usage:
```bash
clingo-dl encodings/preprocessing.lp <routing> encodings/schedule.lp <heuristic> <encodings/min_soc.lp> <instance> <config>
```

Example call:
```bash
clingo-dl encodings/preprocessing.lp encodings/gac_routing.lp encodings/schedule.lp encodings/min_soc.lp x11_y6_n66_r2_s16_ps1_pr16_u16_o2_N001.lp -t2 --propagate=partial --stats
```

## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Optimization / Multi-shot (supports acyclicity and difference constraints)
* **Format:** ASP-Core-2, clingo (requires `clingo-dl` or hybrid solving for some encodings)
* **Tested With:** clingo >= 5.6.0

### :material-chart-bar: Instances
* **Generation:** Automatic (via `conflict-free-routing` generator)
* **Details:**  
Includes benchmarks on various graph topologies (grids, warehouse-inspired layouts) with scaling agent counts, used to evaluate the effectiveness of partial-order based scheduling.

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None (synthetic benchmarking data)

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
[https://github.com/krr-up/conflict-free-routing-benchmarks](https://github.com/krr-up/conflict-free-routing-benchmarks)
* **Generator URL:**  
[https://github.com/krr-up/conflict-free-routing](https://github.com/krr-up/conflict-free-routing)
* **Reference:**  
Kaminski, R., Schaub, T., Son, T. C., Švancara, J., & Wanko, P. (2024). *Routing and Scheduling in Answer Set Programming applied to Multi-Agent Path Finding*. arXiv:2403.12153. [https://arxiv.org/abs/2403.12153](https://arxiv.org/abs/2403.12153)

### :material-card-account-mail-outline: Contact
* **Name:** Roland Kaminski / Philipp Wanko (Potassco Team)
* **Email:** Roland.Kaminski@potassco.com, Philipp.Wanko@potassco.com

### :material-lightbulb-outline: Miscellaneous
* **Complexity:** NP-hard
* **Metadata:**  
Available in the `conflict-free-routing-paper` repository, including experimental setups and scripts.
* **Other Notes:**  
The encoding explores the trade-off between the granularity of time and the efficiency of the solving process by outsourcing temporal constraints to difference logic.

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
