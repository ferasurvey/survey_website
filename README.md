# A Survey on Facial Expression Recognition of Static and Dynamic Emotions

This is the official repository for our [paper](https://arxiv.org/pdf/2408.15777) entitled *“A Survey on Facial Expression Recognition of Static and Dynamic Emotions”*.

## Taxonomy Overview

![images/taxonomy_overview.png](images/taxonomy_overview.png)

Taxonomy of FER of static and dynamic emotions. We present a hierarchical taxonomy that categorizes existing FER models by input type, task challenges, and network structures within a systematic framework, aiming to provide a comprehensive overview of the current FER research landscape. First, we have introduced datasets, metrics, and workflow (including literature and codes) into a public GitHub repository. Then, image-based SFER and video- based DFER overcome different task challenges using various learning strategies and model designs. Following, we analyzed recent advances of FER on benchmark datasets. Finally, we discussed and concluded some important issues and potential trends in FER, highlighting directions for future developments.

## Comparisons with SOTA FER-related reviews

![images/comparisons.png](images/comparisons.png)

## Datasets

![images/Datasets.jpg](images/Datasets.jpg)

Image-based static facial frames (Above) and video-based dynamic facial sequences (Below) of seven basic emotions in the lab and wild. Samples are from (a) JAFFE, (b) CK+, (c) SFEW, (d) ExpW, (e) RAF-DB, (f) AffectNet, (g) EmotioNet, (h) CK+, (i) Oulu-CASIA, (j) DFEW, (k) FERV39k, and (l) MAFW.

### Video-based DFER Datasets

| **Categories**          |                | **Datasets**                                                                                                     | **Year** | **ECT** | **Emotion**                | **Training Numbers** | **Testing Numbers** |
|-------------------------|----------------|------------------------------------------------------------------------------------------------------------------|----------|----------|----------------------------|----------------------|---------------------|
| **Modality**             | **Scene**      |                                                                                                                  |          |          |                            |                      |                     |
| **Image-based SFER Datasets** | **Lab**         | [JAFFE](http://www.kasrl.org/jaffe.html)                                                                          | 1998     | P        | Sev                        | 213                  | 213                 |
|                         |                | [CK+](http://vasc.ri.cmu.edu/idb/html/face/facial_expression/)                                                    | 2010     | P/I      | Sev                        | 241                  | 241                 |
|                         |                | [MMI](https://mmifacedb.eu/)                                                                                      | 2010     | P        | Sev                        | 370                  | 370                 |
|                         |                | [Oulu-CASIA](http://www.cse.oulu.fi/CMV/Downloads/Oulu-CASIA)                                                     | 2011     | P        | Sev                        | 720                  | 240                 |
|                         |                | [RaFD](https://rafd.socsci.ru.nl/?p=main)                                                                         | 2010     | P        | Sev, C                     | 1,448                | 160                 |
|                         | **Wild**        | [FER-2013](https://medium.com/@birdortyedi_23820/deep-learning-lab-episode-3-fer2013-c38f2e052280)                | 2013     | P/I      | Sev                        | 28,709               | 3,589               |
|                         |                | [SFEW 2.0](https://cs.anu.edu.au/few/)                                                                            | 2011     | P/I      | Sev                        | 958                  | 436                 |
|                         |                | [EmotioNet](http://www.pitt.edu/~emotion/downloads.html)                                                          | 2016     | P/I      | Sev, C                     | 80,000               | 20,000              |
|                         |                | [RAF-DB](http://www.whdeng.cn/raf/model1.html)                                                                    | 2017     | P/I      | Sev, Com                   | 12,271               | 3,068               |
|                         |                | [AffectNet](http://mohammadmahoor.com/affectnet/)                                                                 | 2017     | P/I      | Sev, Con.                  | 283,901              | 3,500               |
|                         |                | [ExpW](https://mmlab.ie.cuhk.edu.hk/projects/socialrelation/index.html)                                           | 2017     | P/I      | Sev                        | 75,048               | 16,745              |
|                         | **Lab (3D)**    | [BU-3DFE](https://www.cs.binghamton.edu/~lijun/Research/3DFE/3DFE_Analysis.html)                                  | 2006     | P        | Sev                        | 2,000                | 500                 |
|                         |                | [Bosphorus](http://bosphorus.ee.boun.edu.tr/)                                                                     | 2008     | P        | Sev                        | 2,326                | 2,326               |
|                         |                | [4DFAB](https://ibug.doc.ic.ac.uk/resources/4dfab/)                                                               | 2018     | P/I      | Sev                        | 1,440k               | 360k                |
| **Video-based DFER Datasets** | **Lab**         | [CK+](http://vasc.ri.cmu.edu/idb/html/face/facial_expression/)                                                    | 2010     | P/I      | Sev                        | 241                  | 241                 |
|                         |                | [MMI](https://mmifacedb.eu/)                                                                                      | 2010     | P/I      | Sev                        | 1,450                | 1,450               |
|                         |                | [Oulu-CASIA](http://www.cse.oulu.fi/CMV/Downloads/Oulu-CASIA)                                                     | 2011     | P        | Six                        | 2,160                | 720                 |
|                         | **Wild**        | [AFEW 8.0](https://cs.anu.edu.au/few/AFEW.html)                                                                   | 2011     | P/I      | Sev                        | 773                  | 383                 |
|                         |                | [CAER](https://caer-dataset.github.io/)                                                                           | 2019     | P/I      | Sev                        | 9,240                | 2,640               |
|                         |                | [DFEW](https://dfew-dataset.github.io/)                                                                           | 2020     | P/I      | Sev                        | 12,000               | 3,000               |
|                         |                | [FERV39k](https://wangyanckxx.github.io/Proj_CVPR2022_FERV39k.html)                                               | 2022     | P/I      | SE                         | 35,887               | 3,000               |
|                         |                | [MAFW](https://mafw-database.github.io/MAFW/)                                                                     | 2022     | P/I      | Sev, C, A, D, H, Com        | 8,036                | 2,009               |

Summary of the in-the-lab or in-the-wild datasets with static and dynamic emotions for FER training and evaluation. ECT: Elicitation; P: Posed; I: Instinctive; Sev: Seven Emotions (Happy, Angry, Surprise, Fear, Sad, Disgust, Neutral); C: Contempt; A: Anxiety;  D: Disappointment; H: Helplessness; Com: Compound.

## Workflow of Generic Facial Expression Recognition

![images/Workflow.jpg](images/Workflow.jpg)

The workflow and main components of generic facial expression recognition.

## Image-based Static FER

Image-based static facial expression recognition (SFER) involves extracting features from a single image, which captures complex spatial information that related to facial expressions, such as landmarks, and their geometric structures and relationships. In the following, we will first introduce the general architecture of SFER, and then elaborate specific design of SFER methods from the challenge-solving perspectives, including disturbance-invariant SFER, 3D SFER, uncertainty-aware SFER, compound SFER, cross-domain SFER, limited-supervised SFER, and cross-modal SFER.

### General SFER

![images/gernearl_based_SFER_00.jpg](images/gernearl_based_SFER_00.jpg)

The architecture of general SFER. Figure is reproduced based on (a) CNN-based model, (b) GCN-based model, and (c) Transformer-based model.

### Disturbance-invariant SFER

![images/Disturbance_invariant_SFER_00.jpg](images/Disturbance_invariant_SFER_00.jpg)

The architecture of disturbance-invariant SFER. Figure is reproduced based on (a) Attention-based model (AMP-Net) and (b) Decomposition-based model.

### 3D SFER

![images/3D_SFER_00.jpg](images/3D_SFER_00.jpg)

The architecture of 3D SFER. Figure is reproduced based on (a) GAN-based learning (GAN-Int) and (b) Multi-view learning (MV-CNN).

### Uncertainty-aware SFER

![images/Uncertainy_aware_SFER_00.jpg](images/Uncertainy_aware_SFER_00.jpg)

The architecture of uncertainty-aware SFER. Figure is reproduced based on (a) the label uncertainty learning (LA-Net) and (b) data uncertainty learning (LNSU-Net).

### Compound SFER

Compound emotions refer to complex emotional states formed by the combination of at least two basic emotions, which are not independent, discrete categories but exist within a continuous emotional spectrum composed of multiple dimensions. Compared with discrete "basic" emotions or a few dimensions, compound emotions provide a more accurate representation of the diversity and continuity of human complex emotions.

### Cross-domain SFER

![images/crossdomain_sfer.jpg](images/crossdomain_sfer.jpg)

The architecture of cross-domain SFER. Figure is reproduced based on (a) the transfer learning-based model (CSRL) and (b) the adaption learning-based model (AGRA).

### Weak-supervised SFER

![images/Weak-supervised.jpg](images/Weak-supervised.jpg)

The architecture of weak-supervised SFER. Figure is reproduced based on the Ada-CM.

### Cross-modal SFER

![images/Cross-modal.png](images/Cross-modal.png)

The architecture of cross-modal SFER. Figure is reproduced based on the CEprompt.

## Video-based Dynamic Facial Expression Recognition

The video-based DFER involves analyzing facial expressions that change over time, necessitating a framework that effectively integrates spatial and temporal information. The core objective of DFER is to extract and learn the features of expression changes from video sequences or image sequences. Due to the complexity and diversity of input video or image sequences, DFER faces various task challenges. Based on different solution approaches, these challenges can be categorized into seven basic types: general DFER, sampling-based DFER, expression intensity-aware DFER, multi-modal DFER, static to dynamic FER, self-supervised DFER, and cross-modal DFER.

### General DFER

![images/generaldfer.png](images/generaldfer.png)

The architecture of general DFER. Figure is reproduced based on (a) CNN-RNN based model (SAANet) and (b) the transformer-based model (EST).

### Sampling-based DFER

![images/fig9-Sampling-based_dfer_00.jpg](images/fig9-Sampling-based_dfer_00.jpg)

The architecture of sampling-based DFER. Figure is reproduced based on explainable sampling (Freq-HD).

### Expression Intensity-aware DFER

Facial expressions are inherently dynamic, with intensity either gradually shifting from neutral to peak and back or abruptly transitioning from peak to neutral, making the accurate capture of these fluctuations essential for understanding expression dynamics.

### Static to Dynamic FER

The static to dynamic FER utilized the high-performance SFER knowledge to explore appearance features and dynamic dependencies.

### Multi-modal DFER

![images/multi_modal_fusion_dfer.png](images/multi_modal_fusion_dfer.png)

The architecture of multi-modal DFER. Figure is reproduced based on the fusion-based model (T-MEP).

### Self-supervised DFER

![images/Self_supervised_DFER_00.jpg](images/Self_supervised_DFER_00.jpg)

The architecture of self-supervised DFER. This is reproduced based on the MAE-DFER.

### Visual-Language DFER

![images/DFER_CLIP.png](images/DFER_CLIP.png)

The architecture of vision-language DFER. Figure is reproduced based on DFER-CLIP.

## Citation

If you find our work useful, please cite our paper:

```latex
@article{,
  author    = {Yan Wang, Shaoqi Yan, Yang Liu, Wei Song, Jing Liu, Yang Chang, Xinji Mai, Xiping Hu, Wenqiang Zhang, Zhongxue Gan},
  title     = {A Survey on Facial Expression Recognition of Static and Dynamic Emotions},
  journal   = {},
  year      = {2024},
}
```
