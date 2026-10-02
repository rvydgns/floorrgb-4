\# FloorRGB-4



\*\*FloorRGB-4: A Four-Class RGB Dataset for Indoor Floor Surface Classification\*\*



FloorRGB-4 is an RGB image dataset developed for indoor floor-surface classification research. The dataset contains \*\*2,245 manually labeled images\*\* belonging to four surface classes: \*\*concrete, epoxy, parquet, and rubber\*\*.



The dataset was created to support research on visual surface recognition, including applications in computer vision and mobile robotics.



\## Dataset Overview



| Property | Description |

|---|---|

| Total images | 2,245 |

| Number of classes | 4 |

| Classes | Concrete, Epoxy, Parquet, Rubber |

| Image type | RGB |

| Training images | 1,796 |

| Validation images | 226 |

| Test images | 223 |

| Acquisition environments | More than 15 indoor environments |

| Acquisition devices | Seven different smartphone models |

| Labeling | Manual |

| Model input size used in the associated study | 224 × 224 pixels |



\## Class Distribution



| Subset | Concrete | Epoxy | Rubber | Parquet | Total |

|---|---:|---:|---:|---:|---:|

| Training | 459 | 444 | 429 | 464 | 1,796 |

| Validation | 58 | 56 | 54 | 58 | 226 |

| Test | 57 | 55 | 53 | 58 | 223 |

| \*\*Total\*\* | \*\*574\*\* | \*\*555\*\* | \*\*536\*\* | \*\*580\*\* | \*\*2,245\*\* |



\## Data Acquisition



Images were collected from \*\*more than 15 indoor environments\*\* under varying acquisition conditions.



The dataset includes variations in lighting conditions, including \*\*natural daylight and artificial indoor lighting\*\*, as well as images captured at different times of the day, including morning, afternoon, and late afternoon.



Seven different smartphone models were used during data collection to introduce variability in camera characteristics and image acquisition conditions.



Images were acquired using handheld smartphones rather than a robot-mounted camera.



Each image was manually assigned to its corresponding physical surface class.



\## Surface Classes



The dataset contains the following four categories:



\*\*Concrete\*\* — indoor concrete floor surfaces.



\*\*Epoxy\*\* — epoxy-coated floor surfaces.



\*\*Parquet\*\* — indoor parquet and wood-based floor surfaces.



\*\*Rubber\*\* — rubber floor surfaces.



\## Dataset Structure



The dataset is distributed using fixed training, validation, and test subsets.



```text

dataset/

├── train/

│   ├── concrete/

│   ├── epoxy/

│   ├── parquet/

│   └── rubber/

│

├── val/

│   ├── concrete/

│   ├── epoxy/

│   ├── parquet/

│   └── rubber/

│

└── test/

&#x20;   ├── concrete/

&#x20;   ├── epoxy/

&#x20;   ├── parquet/

&#x20;   └── rubber/

```



These predefined subsets correspond to the experimental splits used in the associated study and should be preserved when reproducing the reported experiments.



\## Image Preprocessing



The original image resolutions vary because the images were acquired using different smartphone cameras.



In the associated classification experiments, images from the training, validation, and test subsets were loaded as RGB data and resized to \*\*224 × 224 pixels\*\* before being provided to the classification networks.



The 224 × 224 resolution therefore represents the \*\*network input size\*\* and not necessarily the original resolution of the photographs contained in the dataset.



Online random data augmentation was applied \*\*only to training images\*\* during model training.



Validation and test images were resized without random augmentation.



\## Metadata



The repository contains additional files under the `metadata/` directory:



```text

metadata/

├── manifest.csv

├── class\_counts.csv

└── checksums.sha256

```



`manifest.csv` provides the relative file path, dataset subset, class label, filename, file extension, file size, and SHA-256 checksum for every image.



`class\_counts.csv` contains the number of images in each class and subset.



`checksums.sha256` can be used to verify dataset file integrity.



\## Intended Use



FloorRGB-4 is intended primarily for research and educational use in areas such as:



\- indoor floor-surface image classification,

\- computer vision,

\- deep learning,

\- texture recognition,

\- visual perception for mobile robotics,

\- evaluation of lightweight and real-time classification models.



The dataset may also be used for benchmarking new image-classification architectures under the provided fixed data split.



\## Limitations



FloorRGB-4 contains four indoor surface categories and should not be interpreted as representing all possible indoor or industrial flooring materials.



The dataset was collected in a limited number of physical environments and geographical locations. Models trained on the dataset may therefore exhibit reduced performance when evaluated under substantially different cameras, lighting conditions, surface appearances, or environments.



The dataset primarily addresses visual surface classification and does not contain depth, inertial, tactile, or other multimodal sensor measurements.



\## Reproducibility



The published training, validation, and test directories represent the dataset partition used for the associated experiments.



Researchers seeking to reproduce the reported results are encouraged to retain the provided directory structure and split assignments.



SHA-256 checksums are provided to enable verification of individual dataset files.



\## License



FloorRGB-4 is released under the \*\*Creative Commons Attribution 4.0 International (CC BY 4.0)\*\* license.



Users may share and adapt the dataset provided that appropriate credit is given to the dataset creators.



See the `LICENSE` file for details.



\## Citation



Citation information will be added after the associated paper review process is completed.



\## Version



\*\*FloorRGB-4 v1.0.0\*\*



This version contains 2,245 RGB images distributed across four surface classes and fixed training, validation, and test subsets.

