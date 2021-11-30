# OverlapNet - Loop Closing for 3D LiDAR-based SLAM

### OverlapNet was nominated as the Best System Paper at Robotics: Science and Systems (RSS) 2020 

**This repo contains the pytorch implemention of OverlapNet.**   

OverlapNet is modified Siamese Network that predicts the overlap and relative yaw angle of a pair of range images generated by 3D LiDAR scans. 

Developed by [Xieyuanli Chen](http://www.ipb.uni-bonn.de/people/xieyuanli-chen/) and [Thomas Läbe](https://www.ipb.uni-bonn.de/people/thomas-laebe/).

This pytorch-implemention is developed by [Junyi Ma](https://github.com/BIT-MJY)  


## Publication
If you use our implementation in your academic work, please cite the corresponding [paper](https://www.ipb.uni-bonn.de/wp-content/papercite-data/pdf/chen2020rss.pdf):  
    
	@inproceedings{chen2020rss, 
			author = {X. Chen and T. L\"abe and A. Milioto and T. R\"ohling and O. Vysotska and A. Haag and J. Behley and C. Stachniss},
			title  = {{OverlapNet: Loop Closing for LiDAR-based SLAM}},
			booktitle = {Proceedings of Robotics: Science and Systems (RSS)},
			year = {2020},
			codeurl = {https://github.com/PRBonn/OverlapNet/},
			videourl = {https://www.youtube.com/watch?v=YTfliBco6aw},
	}




#### Training

```bash
python tools/training.py
```

#### Testing on KITTI00
```bash
python tools/gen_feature_map_kitti00.py
python tools/testing_kitti00.py
```


#### Data structure

The recommended data structure is as follows:

```bash
├── config
├── dataset_full
│   ├── 00
│       ├── 000000.bin
│	├── ...
│	└── 004541.bin
│   ├── 01
│   ├── ...
│   └── 10
├── loop_gt_seq00_0.3overlap_inactive.npz
├── modules
└── tools
    ├── amodel1.pth.tar
    └── feature_map_kitti00
```

## License

Copyright 2020, Xieyuanli Chen, Thomas Läbe, Cyrill Stachniss, Photogrammetry and Robotics Lab, University of Bonn.

This project is free software made available under the MIT License. For details see the LICENSE file.


