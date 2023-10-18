# DSEC-MOT

## Introduction
Welcome to the new challenging event-based multi-object tracking dataset (DSEC-MOT) repository. Our goal is to provide a challenging and diverse event-based MOT dataset with various real-world scenarios to facilitate the objective and comphrehensive evaluation of event-based multi-object tracking algorithms. This dataset, built upon [DSEC](https://dsec.ifi.uzh.ch/), contains a variety of traffic entities and complex scenarios, aiming to address the current lack of event-based MOT datasets.

<div align=center>
<img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_00_b.gif" width="240">  <img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_01_d.gif" width="240">  <img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_01_e.gif" width="240">
</div>

<div align=center>
<img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_04_b.gif" width="240">  <img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_09_d.gif" width="240">  <img src="https://github.com/wshku/DSEC-MOT/blob/main/figures/zurich_city_01_e_2.gif" width="240">
</div>

## Citation
When using this dataset in an academic context, please cite the following publication:
```
@article{wang2023spikemot,
  title={SpikeMOT: Event-based Multi-Object Tracking with Sparse Motion Features},
  author={Wang, Song and Wang, Zhu and Li, Can and Qi, Xiaojuan and So, Hayden Kwok-Hay},
  journal={arXiv preprint arXiv:2309.16987},
  year={2023}
}
```

## Dataset Statistics
DSEC-MOT contains:
- 12 annotated sequences with a total of 37,080 boxes, 502 tracks, and 769.2-second duration
- 7 object classes including cars, pedestrians, bicycles, motorcycles, buses, trucks, and trains
- Challenging scenarios including crowded urban areas and rural scenes with various lighting conditions
- Severe occlusions, making the dataset suitable for testing trackers' occlusion handling capabilities
- Event resolution 640 $\times$ 480

![DSEC-MOT visual representation](https://github.com/wshku/DSEC-MOT/blob/main/figures/overview_dsecmot.png)

## Download
[DSEC event files](https://dsec.ifi.uzh.ch/dsec-datasets/download/)  
[Annotation files](https://drive.google.com/drive/folders/1BMzf-mAq1-pwtCWc7zw3KoYYF4igZXAj?usp=sharing) (1.0 MB)

## Annotation Format
The annotation data for the DSEC-MOT dataset is stored in txt files, with each annotation occupying a single line. 

The format of the annotation is as follows:  
`[timestamp, track ID, box left, box top, box width, box height, class ID]`

- `timestamp` represents the time at which the specific object is annotated
- `track ID` is assigned for each unique object being tracked in the event sequence
- `box left` and `box top` denote the coordinates of the top-left corner of the bounding box
- `box width` and `box height` specify the dimensions of the bounding box surrounding the object
- `class ID` indicates the class of the object being tracked

| Class ID |    Label    |
|:--------:|:-----------:|
| 0        | Car         |
| 1        | Pedestrians |
| 2        | Bicycles    |
| 3        | Motorcycles |
| 4        | Buses       |
| 5        | Trucks      |
| 6        | Trains      |

Example annotation:  
`[54828357559, 10, 178, 222, 100, 70, 0]`

This example annotation represents a car appearing at the timestamp 54828357559 microsecond, with a unique track ID of 10. The bounding box for this object has its top-left corner at coordinates (178, 222) and dimensions of width 100 and height 70.

---
We hope our DSEC-MOT dataset contributes to advancing research in event-based multi-object tracking. If you have any questions or issues, feel free to reach out to us or open an issue in this GitHub repository. Enjoy tracking!

