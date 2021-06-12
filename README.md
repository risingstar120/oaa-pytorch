# OAA-PyTorch
The PyTorch code for ["Integral Object Mining via Online Attention Accumulation"](http://openaccess.thecvf.com/content_ICCV_2019/papers/Jiang_Integral_Object_Mining_via_Online_Attention_Accumulation_ICCV_2019_paper.pdf), which is implemented based on the code of [psa](https://github.com/jiwoon-ahn/psa) and [ACoL](https://github.com/xiaomengyc/ACoL).  

## Installation
python3  
torch >= 1.0  
tqdm  
torchvision  
python-opencv

Download the [VOCdevkit.tar.gz](https://drive.google.com/file/d/1uh5bWXvLOpE-WZUUtO77uwCB4Qnh6d7X/view) file and extract it into data/ folder.

## Attention accumulation
```
cd OAA-PyTorch/
./train.sh 
```
After the training process, you can resize the accumulated attention map to original image size.
```
cd ./runs/exp1/
python res.py
```
For a comparison with the attention maps generated by the final classification model, you can generate them by
```
./test.sh
```
## Pre-accumulated maps and models [[link]](https://drive.google.com/drive/folders/1mu_rYkZ8hCiM0X9tjq04R0K-gJ17RPRU?usp=sharing)
## Integal Attention learning
If you want to skip the online attention accumulation process to train the integral model directly, Download the pre-accumulated maps and 
extract them to `exp1/`.
```
./train_iam.sh
./test_iam.sh
```
If you have any question about OAA, please feel free to contact [Me](https://pengtaojiang.github.io/) (pt.jiang AT mail DOT nankai.edu.cn). 
