# RGB-Thermal Semantic Segmentation for Electric Power Scene

*[Dual-Space Graph-Based Interaction Network](https://github.com/hhujiang/DSGBINet) (DSGBINet)* is the RGB-T semantic segmentation method for electric power scene.

## RGBT Datasets for both Transmission Lines (TLs) and Transformer Substations (TSs)
We annotated the RGBT image pairs to build the datasets for both TL and TS scenes via [labelme](https://github.com/wkentaro/labelme), including:

### `RGBT-TL Dataset`
* Dataset with **600 pix-level annotated RGBT image pairs.**
* All images have been **calibrated, aligned and augmented.**
* Captured by a *DJI M300 RTK drone equipped with a [FLIR Vue Pro IR camera](https://www.flir.com/products/vue-pro/) and a binocular vision camera.*

### `RGBT-TS Dataset`
* Dataset with **400 pix-level annotated RGBT image pairs.**
* All images have been **calibrated, aligned and augmented.**
* Captured handheld by *cameras removed from the drone camera modules.*

### Dataset Augmentation
* **Perform power law** transformation on visual images to simulate changes of time.
* Enhance visual images with different interference including day, night, fog and snow conditions via **[ImageAug](https://github.com/paixi/ImageAug).**
* Generate fake thermal infrared images via **[pix2pix](https://github.com/phillipi/pix2pix).**

## Comparative Results
* **Comparative results (%) on [MFNet](https://github.com/haqishen/MFNet-pytorch) Dataset.**

The images are available in the [results](https://github.com/hhujiang/DSGBINet/tree/main/results) and the metrics are as follows：

| class | background | car | person | bike | curve | car stop | guardrail | color cone | bump |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| recall | 0.986319 | 0.951551 | 0.891679 | 0.851572 | 0.660197 | 0.567425 | 0.077723 | 0.819909 | 0.728204 |
| iou | 0.979125 | 0.873809 | 0.695004 | 0.647432 | 0.462921 | 0.434398 | 0.033048 | 0.616937 | 0.489138|

* **Comparative results (%) on [PST900](https://github.com/ShreyasSkandanS/pst900_thermal_rgb) Dataset.**

The images are available in the [results](https://github.com/hhujiang/DSGBINet/tree/main/results) and the metrics have been given in the paper.

## Note
We have signed a technical cooperation contract with Huawei on September 6, 2022, so the `RGBT-TLD` and `RGBT-TSD` datasets **are not publicly available for now.**
