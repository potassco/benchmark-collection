# BioASP: Life Sciences Reasoning Benchmarks  

> CASPO, MENECO, EXDESI, PRECURSOR, IGGY

### 📖 Description
A collection of ASP benchmarks from systems biology and bioinformatics, covering reasoning on biological networks,
optimization of metabolic models, and experiment design. The encodings solve real-world biological reasoning and
optimization tasks using Answer Set Programming.

### ⚙️ Technical Details
* **Type:** Decision, Optimization (some multi-shot usage via scripting)
* **Format:** ASP-Core-2 / clingo
* **Tested With:** clingo (various 5.x versions over time)

### 📊 Instances
* **Generation:** Real-world biological data
* **Details:**  
    Each benchmark contains original datasets (biological networks, reactions, experiments) transformed
    into ASP facts. Instance sizes vary from small curated examples to medium-to-large real-world networks.

### 🔒 Data & Access (Confidentiality)
* **Status:** Public
* **License:** Repository-specific open-source licenses (see individual repositories)
* **Sensitivity:** No personal or sensitive data; biological network data only

### 🔗 Source & Literature
* **Repositories/ZIPs:**
    * Reasoning on signaling networks (CASPO): <https://github.com/bioasp/caspo>
    * Metabolic network completion (MENECO): <https://github.com/bioasp/meneco>
    * Experiment design (EXDESI): <https://github.com/bioasp/exdesi>
    * Minimal metabolic precursor sets (PRECURSOR): <https://github.com/bioasp/precursor>
    * Influence graph analysis (IGGY): <https://github.com/bioasp/iggy>
* **Generator URL:**  
    Data preparation and instance generation scripts are included in the respective repositories.
* **Reference:**  
    See publications cited in the individual repositories (systems biology / BioASP literature).

### 👤 Contact
* **Name:** BioASP contributors
* **Email:** See GitHub repository contacts / maintainers

### 💡 Miscellaneous
* **Complexity:**  
    Domain-specific reasoning and optimization problems; includes NP-hard optimization tasks.
* **Metadata:**  
    No unified metadata format across repositories; instance properties are partially documented in README files.
* **Other Notes:**  
    All benchmarks follow a similar workflow:
    1. Transform biological data into ASP facts
    2. Combine with problem-specific ASP encodings
    3. Solve using one or multiple calls to clingo
    4. Post-process solver output into domain-specific results
