# Drone Detection Model
The provided model is a fine-tuned object detection model for real-time drone detection, built on Ultralytics YOLO11n and trained on the SynDroneVision synthetic drone dataset.
This model is subject to the licenses of its components.
<br>


## Base Model: Ultralytics Yolo11n
[Ultralytics's YOLO11n](https://docs.ultralytics.com/models/yolo11) is the smallest, ***nano*** variant of the Ultralytics YOLO11 computer vision model family, containing just 2.6 million parameters.
It is lightweight and optimized for high-speed edge deployment, mobile devices, and low-power hardware - ideal for a real-time object detection use-case.

| Property       | Details                        |
| -------------- | ------------------------------ |
| Version        | YOLO11n                        |
| Parameters     | 2.6M                           |
| Input Size     | 640 × 640                      |
| Task           | Object Detection               |
| Depth Multiple | 0.50                           |
| Width Multiple | 0.25                           |
<br>

Details:
* **Source:** [Ultralytics YOLO11](https://github.com/ultralytics/ultralytics/blob/main/docs/en/models/yolo11.md)
* **License:** [AGPL 3.0](https://github.com/ultralytics/ultralytics/blob/main/LICENSE)
* **Citation:** No formal research paper published; Jocher, G., & Qiu, J. (2024). *Ultralytics YOLO11* (v11.0.0). Ultralytics. https://github.com/ultralytics/ultralytics
<br>


## Dataset: SynDroneVision
[SynDroneVision](https://zenodo.org/records/13360116) is a synthetic dataset designed for drone detection tasks, providing diverse aerial scenarios and drone appearances to support robust model training.

| Property          | Details                                      |
| ----------------- | -------------------------------------------- |
| Task              | Object Detection                             |
| Classes           | 1 (Drone)                                    |
| Total Images      | 144,038 annotated RGB images                 |
| Train Split       | 131,238 images                               |
| Val Split         | 8,800 images                                 |
| Test Split        | 4,000 images                                 |
| Resolution        | 2560 x 1489                                  |
<br>

Details:
* **Source:** [Zenodo (Record 13360116)](https://zenodo.org/records/13360116)
* **License:** [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/legalcode.en)
* **Citation:** Lenhard et al. (2025). *SynDroneVision*. WACV 2025. DOI: [10.1109/WACV61041.2025.00742](https://doi.org/10.1109/WACV61041.2025.00742)
<br>


## Fine-tuning
This model was fine-tuned on the following system:

| Component        | Details                                                                 |
| ---------------- | ----------------------------------------------------------------------- |
| Operating System | Ubuntu 20.04                                                            |
| CPU              | 2 × Intel Xeon Gold 6330 @ 2.00GHz<br>(2 threads/core, 28 cores/socket) |
| GPU              | 2 × NVIDIA A100 80GB PCIe                                               |
<br>

***NOTE:*** For instructions on reproducing or retraining this model, please see [finetune.md](https://github.com/IntelLabs/Video-Curation-Sample/blob/main/doc/finetune.md).

