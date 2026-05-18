# Conflict-free Routing for Multi-Agent Path Finding

### 📖 Description
A benchmark suite for multi-agent path finding (MAPF) focusing on alternative approaches to routing
and scheduling in Answer Set Programming. It utilizes partial orders instead of fixed time steps to
avoid collisions (vertex, edge, and follow conflicts) while optimizing for flowtime or makespan.

### ⚙️ Technical Details
* **Type:** Optimization / Multi-shot (supports acyclicity and difference constraints)
* **Format:** ASP-Core-2, clingo (requires `clingo-dl` or hybrid solving for some encodings)
* **Tested With:** clingo >= 5.6.0

### 📊 Instances
* **Generation:** Automatic (via `conflict-free-routing` generator)
* **Details:**  
Includes benchmarks on various graph topologies (grids, warehouse-inspired layouts) with scaling agent counts, used to evaluate the effectiveness of partial-order based scheduling.

### 🔒 Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None (synthetic benchmarking data)

### 🔗 Source & Literature
* **Repository/ZIP:**  
[https://github.com/krr-up/conflict-free-routing-benchmarks](https://github.com/krr-up/conflict-free-routing-benchmarks)
* **Generator URL:**  
[https://github.com/krr-up/conflict-free-routing](https://github.com/krr-up/conflict-free-routing)
* **Reference:**  
Kaminski, R., Schaub, T., Son, T. C., Švancara, J., & Wanko, P. (2024). *Routing and Scheduling in Answer Set Programming applied to Multi-Agent Path Finding*. arXiv:2403.12153. [https://arxiv.org/abs/2403.12153](https://arxiv.org/abs/2403.12153)

### 👤 Contact
* **Name:** Roland Kaminski / Philipp Wanko (Potassco Team)
* **Email:** Roland.Kaminski@potassco.com, Philipp.Wanko@potassco.com

### 💡 Miscellaneous
* **Complexity:** NP-hard
* **Metadata:**  
Available in the `conflict-free-routing-paper` repository, including experimental setups and scripts.
* **Other Notes:**  
The encoding explores the trade-off between the granularity of time and the efficiency of the solving process by outsourcing temporal constraints to difference logic.
