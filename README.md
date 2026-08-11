# MQBac

MQBac (Meta Quantum Backend) is the backend-selection and runtime-estimation half of **SeleQtor**. It consumes the metrics and features collected by [QBacMet](https://github.com/srikarchundury/QBacMet) and turns them into actionable decisions for Q-HPC job placement.

[![IEEE QCE 2026](https://img.shields.io/badge/IEEE%20QCE%20'26-SeleQtor-lightgrey.svg)]()
*(paper link will appear at IEEE Xplore once published)*

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](LICENSE)

## Goals

MQBac targets two goals:

1. **Auto-select a QPM backend for QFw**, at the same place where MPI processes are decided based on #qubits.

2. **Estimate the runtime** of a given quantum circuit/algorithm, for a chosen QPM backend (or one selected via goal 1), given the resources available to it (classical/quantum queue priorities, etc.).

Both goals are driven by the features/metrics collected by [QBacMet](https://github.com/srikarchundury/QBacMet).

## Contents

- `0_preprocess.ipynb` — preprocessing of raw QBacMet output into modeling-ready datasets
- `1_analyze.ipynb` — exploratory analysis of collected metrics/features
- `2_model.ipynb` — backend-selection and runtime-estimation models
- `get_more_data.ipynb`, `get_more_data_ibmq.ipynb`, `get_more_data_ionq.ipynb` — data collection notebooks per provider
- `qbacmet_analysis.ipynb` — analysis of QBacMet-collected metrics/features
- `bench_meta_gen.py` — benchmark metadata generation
- `final_data/` — processed datasets used for modeling
- `tables/`, `images/` — generated tables and figures

## Installation

```bash
git clone https://github.com/srikarchundury/MQBac.git
cd MQBac
pip install -r requirements.txt
```

## Related Tools

- [QBacMet](https://github.com/srikarchundury/QBacMet) — vendor-agnostic metrics/feature collector that MQBac consumes.

## Citation

If you use MQBac in your research, please cite:

```bibtex
@inproceedings{chundury2026seleqtor,
    author = {Chundury, Srikar and Kim, Seongmin and Gopalakrishnan Meena, Muralikrishnan and Lu, Chao and Suh, In-Saeng and Mueller, Frank},
    title = {SeleQtor: Intelligent Quantum Backend Selection and Runtime Estimation},
    year = {2026},
    booktitle = {IEEE International Conference on Quantum Computing and Engineering (QCE '26)},
    note = {To appear}
}
```

## License

MQBac is licensed under the [BSD 3-Clause License](LICENSE).
