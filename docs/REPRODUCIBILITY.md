# Reproducibility notes

## Git LFS

Install Git LFS before cloning the full repository:

```bash
git lfs install
git clone https://github.com/zhiyizhang0220/EAGLE-YOLO.git
cd EAGLE-YOLO
git lfs pull
```

## Environment

Create the template environment:

```bash
conda env create -f environment.yml
conda activate eagle-yolo
```

The exact training environment should be recorded before publication, including CUDA, PyTorch, Ultralytics, MMDetection, GPU model, and operating system versions.

## Assets

- YOLO-format dataset files are stored under `dataset/`.
- Benchmark detector outputs and checkpoints are stored under `benchmark_results/`.
- Module ablations are stored under `ablation_studies/`.
- Data augmentation ablations are stored under `dataset_ablation/`.
- Cross-dataset/generalization tests are stored under `generalization_tests/`.

## Integrity

Generate or refresh checksums before a release:

```bash
git lfs ls-files --long > metadata/lfs-files.txt
```

For a formal release, add SHA-256 checksums for major artifacts after all files are finalized.
