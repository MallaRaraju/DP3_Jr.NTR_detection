# DP3_Jr.NTR_detection
* step 1: data collection 
  * I have collected the images of actor Jr.NTR one of the main leads of the recent blockbuster RRR.
* step 2: Labeled them in Roboflow
  * The collected data was labeled in Roboflow with a total of 93 images split into training, testing, and validation sets with 59, 9, and 25 respectively.
* step 3: Loading and Augmentation
  * The labeled data was then loaded into google colab by using the API key in the COCO format.
  * Since this dataset is very small, I augmented it for which I build an augmentation pipeline using albumentation module and saved it in a folder in labelme format.
* step 4: Data pipelining
  * The augmented images and labels are saved and then passed into a TensorFlow data pipeline separately with 8 images and labels in a batch without shuffling  and then         zipped together and shuffled.
* step 6: Build Model
  * I built two models with different heads and VGG16 as the backbone. The model architectures are provided in the same repo as .png images.
* step 5: Define the loss function
  * For training the data, I used Adam optimizer and for classification, BinaryCrossEntropy was used.
  * For regression, I build a simple loss function, which is similar to the loss function of YOLO with a small change.
* step 6:Train and save
  * Finally the models were trained and saved.
