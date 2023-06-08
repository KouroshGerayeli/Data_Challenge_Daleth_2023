# Data_Challenge_Daleth_2023
Low Contrast Wave Anomalies Detection and Classification in Infrared Images

Three datasets were provided in this project.Each had two classes labeled with 'Ok' and 'vague'. For each of the datasets, .ipynb file is provided in this repository.
Dataset details : 

1.
- Balanced dataset
- 200 images
- Uniform format 640x512

2.
- Unbalanced dataset, ratio 7:1
- ~4000 images
- Uniform format 640x512

3.
- Unbalanced dataset, ratio 7:1
- ~5500 images
- Various formats


---------------------------
Regarding the first dataset, we used resnet50 model for the transfer learning approach and some layers were added to it.

Here is the general architecture of this model:
![ResNet50_dataset1](https://github.com/KouroshGerayeli/Data_Challenge_Daleth_2023/assets/92382815/aee6e310-56e9-4e61-bd8d-7e86a9fcae46)

---------------------------
For the second dataset we used Resnet101 and also we added a scheduler to keep track of the transfer learning rate. The scheduler multiplies the transfer learning rate by e^(-0.1). We also used early stopping method in order to avoid overfitting. 






