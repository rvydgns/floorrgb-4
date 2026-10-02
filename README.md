# FloorRGB-4

**FloorRGB-4** is a four-class RGB image dataset developed for indoor floor-surface classification.

The dataset contains **2,245 manually labeled images** from four surface classes:

- Concrete
- Epoxy
- Parquet
- Rubber

Images were collected from **more than 15 indoor environments** under varying lighting conditions and using **seven different smartphone models**.

## Dataset Distribution

| Subset | Concrete | Epoxy | Rubber | Parquet | Total |
|---|---:|---:|---:|---:|---:|
| Training | 459 | 444 | 429 | 464 | 1,796 |
| Validation | 58 | 56 | 54 | 58 | 226 |
| Test | 57 | 55 | 53 | 58 | 223 |
| **Total** | **574** | **555** | **536** | **580** | **2,245** |

## Data Collection

Images were captured using handheld smartphones in different indoor environments.

The acquisition conditions include variations in:

- natural and artificial lighting,
- time of day,
- camera characteristics,
- viewing conditions.

Each image was manually labeled according to its corresponding physical floor surface.

## Dataset Structure

```text
dataset/
├── train/
│   ├── concrete/
│   ├── epoxy/
│   ├── parquet/
│   └── rubber/
├── validation/
│   ├── concrete/
│   ├── epoxy/
│   ├── parquet/
│   └── rubber/
└── test/
    ├── concrete/
    ├── epoxy/
    ├── parquet/
    └── rubber/
```

The provided train, validation, and test splits correspond to those used in the associated study.

## Preprocessing

The original image resolutions vary across acquisition devices.

For the associated experiments, all images were loaded as RGB data and resized to **224 × 224 pixels** before being provided to the classification models.

The 224 × 224 resolution therefore represents the **model input size**, not necessarily the original image resolution.

Random online augmentation was applied only to training images. Validation and test images were resized without random augmentation.

## Download

Dataset images are stored using **Git LFS**.

```bash
git lfs install
git clone https://github.com/rvydgns/floorrgb-4.git
cd floorrgb-4
git lfs pull
```

## Metadata

The `metadata/` directory contains:

- `manifest.csv` — file paths, labels, split information, file sizes, and SHA-256 hashes
- `class_counts.csv` — class-wise image counts
- `checksums.sha256` — dataset integrity checksums

## Intended Use

FloorRGB-4 is intended for research on:

- floor-surface classification,
- texture recognition,
- computer vision,
- deep learning,
- visual perception for mobile robotics.

## Version

**Version 1.0.0**

2,245 images · 4 classes · Fixed train/validation/test split

## License

This dataset is released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

See [`LICENSE`](LICENSE) for details.

## Citation

Formal citation information will be added after completion of the associated paper review process.

Until then, the dataset may be referenced as:

**FloorRGB-4, Version 1.0.0.**
