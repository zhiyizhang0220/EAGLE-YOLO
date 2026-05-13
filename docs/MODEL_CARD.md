# Model card

## Model name

EAGLE-YOLO.

## Base model

YOLO11n.

## Intended use

Real-time maize seedling detection for robotic intra-row weeding, crop-protection-zone construction, and field robotic perception on edge devices.

## Core modules

- EAS-Stem: preserves shallow edge and saliency cues.
- BDFM: supports global-local dual-stream feature interaction.
- EMBS-FPN: improves efficient multi-scale feature fusion.
- PowerAlign-LSCD: improves lightweight classification-localization quality alignment.

## Reported test performance

- mAP50: 99.0%.
- mAP75: 81.8%.
- mAP50:95: 71.5%.
- Parameters: 0.73 M.
- GFLOPs: 2.8.
- Model size: 2.0 MB.
- Jetson Orin NX average inference time: approximately 12 ms per frame.

## Validation scope

The model was evaluated through held-out testing, representative-detector comparisons, ablation studies, cross-dataset generalization tests, edge-device deployment, and closed-loop field trials.

## Limitations

The model is designed for maize seedling detection. Before use in other crops, growth stages, cameras, or weeding mechanisms, users should perform local validation and safety checks.
