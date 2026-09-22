# Conflict-free Routing for Multi-Agent Path Finding

## :material-file-document-outline: Description
This benchmark suite is designed for multi-agent path finding (MAPF) in Answer Set Programming.
It focuses on the two central tasks in MAPF: finding a route for every agent and scheduling
the agents movements so that they do not collide. The instances are intended to compare
different routing and scheduling strategies, including approaches that combine ASP with
difference logic.

The suite is closely related to [asprilo](../asprilo/index.md), but has a narrower scope.
It focuses on the asprilo M-domain and its Md-domain variant, both of which describe agents
moving through an environment.
The Md-domain provides a more direct way to represent MAPF instances. It is semantically
equivalent to the M-domain, but states each robots destination explicitly as a
`destination` object at the relevant coordinates.
Tasks such as moving shelves, assigning orders, and managing products are outside the scope of
this collection.

## :material-play-circle-outline: Usage
The collection contains instances in the asprilo Md-domain and
[MAPF Instance Format (MIF)](https://github.com/krr-up/mapf-instance-format).
Instances generated with the [asprilo](../asprilo/index.md) generator can be converted to the
Md-domain with the `misc/convert-md.sh` script:

```bash
convert/convert-md.sh --[m2md|md2m|am2md|amd2m] <instance>
```

The conversion mode selects the supported direction and input format. The resulting instance
can then be used with the encodings from the conflict-free-routing repository.

New MIF instances can be generated with the
[MAPF instance generator](https://github.com/krr-up/mapf-instance-generator).

Basic encodings for solving M-domain instances are provided. Md-instances can be used together with `misc/augment-md-to-m.lp`, which translates the explicit Md-domain destinations into
the corresponding M-domain representation.

For an M-domain instance, a general invocation has the following form:
```bash
clingo-dl encodings/preprocessing.lp <routing> encodings/schedule.lp <heuristic> <encodings/min_soc.lp> <m-instance> <config>
```

For an Md-domain instance, add `misc/augment-md-to-m.lp`:
```bash
clingo-dl misc/augment-md-to-m.lp encodings/preprocessing.lp <routing> encodings/schedule.lp <heuristic> <encodings/min_soc.lp> <md-instance> <config>
```

Example call:
```bash
clingo-dl misc/augment-md-to-m.lp encodings/preprocessing.lp encodings/gac_routing.lp encodings/schedule.lp encodings/min_soc.lp instances/md/gridworld/x3_y3_r1_n6/x3_y3_n6_r1_s1_ps1_pr1_u1_o1_l1_N001.lp -t2 --propagate=partial --stats
```
The [repository](https://github.com/krr-up/conflict-free-routing) contains additional routing and scheduling encodings, heuristics, and
experimental scripts for alternative solving strategies.

## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Optimization / Multi-shot (supports acyclicity and difference constraints)
* **Format:** ASP-Core-2, clingo (requires `clingo-dl` or hybrid solving for some encodings)
* **Tested With:** clingo >= 5.6.0

### :material-chart-bar: Instances
* **Generation:** Automatic, using the conflict-free-routing or MAPF instance generators
* **Details:**  
Includes benchmarks on various graph topologies (grids and warehouse-inspired layouts) with varying numbers of agents, used to evaluate the effectiveness of partial-order-based scheduling.

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None (synthetic benchmarking data)

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
[https://github.com/krr-up/conflict-free-routing](https://github.com/krr-up/conflict-free-routing)  
[https://github.com/krr-up/conflict-free-routing-benchmarks](https://github.com/krr-up/conflict-free-routing-benchmarks)
* **Generator:**  
[https://github.com/potassco/asprilo](https://github.com/potassco/asprilo)  
[https://github.com/krr-up/mapf-instance-generator](https://github.com/krr-up/mapf-instance-generator)  
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
The encodings explore the trade-off between the granularity of time and solving efficiency.
Some temporal constraints are delegated to difference logic, allowing the ASP encoding to
represent ordering and scheduling decisions without explicitly enumerating every time step.

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
