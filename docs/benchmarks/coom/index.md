# COOM Configuration

## :material-file-document-outline: Description
A collection of scalable product configuration problems specified in the
[COOM](https://www.coom-lang.org) language created to be solved with the
[COOM Suite](https://github.com/potassco/coom-suite).  
This collection includes benchmark instances, scripts to generate more instances, and
everything required to run the benchmarks using the
[potassco-benchmark-tool](https://potassco.org/benchmark-tool).


## :material-play-circle-outline: Usage
The COOM Suite can be installed using pip. It is recommended to create a clean python
environment beforehand, e.g., using conda.

```bash
conda create -n <enc-name> python=3.14
conda activate <env-name>
pip install coomsuite
```

Instances can then be solved using:

```bash
coomsuite solve <instance>
```

For more information on how to use the COOM Suite check the [documentation](https://docs.potassco.org/coom-suite).

All instances and encodings were tested using clingo >=5.8.0

Scripts to generate new instances can be found in the directory of the specific domain, e.g.,
`benchmarks/restaurant/create_instance.sh`

---

The benchmark-tool can also be installed using pip:

```bash
pip install potassco-benchmark-tool
```

To run the benchmarks, the following steps have to be performed.  
Replace `laptop` with `cluster` if you want to run the benchmarks on the cluster
instead of locally.

1. Generate the benchmark folder structure and scripts

    ```bash
    btool gen runscripts/runscript-all-laptop.xml
    ```

2. Run the benchmarks

    ```bash
    ./output/coom-benchmark-project/laptop/start.py
    ```

3. Verify results

    ```bash
    btool verify output/coom-benchmark-project/laptop/results
    ```

4. Evaluate and convert the results

    ```bash
    btool eval runscripts/runscript-all-laptop.xml | btool conv -o result-all.xlxs
    ```

Additional scripts, e.g., for creating plots, can be found in the
[COOM Suite Benchmarks](https://github.com/potassco) repository.


## :material-information-outline: Metadata
### :material-cog-outline: Technical Details
* **Type:** Configuration, Multi-shot (wip)
* **Format:** [COOM](https://www.coom-lang.org/) (translations to ASP through [COOM Suite](https://github.com/potassco/coom-suite))
* **Tested With:** clingo>=5.8

### :material-chart-bar: Instances
* **Generation:** Each domain has its own script, one real-world anonymized domain (space-collider)
* **Details:**  
Multiple domains with about 3-50 instances each (work in progress)

### :material-lock-outline: Data & Access Data & Access (Confidentiality)
* **Status:** Public
* **License:** MIT
* **Sensitivity:** Mostly artificial instances, real-world problems are already anonymized

### :material-book-open-variant: Source & Literature
* **Repository/ZIP:**  
https://github.com/potassco/coom-benchmarks
* **Reference:**  
https://arxiv.org/abs/2504.00013

### :material-card-account-mail-outline: Contact
* **Name:** Nicolas Rühling
* **Email:** nruehling@uni-potsdam.de

### :material-lightbulb-outline: Miscellaneous
* **Other Notes:**  
The corresponding clingo encoding can be found in the [COOM Suite](https://github.com/potassco/coom-suite): https://github.com/potassco/coom-suite/blob/master/src/coomsuite/encodings/encoding-base-clingo.lp

## :material-download-outline: Download

In the future you will be able to download the benchmark set here.
