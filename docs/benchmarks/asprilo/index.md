# **asprilo** (Robotic Intra-Logistics Benchmark Suite)

## :material-file-document-outline: Description
A benchmark framework to study typical scenarios in intra-logistics and warehouse automation.
It models complex multi-agent pathfinding (MAPF) and task assignment problems where mobile
robots move shelves to picking stations.  
The `Scripts` directory contains scripts to generate structured and random benchmark sets from
the A,B,C and M domain using the asprilo generator (see below).

## :material-play-circle-outline: Usage
All asprilo tools can be installed from the asprilo [repository](https://github.com/potassco/asprilo).  
The tools are also available via the potassco conda channel, but these are most likely outdated.
To install the tools simply use or create a conda environment with python=>3.9.
```bash
conda create -n <env> python=3.13
conda activate <env>
git clone https://github.com/potassco/asprilo.git
```
Install the generator:
```bash
cd asprilo/generator
pip install .
gen -h
```
Install the visualizer:
```bash
cd asprilo/visualizer
pip install .
viz -h
```
A detailed description on how to use these tools can be found [here](https://asprilo.github.io)

### :material-flask-outline: Examples
Structured (real-world-like) instance:

- 9x6 floor grid (`-x 9 -y 6`)
- 3x2 shelf cluster dimensions (`-X 3 -Y 2`)
- 6 shelves (`-s 6`)
- 1 picking station (`-p 1`)
- 2 robots (`-r 2`)
- highway layout (`-H`)
- 4 products (`-P 4`)
- 20 product units (`-u 20`)
- 4 orders (`-o 4`)
- guarantee that all products are ordered at least once (`--oap`)

```bash
gen -x 9 -y 6 -X 3 -Y 2 -s 6 -p 1 -r 2 -H -P 4 -u 20 -o 4 --oap
```

Random instance:

- 10x10 floor grid (`-x 10 -y 10`)
- 50 shelves (`-s 50`)
- 10 picking station (`-p 10`)
- 30 robots (`-r 30`)
- 10 products (`-P 10`)
- 100 product units (`-u 100`)
- 8 orders (`-o 8`)
- 2 products per shelf (`--prs 2`)
- 4 clingo threads (`-t 4`)
- verbose output (`-V`)
- incremental generation (`-I`)

```bash
gen -x 10 -y 10 -s 50 -p 10 -r 30 -P 10 -u 100 -o 8 --prs 2 -t 4 -V -I
```

Batch generation:
```bash
gen --batch ./Scripts/batch/abc/structured.yml -I -t 4 -V
```

Generated instances can be found in the `generatedInstances` directory.

### :material-code-json: Encodings
The encodings are in three directories with regard to their problem domains:

- `./abc` contains encodings for asprilo domains A, B and C
- `./m` contains encodings for asprilo domain M
- `./control` contains encodings for supplementary features such as task assignment, highway constrains, etc. for all (some) asprilo domains

A detailed description of the encodings and their naming conventions can be found [here](https://github.com/potassco/asprilo-encodings)

It is recommended to use encodings with the `encoding*` prefix, which provide a shorthand to call
all necessary encodings. A time horizon should also be set, e.g.:
```
clingo ./Encodings/m/encoding.lp <instance.lp> -c horizon=8
```

## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Optimization, Multi-shot, Planning
* **Format:** ASP-Core-2, clingo (utilizes incremental solving and Python scripting)
* **Tested With:** clingo >= 5.4.0

### :material-chart-bar: Instances
* **Generation:** Automatic (via the integrated `asprilo-generator`)
* **Details:**  
Includes structured and random sets (e.g., domains A, B, C, and M). Scale ranges from small 9x6 grids
with 2 robots to large-scale warehouse layouts with dozens of robots and hundreds of shelf locations.

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None (Synthetic/Generated data)

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
[https://github.com/potassco/asprilo-encodings](https://github.com/potassco/asprilo-encodings) (Encodings)
* **Generator URL:**  
[https://github.com/potassco/asprilo](https://github.com/potassco/asprilo) (Tooling & Generator)
* **Reference:**  
Gebser, M., Obermeier, P., Otto, T., Schaub, T., Sabuncu, O., Nguyen, V., & Son, T. C. (2018). *Experimenting with robotic intra-logistics domains*. Theory and Practice of Logic Programming, 18(3-4), 502–519. DOI: 10.1017/S147106841800014X

### :material-card-account-mail-outline: Contact
* **Name:** Philipp Obermeier / Potassco Team
* **Email:** Philipp.Obermeier@potassco.com

### :material-lightbulb-outline: Miscellaneous
* **Complexity:** NP-Hard
* **Metadata:**  
Comprehensive documentation, a solution checker, and a visualizer are available at [https://asprilo.github.io/](https://asprilo.github.io/).
* **Other Notes:**  
The benchmark is designed to be highly modular, supporting various sub-problems like movement-only (M), shelf-to-station assignment (A), and full warehouse scenarios.

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
