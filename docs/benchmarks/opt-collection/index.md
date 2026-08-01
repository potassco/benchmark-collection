# Collection of Optimization Problems

## :material-file-document-outline: Description
Contains encodings and instances of varying sizes and difficulty for the following problems:

- Social Golfer Problem (SGP)
- Shift Design (SD)
- Sudoku Puzzle Generation (SPG)
- Traveling Salesman Problem (TSP)
- Weighted Strategic Companies (WSC)

Each problem is contained in its own directory which includes the encoding with the name
of the problem, e.g. `golfer.lp` for SGP, and an instance directory.

## :material-play-circle-outline: Usage

Example call:
```bash
clingo <encoding.lp> <instance.lp>
```


## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Optimization, Multi-shot
* **Format:** clingo
* **Tested With:** clingo 5.8.0

### :material-chart-bar: Instances
* **Details:**  
Hand-picked instances of varying sizes and difficulty

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
    * raw/including ALASPO:  
    www.kr.tuwien.ac.at/research/projects/bai/kr22.zip
    * clean on the institute cluster:  
    /mnt/beegfs/home/toschmidt/benchmarks 
* **Reference:**  
Eiter, T., Geibinger, T., Ruiz, N.H., et al.: ALASPO: An Adaptive Large-Neighbourhood ASP Optimiser. Proceedings of the Nineteenth International Conference on Principles of Knowledge Representation and Reasoning. 565-569 (2022). doi:10.24963/kr.2022/58

### :material-card-account-mail-outline: Contact
* **Name:** Tom Schmidt
* **Email:** tom.schmidt@uni-potsdam.de

### :material-lightbulb-outline: Miscellaneous
* **Complexity:**  NP-hard (Sudoku: NP-complete)

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
