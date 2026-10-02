# FloorRGB-4 Dataset Card

## Overview

FloorRGB-4 is an RGB image dataset for four-class indoor floor-surface classification.

It contains **2,245 manually labeled images** from the following classes:

| Class | Images |
|---|---:|
| Concrete | 574 |
| Epoxy | 555 |
| Parquet | 580 |
| Rubber | 536 |
| **Total** | **2,245** |

The dataset is divided into:

- **1,796 training images**
- **226 validation images**
- **223 test images**

## Data Collection

Images were collected from **more than 15 indoor environments** using **seven different smartphone models**.

Acquisition conditions include natural daylight, artificial indoor lighting, and different times of the day.

Images were captured using handheld smartphones rather than a robot-mounted camera.

## Annotation

Each image was manually labeled according to the physical floor surface shown in the image.

Available labels are:

```text
concrete
epoxy
parquet
rubber
```

## Image Processing

Original image resolutions vary depending on the acquisition device.

For the associated experiments, images were loaded as RGB data and resized to **224 × 224 pixels**.

Random augmentation was applied only to the training subset.

Validation and test images were resized without random augmentation.

## Metadata

The repository provides:

- `metadata/manifest.csv`
- `metadata/class_counts.csv`
- `metadata/checksums.sha256`

SHA-256 hashes are included to support dataset integrity verification.

## Intended Use

The dataset is intended primarily for research in:

- surface classification,
- texture recognition,
- computer vision,
- deep learning,
- mobile robotic perception.

## Limitations

FloorRGB-4 contains only four indoor surface categories and does not represent all possible floor materials or environmental conditions.

Performance may vary when models are applied to substantially different cameras, lighting conditions, surface appearances, or environments.

The dataset contains RGB images only and does not include depth, inertial, tactile, or other sensor measurements.

## Version and License

**Version:** 1.0.0  
**License:** CC BY 4.0

Formal citation information will be added after completion of the associated paper review process.
