# DP3_Jr.NTR_detection
step 1: data collection 
  I have collected the images of actor Jr.NTR one of the main leads of recent block buster RRR.
step 2: Labeled them in Roboflow
  The collected data was labeled in Roboflow with a total 93 images splitted into training, testing and validation sets with 59, 9 and 25 respectively.
step 3: Loading and Augmentation
  * The labeled data was then loaded into google colab by using the APi key in the COCO format.
  * Since, this dataset is very small, I augumented it for which I build a augmentation pipeline using albumentation module and saved it in a folder in labelme format.
step 4: Data pipelining
  The agumented images and labels which are saved then passed into a tensorflow data pipeline seperately with 8 images and labels in a batch without shuffling  and then ziped    together and shuffled.
step 6: Build Model
  I built two models with different heads and VGG16 as the back bone. The model architectures are provided in the same repo as .png images.
step 5: Define loss function
  * For training the data, I used adam optimizer and for clssification, BinaryCrossEntropy was used.
  * For regression , I build a simple loss function, which is similar to the loss function of yolo with small change.
step 6:Train and save
  Finally the models were trained and saved, the weights are avalable in this repo.
