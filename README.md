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
Regarding the first dataset, we used resnet50 model for the transfer learning approach and some layers were added to it. We used earlystopping function in python to avoid overfitting.

Here is the general architecture of this model:
![ResNet50_dataset1](https://github.com/KouroshGerayeli/Data_Challenge_Daleth_2023/assets/92382815/aee6e310-56e9-4e61-bd8d-7e86a9fcae46)

![download (2)](https://github.com/KouroshGerayeli/Data_Challenge_Daleth_2023/assets/92382815/5fce25f3-766b-496f-8db3-7b636984ac62)
The figure above shows the changes of accuracy and validation accuracy over epoch.
---------------------------
For the second dataset we used Resnet101 and also we added a scheduler to keep track of the transfer learning rate. The scheduler multiplies the transfer learning rate by e^(-0.1). We also used early stopping method in order to avoid overfitting. 

Here is the general architecture of this model: 
![ResNet101_dataset2](https://github.com/KouroshGerayeli/Data_Challenge_Daleth_2023/assets/92382815/b95d8066-bf71-4bee-aabc-1ad8fdf56e0f)

In the code provided for this dataset, you can see that there is 'model.load_weight' line in which we loaded the suitable weight for this model when we did earlystpooing method manually. If you prefer to train the model and use the earlystopping function in python you can just comment 'model.load_weight' and train the model itself.

![Figure_1](https://github.com/KouroshGerayeli/Data_Challenge_Daleth_2023/assets/92382815/7214bdc6-8082-43c6-add6-d0c8a8eb3211)

This figure shows the validation metric changes in terms of epochs and score for the second dataset with 25 epochs.






