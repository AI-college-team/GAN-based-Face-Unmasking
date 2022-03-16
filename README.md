  

<p>
<a  href="https://github.com/hanakim120/GAN-based-Face-Unmasking"><img  src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fhanakim120%2FGAN-based-Face-Unmasking&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>

GAN ��� ����ũ�� ������ �� �̹��� ���� ���� 'Mask2Face'
============================
<p  align="center">
<img  src="./image/logo.png"  width="80%"  align="middle"/>
</p>

## ? Quick overview

#### ����Ʈ �ڷγ� �ô��� ������ �߾��� ��Ű�� ���� ����ũ ������ ��/���� ����

> 1) ������� ����ũ �� ������ ����ũ �κ� Ž�� (Detect Module)
> 2) GAN�� �̿��� ����ũ �� �󱼰� �ڿ������� ��︮�� �� �̹��� ���� (Editor Module)
> 3) ������� �Ǿ� ������ �޾� ������ �󱼰� �� �����ϰ� �̹��� ���� (Face Swap)

- �ڼ��� ������ �Ʒ� ���� ��ǥ �ڷḦ �������ּ���

  
## ? ���� �� ��ǥ �ڷ�

- KAIST SW �������� 2021 ���� AI Į���� ��Ʈ������ ������Ʈ ����� ���� ([link](https://drive.google.com/file/d/1DAgwf9nh3Q2QzTY6EZaIoPVGEnaX11dl/view?usp=sharing))

- Demo Video ([link](https://drive.google.com/file/d/19lh7OmpyMmUEsqIwLp2RscjDyqjgnCnK/view?usp=sharing)) 

- ���� ��ǥ �ڷ� ([link](https://drive.google.com/file/d/1O5R8_9GVTeDSfEUj4zTqSLshJgOFP_f2/view?usp=sharing))

  

## ������Ʈ �� ����
<p  align="center">
<img  src="./image/entire_module.png"  width="80%"  align="middle"/>
</p>




  

## Train model ������

<p  align="center">
<img  src="./image/detector_train.png"  width="80%"  align="middle"/>
</p>

<p  align="center">
<img  src="./image/editor_train.png"  width="80%"  align="middle"/>
</p>

## Skills
<p  align="center">
<img  src="./image/skills.png"  width="80%"  align="middle"/>
</p>


## Folder structure

this repo
�� controller.py
��
��������configs
�� config.py
�� detect.yaml
�� edit.yaml
��
��������dataprepare
�� ��������img_binary
�� ��������img_gt
�� ��������img_mask
�� mask.py
�� numalign.py
��
��������detector
�� ��������detect_result_img
�� ��������weights
�� ��������image
�� detect_model.py
�� detect_trainer.py
�� preprocessing_detect.py
�� sharpening.py
��
��������editor
�� ��������results
�� ��������weights
�� edit_model.py
�� edit_trainer.py
�� preprocessing_edit.py
��������loss
�� adversarial.py
�� dice.py
�� ssim.py
��
��������matrics
�� dicecoeff.py
�� pixelacc.py
��
��������face_swap
�� ��������content
�� ��������imgs
�� ��������models
�� ��������results
�� face_detection.py
�� face_swap.py
�� main.py

## Data set

- AFD(Asian Face Dataset) + BUPT(BUPT Dataset)

- 160 * 160, �� 10,000���� �ȸ� ������ ���

  

## Training Results Sample

<p  align="center">
<img  src="./image/train_result_1.png"  width="80%"  align="middle"/>
<img  src="./image/train_result_2.png"  width="80%"  align="middle"/>
</p>


## Results ()

| | |

|:-------------------------:|:-------------------------:|

|<img  width="900"  alt="screen"  src="./image/train_result_1.png"> | <img  width="900"  alt="screen"  src="./image/train_result_2.png"> |

  

## Face Swap scripts
- test4.jpg �� test6.jpg�� ���� swap

    python main.py --src imgs/test6.jpg --dst imgs/test4.jpg --out results/output6_4.jpg --correct_color

    
## Paper References

-  [A Novel GAN-Based Network for Unmasking of Masked Face](https://ieeexplore.ieee.org/abstract/document/9019697)

  

## Code References

- GAN Generator, Discriminator from https://github.com/kaylode/facemask-removal

- Crop from https://github.com/ternaus/facemask_detection

- Mask detection from https://wjddyd66.github.io/pytorch/Pytorch-Unet/

- Face Swap from https://github.com/wuhuikai/FaceSwap.git

- Mask generator from https://github.com/prajnasb/observations

  

## Book References

- ī�϶� ��������(2019), ����! GAN ������Ʈ(������ ���̾� �ø��� 43), ��Ű�Ͻ�

- Ȳ����(2019), OpenCV 4�� ���� ��ǻ�� ������ �ӽ� ����, �������Ǳ��

  

## License

[![License: LGPL v3](https://img.shields.io/badge/License-MIT-g.svg?style=flat-square)](https://tldrlegal.com/license/gnu-lesser-general-public-license-v3-(lgpl-3))

- Copyright ? [Hana Kim](https://github.com/hanakim120).
