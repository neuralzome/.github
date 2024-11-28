# Challanges
## Camera calibration challange
Write a python script to obtain camera intrinsics (f, cx, cy & distortion_parameters). Use [camera_calibration](https://huggingface.co/datasets/neuralzome/camera_calibration) dataset to test your code.

Usage:
```bash
./estimate_camera_intrinsics.py --path_to_data_dir ./camera_calibration/checkerboard --data_type checkerboard --distortion_model radtan
```

where,
* `--path_to_data_dir`: Path to directory containing images. 
* `--data_type`: Options are 'checkerboard' and 'tagboard'. Reff dataset to see sample images.
* `--distortion_model`: Options are none (i.e. no distortion), [radtan](https://docs.tangramvision.com/metrical/core_concepts/component_models/cameras/#opencv-radtan), [fisheye](https://docs.tangramvision.com/metrical/core_concepts/component_models/cameras/#opencv-fisheye).

Also write a script to remove distortion from image and show it side by side for comparision.

Usage:
```bash
./undistort.py --path_to_img ./camera_calibration/checkerboard/1.png --distortion_model radtan --distortion_parameters -0.37551811  0.15834749  0.00347281 -0.00174248 -0.03258636
```
