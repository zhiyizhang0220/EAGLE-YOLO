# EAGLE-YOLO

**EAGLE-YOLO: An edge-aware lightweight detector for real-time maize seedling detection in robotic intra-row weeding**

This repository provides the research assets for the manuscript submitted to **Artificial Intelligence in Agriculture**. EAGLE-YOLO is an edge-aware lightweight detector built on YOLO11n for real-time maize seedling detection under complex field conditions. The method integrates EAS-Stem, BDFM, EMBS-FPN, and PowerAlign-LSCD to preserve shallow edge cues, enhance global-local feature interaction, improve multi-scale fusion, and align lightweight prediction quality.

## Authors

Zhiyi Zhang, Zhuohuai Guan, Saisai Liu, Shenghong Wei, Mengdi Luo, Jiahe Tang, Yuxiang Huang, Guangqiao Cao, and Zhiqi Zheng.

Corresponding authors: Guangqiao Cao (caoguangqiao@126.com) and Zhiqi Zheng (zhiqizheng@nwsuaf.edu.cn).

Affiliations include Hainan Institute of Northwest A&F University; Nanjing Institute of Agricultural Mechanization, Ministry of Agriculture and Rural Affairs; College of Mechanical and Electric Engineering, Northwest A&F University; and Scientific Research Base for Conservation Tillage Mechanization (Yellow River Basin), Ministry of Agriculture and Rural Affairs.

## Repository status

- Manuscript status: under review.
- Target journal: Artificial Intelligence in Agriculture.
- DOI: not available yet.
- The manuscript `.docx` file is intentionally excluded from version control.
- Large images, videos, spreadsheets, and model weights are tracked with **Git LFS**.

## Repository structure

```text
.
|-- dataset/                # YOLO-format maize seedling images and labels
|-- visualization/          # Detection visualizations and qualitative outputs
|-- benchmark_results/      # Comparison experiments with representative detectors
|-- ablation_studies/       # Model-module ablation results
|-- dataset_ablation/       # Data augmentation and dataset ablation results
|-- generalization_tests/   # Cross-dataset and unseen-domain robustness tests
|-- docs/                   # Data, model, ethics, and reproduction notes
|-- metadata/               # Generated manifests and integrity metadata
|-- Field Trial Data.xlsx   # Field closed-loop intra-row weeding trial data
`-- Field Trial Video.mp4   # Field trial video record
```

## Dataset summary

The newly collected near-ground RGB maize seedling dataset contains **3160 images** and **14,585 maize seedling instances**. Images were collected at the Northwest A&F University experimental farm in Yangling, Shaanxi, China and in Xingtang, Shijiazhuang, Hebei, China. The train/validation/test split is **2212 / 474 / 474**. The annotation format is single-class, axis-aligned YOLO bounding boxes for maize seedlings.

Key collection conditions:

- Camera: Nikon Z5, 25-50 mm f/4-6.3.
- Mounting: top-down, approximately 0.8 m above ground.
- Resolutions: 1920 x 1080 and 4096 x 3072.
- Collection windows: 08:00-10:00, 12:00-14:00, and 17:00-19:00.
- Cultivars: Shandan 650 and Nongda 108.

See [`docs/DATASET_CARD.md`](docs/DATASET_CARD.md) for details.

## Key reported results

On the held-out test set, EAGLE-YOLO achieved:

- mAP50: **99.0%**
- mAP75: **81.8%**
- mAP50:95: **71.5%**
- Parameters: **0.73 M**
- GFLOPs: **2.8**
- Model size: **2.0 MB**
- Jetson Orin NX average inference time: approximately **12 ms per frame**

In closed-loop field trials, EAGLE-YOLO reduced crop damage from 18.47% to 7.59%, increased weeding success from 77.78% to 89.99%, and reduced invalid actuation from 37.64% to 8.41%.

## Git LFS requirement

This repository is intentionally GitHub-only, so large research files are stored with Git LFS. Before cloning or pulling the full repository, install Git LFS:

```bash
git lfs install
git clone https://github.com/zhiyizhang0220/EAGLE-YOLO.git
cd EAGLE-YOLO
git lfs pull
```

GitHub Free/Pro accounts include limited LFS quota. This repository is approximately tens of GB and may require additional Git LFS storage/bandwidth or a GitHub Team plan.

## Environment

The repository contains experimental assets from YOLO-family and MMDetection-style experiments. A minimal environment template is provided in [`environment.yml`](environment.yml). Exact environment versions should be verified against the training machine before publication.

## Reproduction notes

The stored folders contain datasets, validation outputs, model checkpoints, training logs, comparison results, ablation results, and field-trial assets. See:

- [`docs/REPRODUCIBILITY.md`](docs/REPRODUCIBILITY.md)
- [`docs/MODEL_CARD.md`](docs/MODEL_CARD.md)
- [`docs/FIELD_TRIAL.md`](docs/FIELD_TRIAL.md)

## Citation

If you use this repository, please cite the manuscript once published. A provisional citation file is provided in [`CITATION.cff`](CITATION.cff).

## License

The repository currently uses the MIT License for code and documentation. Dataset and model-weight reuse terms should be confirmed by the authors before journal publication; see [`docs/DATA_AVAILABILITY.md`](docs/DATA_AVAILABILITY.md).
