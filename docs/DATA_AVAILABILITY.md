# Data availability

This repository is prepared as a GitHub-only research asset repository for the EAGLE-YOLO manuscript submitted to Artificial Intelligence in Agriculture.

The manuscript file itself is excluded from version control. Research assets, including dataset files, experimental images, model checkpoints, field-trial spreadsheet data, and field-trial video, are intended to be uploaded to GitHub using Git LFS.

Because the repository contains tens of GB of data, users must install Git LFS before cloning the full repository:

```bash
git lfs install
git clone https://github.com/zhiyizhang0220/EAGLE-YOLO.git
cd EAGLE-YOLO
git lfs pull
```

## Dataset

The `dataset/` directory contains the maize seedling detection dataset in YOLO format with image and label splits. The dataset contains 3160 RGB images and 14,585 annotated maize seedling instances. The split is 2212 training images, 474 validation images, and 474 test images.

## Experimental assets

- `benchmark_results/`: representative detector comparison outputs and checkpoints.
- `ablation_studies/`: model-module ablation outputs and checkpoints.
- `dataset_ablation/`: data augmentation and dataset ablation outputs.
- `generalization_tests/`: cross-dataset and unseen-domain robustness outputs.
- `visualization/`: qualitative detection visualizations.
- `Field Trial Data.xlsx`: closed-loop field trial spreadsheet.
- `Field Trial Video.mp4`: closed-loop field trial video.

## Restrictions and responsibilities

The dataset was collected in agricultural field environments. Users should respect the scientific citation, repository license, and any additional terms added by the authors before publication. If exact farm-level location information or unpublished manuscript content is not required for reuse, users should cite only the published paper and this repository.
