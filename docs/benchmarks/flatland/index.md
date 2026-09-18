# Flatland Environments

## :material-file-document-outline: Description
A collection of [Flatland](https://flatland-association.github.io/flatland-book/intro.html)
instances for comparing ASP encodings. The environments are derived from the actual
competition, but they do not currently account for malfunctions or speed.

## :material-play-circle-outline: Usage
This benchmark set contains 15 difficulty classes (Test_00 to Test_14), each with 10 levels,
as well as a script for splitting these levels into multiple environment instances.

```
python split.py <dir> <instance|all>
```

Where `dir` is the directory containing the base environment instances and `instance` the
instance file to split, or "all" to split all instances in the directory.

Example call:
```
python split.py Test_00 Level_1
```

> **__NOTE:__** clingo Python API needs to be installed for the generator to work.

The encodings are not included, but they can be found [here](https://github.com/potassco/flaspland-encodings),
together with instructions on how to use them. The repository also includes a
[guide](https://github.com/potassco/flaspland-encodings/tree/main/benchmarking) for
using flatland with the benchmark tool.

New instances can be generated as described in the *Creating environments* section
[here](https://github.com/krr-up/flatland).
This requires installing flatland-rl.

## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Uncertain
* **Format:** clingo
* **Tested With:** clingo 5.8.0

### :material-chart-bar: Instances
* **Generation:** Automatic
* **Details:** 150 (18,000 instances)
  * Instances come from the final round of the competition
  * 15 difficulty classes
  * Each class has 10 levels (base environments)
  * Each level contains 7 trains
  * Each level can be split split into 120 instances based on a selection of trains
    * 21 two-train environments
    * 35 three-train environments
    * 35 four-train environments
    * 21 five-train environments
    * 7 six-train environments
    * 1 seven-train environment (original)

### :material-lock-outline: Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** None

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:** [flatland-rl](https://github.com/flatland-association/flatland-rl)
* **Generator URL:** [gen_envs.py](https://github.com/krr-up/flatland/blob/main/benchmarks/gen_envs.py)
* **Reference:** [Flatland-RL : Multi-Agent Reinforcement Learning on Trains](https://arxiv.org/abs/2012.05893)

### :material-card-account-mail-outline: Contact
* **Name:** Ryan Kepler Murphy
* **Email:** ryan.murphy@uni-potsdam.de

### :material-lightbulb-outline: Miscellaneous
* **Complexity:** Unknown
* **Metadata:** [Environment Configurations](https://flatland-association.github.io/flatland-book/challenges/flatland3/envconfig.html)

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
