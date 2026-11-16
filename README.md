# Unified Real-time Video Stitching with Off-the-shelf Cameras

This dataset is updated and now available at [BaiduNetDisk](https://pan.baidu.com/s/1FcQy62cn-quB_1gLQS36TQ?pwd=a392) Code：a392.


# Abstract
Existing commercial omnidirectional cameras (ODCs) are costly to produce because they depend on specialized architectures, such as Insta360’s reflectors and Qualcomm’s folded optics.
While building an ODC system with off-the-shelf cameras substantially reduces production costs, the primary challenge is maintaining sufficiently small inter-camera baselines to ensure that post-stitching parallax in overlapping regions remains imperceptible to human vision.
This paper presents a systematic approach for constructing ODC systems from off-the-shelf cameras, with three key advantages: 1) High-quality stitching: we propose a novel video stitching pipeline combining offline‑calibration‑based global alignment, optical‑flow‑based online parallax optimization for local alignment, and temporal stabilization constraints from historical‑frame optical flows, thereby mitigating parallax and temporal instability; 2) Real-time performance: GPU-parallel implementations of local homography estimation, image warping, and blending enable real-time stitching; 3) Generality: the pipeline applies to any ODC system assembled from off-the-shelf cameras.
Combining the advantages above, we have designed an ODC system based on a pair of off-the-shelf fisheye cameras (220$^{\circ}$ field-of-view, FoV).
To evaluate the proposed system, we construct a test set containing 14 video sequences (39,988 images) with this ODC. On this set, our pipeline produces higher-quality stitched images than existing SOTA approaches and achieves up to 20 FPS on video streams.

# Instructions:
The dataset is collected by a dual‑fisheye camera system, where two 220° ultra‑wide‑angle fisheye lenses are fixed back‑to‑back. Only these two lenses can cover a full 360° spherical field‑of‑view. This design brings the following advantages for panoramic stitching dataset acquisition:

Minimized system complexity while maximizing the field‑of‑view coverage.
Limited overlapping regions, which motivates the development of more robust stitching algorithms.
The dataset consists of raw fisheye images captured by the dual‑fisheye camera, camera calibration parameters, and ERP images projected from the original fisheye frames.
