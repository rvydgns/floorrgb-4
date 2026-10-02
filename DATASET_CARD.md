\# FloorRGB-4 Dataset Card



\## Dataset Description



FloorRGB-4 is a four-class RGB image dataset for indoor floor-surface classification.



The dataset consists of 2,245 manually labeled images representing concrete, epoxy, parquet, and rubber surfaces.



It was developed to provide a controlled dataset for investigating image-based surface recognition methods, particularly for computer vision and mobile robotic perception applications.



\## Dataset Composition



The complete dataset contains:



| Class | Number of Images |

|---|---:|

| Concrete | 574 |

| Epoxy | 555 |

| Parquet | 580 |

| Rubber | 536 |

| \*\*Total\*\* | \*\*2,245\*\* |



The predefined dataset split contains 1,796 training images, 226 validation images, and 223 test images.



\## Data Collection



Data were collected from more than 15 indoor environments.



Image acquisition was performed under different lighting conditions, including natural daylight and artificial indoor lighting, and at different times of the day.



Seven different smartphone models were used to provide variability in camera characteristics.



The photographs were acquired using handheld smartphones. The cameras were not mounted on a mobile robot during dataset acquisition.



\## Annotation



Each image was manually labeled according to the physical floor surface represented in the image.



The available labels are:



`concrete`



`epoxy`



`parquet`



`rubber`



The directory containing each image represents its class label.



\## Dataset Splits



A fixed training, validation, and test partition is provided.



| Subset | Concrete | Epoxy | Rubber | Parquet | Total |

|---|---:|---:|---:|---:|---:|

| Train | 459 | 444 | 429 | 464 | 1,796 |

| Validation | 58 | 56 | 54 | 58 | 226 |

| Test | 57 | 55 | 53 | 58 | 223 |



The published split corresponds to the partition used in the associated classification experiments.



\## Image Format and Preprocessing



Images are represented as RGB data.



Native image resolution may differ between images because multiple smartphone cameras were used for acquisition.



For the experiments associated with this dataset, each image was resized to 224 × 224 pixels during data loading before being passed to the classification network.



Therefore, 224 × 224 pixels should be interpreted as the model input resolution rather than the original acquisition resolution.



Random online augmentation was applied only to the training subset. Validation and test images were resized without random augmentation.



\## Metadata and Integrity



A manifest is provided at:



`metadata/manifest.csv`



The manifest records the dataset-relative filepath, split, class label, filename, file extension, size in bytes, and SHA-256 checksum of every image.



Dataset integrity can additionally be verified using:



`metadata/checksums.sha256`



Class and subset counts are available in:



`metadata/class\_counts.csv`



\## Intended Uses



FloorRGB-4 may be used for research on visual floor-surface classification, texture recognition, image classification, deep learning, mobile robotic perception, and related computer-vision tasks.



The fixed split can also be used to facilitate reproducible comparison between classification models.



\## Out-of-Scope Uses



The dataset was not designed for identifying every possible floor material or for guaranteeing performance in unrestricted outdoor or industrial environments.



It should not be interpreted as a comprehensive representation of all surface conditions, camera systems, geographical environments, or lighting conditions.



\## Known Limitations



The dataset contains only four surface categories.



Although images were collected from more than 15 environments and using multiple smartphone models, the dataset remains limited compared with the diversity of real-world flooring conditions.



Models trained exclusively on FloorRGB-4 may be sensitive to domain shifts caused by different cameras, floor materials, illumination, image viewpoints, contamination, wear, reflections, or other environmental conditions.



The dataset contains RGB images only and does not include depth, inertial, tactile, acoustic, or other sensor modalities.



\## Version



Version: \*\*1.0.0\*\*



Total images: \*\*2,245\*\*



Classes: \*\*4\*\*



\## License



FloorRGB-4 is distributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.



\## Citation



Formal citation information will be added after completion of the associated paper review process.

