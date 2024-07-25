# DrivingGaussian👋

This is the official implementation of **DrivingGaussian: Composite Gaussian Splatting for Surrounding Dynamic Autonomous Driving Scenes**.

[**Paper**](https://cvpr.thecvf.com/virtual/2024/poster/31081) | [Xiaoyu Zhou](xyrain.zhou@gmail.com), Zhiwei Lin, Xiaojun Shan, Yongtao Wang, Deqing Sun, Ming-Hsuan Yang

## Update
* 2024/05/10 - Code: please sign the [application](https://github.com/VDIGPKU/DrivingGaussian/blob/main/DrivingGaussian%20Application.docx) to obtain the code
* 2024/03/13 - Pre-trained weights are released
* 2024/02/27 - Paper: Accepted by CVPR 2024 👏
* 2023/12/07 - [**Webpage**](https://pkuvdig.github.io/DrivingGaussian/)

### Demo
<img src="https://github.com/VDIGPKU/DrivingGaussian/blob/main/assets/video.gif" width="700"/>

### Qualitative Comparison
<img src="https://github.com/VDIGPKU/DrivingGaussian/blob/main/assets/teaser.png" width="700"/>

### Overview
<img src="https://github.com/VDIGPKU/DrivingGaussian/blob/main/assets/method.png" width="700"/>

### Corner Case Simulation
<img src="https://github.com/VDIGPKU/DrivingGaussian/blob/main/assets/cornercase.gif" width="700"/>

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


## Acknowledgements
The overall code and renderer are based on [3DGS](https://github.com/graphdeco-inria/gaussian-splatting), [Deformable](https://github.com/ingra14m/Deformable-3D-Gaussians), and [4DGS](https://github.com/hustvl/4DGaussians). We sincerely thank the authors for their great work.

## BibTex

```
@inproceedings{zhou2024drivinggaussian,
  title={Drivinggaussian: Composite gaussian splatting for surrounding dynamic autonomous driving scenes},
  author={Zhou, Xiaoyu and Lin, Zhiwei and Shan, Xiaojun and Wang, Yongtao and Sun, Deqing and Yang, Ming-Hsuan},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={21634--21643},
  year={2024}
}
```


## License
The project is only free for academic research purposes, but needs authorization forcommerce. For commerce permission, please contact wyt@pku.edu.cn.
