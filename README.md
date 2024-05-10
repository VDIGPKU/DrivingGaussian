# DrivingGaussian👋

This is the official implementation of **DrivingGaussian: Composite Gaussian Splatting for Surrounding Dynamic Autonomous Driving Scenes**.

[**Paper**](https://cvpr.thecvf.com/virtual/2024/poster/31081) | [Xiaoyu Zhou📧](xyrain.zhou@gmail.com), [Zhiwei Lin📧](zwlin@pku.edu.cn), [Xiaojun Shan📧](sxjailame@gmail.com), [Yongtao Wang📧](wyt@pku.edu.cn), [Deqing Sun📧](deqingsun@gmail.com), [Ming-Hsuan Yang📧](minghsuanyang@gmail.com)

## Update
* 2024/04/25 - Code: please sign the [application](https://github.com/VDIGPKU/DrivingGaussian/blob/main/DrivingGaussian%20Application.docx) to obtain the code
* 2024/03/13 - Pre-trained weights are released
* 2024/02/27 - Paper: Accepted by CVPR2024 👏
* 2023/12/07 - [**Webpage**](https://pkuvdig.github.io/DrivingGaussian/)

## Weights
Pre-trained weights for certain scenes are released:
[Google Cloud](https://drive.google.com/drive/folders/1O5juORTGcrpeK4nlbW7AVcTvBBtOir?usp=sharing)

## Requirements

## Setups
Please follow the [3DGS](https://github.com/graphdeco-inria/gaussian-splatting) to install the relative packages.
```bash
git clone https://github.com/VDIGPKU/DrivingGaussian
cd DrivingGaussian
git submodule update --init --recursive
conda create -n DrivingGaussian python=3.8 
conda activate DrivingGaussian

pip install -r requirements.txt
pip install -e submodules/depth-diff-gaussian-rasterization
pip install -e submodules/simple-knn
```

## Training
For training the driving scenes dataset, 
```bash
python train.py -s "data/nuscenes/sceneID/" -m "saved/checkpoints/"
```

## Rendering
Render the images with the following script
```bash
python render_combine.py -m "saved/checkpoints/"
```

## Tools and Preprocessing
```bash

```

## Acknowledgements
The overall code and renderer are based on [3DGS](https://github.com/graphdeco-inria/gaussian-splatting) and [4DGS](https://github.com/hustvl/4DGaussians). We sincerely thank the authors for their great work.

## License
The project is only free for academic research purposes, but needs authorization forcommerce. For commerce permission, please contact wyt@pku.edu.cn.
