# Perceptual-SR
new project for facial image SR

# Dependencies
    Python 2.XXX<3.0
    OpenCV 3.4.0
    Caffe 
    NVIDIA GPU + CUDA
    Jupyter Notebook
    Visual Studio 2015 X64

# Reimplementation
1. Face Coarse SR and Face segmentation
---------------------------------------
    run HCRF_main.ipynb on Jupyter Notebook. Modify the directories of files based on your working environment.

2. Random Forest refinement
---------------------------
    download the random forests models from 
    
  https://drive.google.com/open?id=1eiQDcYh-s1PAlFmr8-PHEQDaqRTKaJiF 

  https://drive.google.com/open?id=1sLDjUh8kSbTQFgj01KKrGpBB3Qmlr7yX

    to stage1 and stage2 folders and run HCRF_s3_RF_s1.exe and HCRF_s3_RF_s2.exe

3. Testing resulrs on Helen, CelebA and IJCAI dataset can be downloaded from 
----------------------------------------------------------------------------

# Experimental results
1. We compared our proposed HCRF with state-of-the-arts face image SR approaches on objective quality by using PSNR and SSIM as follow

| Dataset  | Eval  | Bicubic  | SRCNN  | VDSR  | SRResNet  | UR-DGN  | FSRNet  | HCRF(Proposed)  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| HELEN-50  | PSNR  | 23.69 |  23.97 | 24.61  | 25.30  | 24.22  | 26.21  | 27.08  |
|   | SSIM  | 0.6592  | 0.6779  | 0.6980  | 0.7297  | 0.6909  | 0.7720  | 0.8139  |
| CelebA-1000  | PSNR  | 23.75  | 24.26  | 24.83  | 25.82  | 24.63  | 26.60  | 26.81  |
|   | SSIM  | 0.6423  | 0.6634  | 0.6878  | 0.7369  | 0.6851  | 0.7628  | 0.7731  |

2. We also compared different approaches on subjective quality by using OpenFace toolbox to measure similarity of facial features. The lower the better. We tested the results on Helen testing datasets

![image](https://github.com/Holmes-Alan/Face-SR/blob/master/results/figure7.pdf)
