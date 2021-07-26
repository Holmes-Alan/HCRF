# Hierarchical CNN based Random Forests (HCRF) approach for face super-resolution
We propose a novel approach of CNN and Random Forests for 8x facial image super-resolution. We claim the following points:

• A Siamese Network for Low-Resolution facial image segmentation. 

• Random Forests based model for facial feature reﬁnement.

Please cite our work if you use our code or dataset as,
# BibTex

        @InProceedings{Liu2021refvae,
            author = {Zhi-Song Liu, Wan-Chi Siu and Yui-Lam Chan},
            title = {Features Guided Face Super-Resolution via Hybrid Model of Deep Learning and Random Forests},
            booktitle = {IEEE Transactions on Image Processing},
            volume = {30},
            page = {4157-4170},
            year = {2021}
        }
        
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
  https://drive.google.com/open?id=1MYXyk0J_P3u6NV-x6m4Q73BG3wzVm2T2
  
  https://drive.google.com/open?id=15uCll3pwgOV9wkQYP-ag2RQypESnA6rQ
  
# Experimental results
1. We compared our proposed approach with state-of-the-arts face image SR approaches on objective quality by using PSNR and SSIM as follow

| Dataset  | Eval  | Bicubic  | SRCNN  | VDSR  | SRResNet  | UR-DGN  | FSRNet  | Proposed  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| HELEN-50  | PSNR  | 23.69 |  23.97 | 24.61  | 25.30  | 24.22  | 26.21  | 27.08  |
|   | SSIM  | 0.6592  | 0.6779  | 0.6980  | 0.7297  | 0.6909  | 0.7720  | 0.8139  |
| CelebA-1000  | PSNR  | 23.75  | 24.26  | 24.83  | 25.82  | 24.63  | 26.60  | 26.81  |
|   | SSIM  | 0.6423  | 0.6634  | 0.6878  | 0.7369  | 0.6851  | 0.7628  | 0.7731  |

    We also calculate the Cosine Similarity on HELEN dataset as follow
   
| Model  | Bicubic  | SRCNN  | VDSR  | UR-DGN  | MNCE  | FSRNet  | Proposed  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| Cos. Sim  | 0.9858  | 0.9889  | 0.9872  | 0.9906  | 0.9912  | 0.9929  | 0.9931  |

2. We also compared different approaches on subjective quality by using OpenFace toolbox to measure similarity of facial features. The lower the better. We tested the results on Helen testing datasets

![Similarity Comparison](https://github.com/Holmes-Alan/Face-SR/blob/master/results/Simi_Compare.png)

3. Visual Comparison

![Visual Comparison](https://github.com/Holmes-Alan/Face-SR/blob/master/results/VQ_Compare.png)
