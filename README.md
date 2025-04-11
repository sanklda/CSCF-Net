# CSCF-Net  
-----Code------
Cross-Scale Context-Aware Ship Detection in SAR Images using CSCF-Net  

The source code of the proposed algorithm in this paper are given in this folder.
## Catalogue
1.Environment  
2.Dataset processing  
3.How to train 
4.How to predict
5.Dataset Source  
6.Key code interpretation  
7.Others  
8.Conclusion  
## Environment  
    python: 3.10.14
    torch: 2.2.2+cu121
    torchvision: 0.17.2+cu121
    timm: 1.0.7
    mmcv: 2.2.0
    mmengine: 0.10.4
## Dataset processing
The training is conducted using the YOLO format.  
We have provided examples of the .txt file in the trainingdataset_record.、
## How to train
Run train.py for detection, and then enter the image path for detection.  
Notice that model and data are changed to your own paths.  
model points to the trained weight file.
Run val.py to obtain the evaluation results, which will be saved in the run folder.
## DataSet Source
The HRSID dataset we used in this paper comes from:  
Wei S, Zeng X, Qu Q, et al. HRSID: A high-resolution SAR images dataset for ship detection and instance segmentation[J]. Ieee Access, 2020, 8: 120234-120254.
## Key code interpretation
`train.py` The full implementation of a YOLO-based object detection model with support for one images as input.  
## Others 
Support different size model training, respectively, s, m, l, x version of yolo11.
## Conclusion
This paper proposes a Cross-Scale Context Fusion Network and a Task-Alignment Detection Head to achieve more accurate SAR target detection performance. The MSFF module and the MTIDH module are the two core components that enable this functionality. In this study, the HRSID and LS-SSDD-v1.0 datasets were used as the training sets for experiments. The experimental results demonstrate that the proposed method effectively integrates contextual information across different scales, providing richer target features and enhancing the accuracy of SAR target detection. In future work, we will continue to explore the application of multi-scale fusion in SAR target detection scenarios.
## Academic citation  
If you need to use our program, please quote in one format  
```latex
@article{qi2025cscfnet,
  title={Cross-Scale Context-Aware Ship Detection in SAR Images using CSCF-Net},
  author={Qi, Huang ,Guo , Tvz},
  journal={The visual computer},
  year={2025},
  code={https://github.com/sanklda/CSCF-Net}
}
