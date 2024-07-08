# A deep learning harmonization of multi-vendor MRI for robust intervertebral disc segmentation

![network](https://github.com/Chae-Woo/Harmonisation/assets/45866328/fe62955e-6ee3-4f62-8eb2-824b76f74a86)

Overall architecture of the proposed harmonization model. (a) The proposed model combines a CycleGAN-based model and two segmentation networks
(S_x, S_y). The G_xy maps the source (non-standard) image x to target (standard) image y for our goal (robust segmentation performance). The segmentation networks enhance the features for disc segmentation while
training the CycleGAN. The S_y was pre-trained on the target images in advance, and the S_x is not pre-trained but incorporated for cycle balance. The
pre-trained S_y provides the ground truths (GTs; green and orange boxes) to calculate the dice loss functions (dash-dotted lines). The RF (radiomic feature) loss is calculated from the
ROI of the harmonized image by comparing it with the pre-obtained RF values from the target images (red line). (b) The G_xy trained in (a) can harmonize
diverse MR images to predict the segmented results via the S_y trained on the target images.
