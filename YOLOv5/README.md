# Steps to train YOLOv5 using palm oil ffb dataset
1) Save a copy of "Training of YOLOv5 on Palm Oil FFB" Google Colab notebook to your own google drive by clicking >>File >> Save a copy in Drive
2) Download the palm oil ffb dataset and upload it to google drive
3) Modify the "PALM.yaml" file according the the specific file path in your google drive, number of classes in this case is 4 ['Overipe','Ripe','Underipe','Unripe']. 
4) Spefify the runtime by clicking Runtime >> Change runtime type >> Hardware accelerator >> GPU
5) If you have subscribed to Colab pro, you may choose "V100" as the "GPU type". Otherwise, you may choose "T4" if you are a free user.
6) Start the training by running the cells in Google Colab until the "training" section and the training process will start.
7) You may modify the "freeze" parameter in the training cell to specify number of layers for trainig. [85 = train the last 20 layers, 90 = train the last 15 layers]
8) After the training is completed, you may run the remaining cells to convert the model to onnx model. 

Error:
If there is error during the training, go the dataset file("train" and "valid") in google drive and delete the file named "labels.cache" in both of the "train" and "valid" file.
