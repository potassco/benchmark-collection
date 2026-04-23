# **asprilo** (Robotic Intra-Logistics Benchmark Suite)

### 📖 Description
A benchmarking framework to study typical scenarios in intra-logistics and warehouse automation.
It models complex multi-agent pathfinding and task assignment problems where mobile robots move
shelves to picking stations.

### ⚙️ Technical Details
* **Type:** Optimization, Multi-shot, Planning
* **Format:** ASP-Core-2, clingo (utilizes incremental solving and Python scripting)
* **Tested With:** clingo >= 5.4.0

### 📊 Instances
* **Generation:** Automatic (via the integrated `asprilo-generator`)
* **Details:**  
Includes structured and random sets (e.g., domains A, B, C, and M). Scale ranges from small 9x6 grids
with 2 robots to large-scale warehouse layouts with dozens of robots and hundreds of shelf locations.

### 🔒 Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None (Synthetic/Generated data)

### 🔗 Source & Literature
* **Repository/ZIP:**  
[https://github.com/potassco/asprilo-encodings](https://github.com/potassco/asprilo-encodings) (Encodings)
* **Generator URL:**  
[https://github.com/potassco/asprilo](https://github.com/potassco/asprilo) (Tooling & Generator)
* **Reference:**  
Gebser, M., Obermeier, P., Otto, T., Schaub, T., Sabuncu, O., Nguyen, V., & Son, T. C. (2018). *Experimenting with robotic intra-logistics domains*. Theory and Practice of Logic Programming, 18(3-4), 502–519. [DOI: 10.1017/S147106841800014X]

### 👤 Contact
* **Name:** Philipp Obermeier / Potassco Team
* **Email:** Philipp.Obermeier@potassco.com

### 💡 Miscellaneous
* **Complexity:** NP-Hard
* **Metadata:**  
Comprehensive documentation, a solution checker, and a visualizer are available at [https://asprilo.github.io/](https://asprilo.github.io/).
* **Other Notes:**  
The benchmark is designed to be highly modular, supporting various sub-problems like movement-only (M), shelf-to-station assignment (A), and full warehouse scenarios.
