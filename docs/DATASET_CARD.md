# Dataset card

## Name

EAGLE-YOLO near-ground RGB maize seedling dataset.

## Purpose

The dataset supports maize seedling detection for crop-safe robotic intra-row weeding under complex field-imaging conditions.

## Collection sites

- Northwest A&F University experimental farm, Yangling, Shaanxi, China; cultivar Shandan 650.
- Xingtang, Shijiazhuang, Hebei, China; cultivar Nongda 108.

## Collection time

- Yangling: June 2024.
- Xingtang: July 2025.

## Acquisition setup

- Camera: Nikon Z5, 25-50 mm f/4-6.3.
- Mounting: top-down, approximately 0.8 m above ground.
- Resolutions: 1920 x 1080 and 4096 x 3072.
- Lighting windows: 08:00-10:00, 12:00-14:00, and 17:00-19:00.

## Dataset size

- Total images: 3160.
- Total maize seedling instances: 14,585.
- Yangling: 2225 images and 10,246 instances.
- Xingtang: 935 images and 4339 instances.
- Split: train/val/test = 2212/474/474.

## Annotation

- Format: YOLO text labels.
- Classes: 1 class, maize seedling.
- Box type: axis-aligned bounding boxes.
- Fully visible and partially occluded seedlings were labeled.
- Cases with only minimal boundary leaf tips and unreliable semantic discrimination were excluded to reduce label noise.

## Known limitations

The dataset is designed for maize seedling detection and crop-protection perception. It does not annotate weeds as target classes. Performance outside maize seedling-stage intra-row weeding scenarios should be evaluated before deployment.
