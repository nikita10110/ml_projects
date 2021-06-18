### Face Recognition Using LBPH Recognizer

For face detection, I used the haarcascade frontal face model. The model is a xml file having data stored in it. Opencv provides the CascadeClassifier that imports models from github. Further I have to give input images to the haar cascade model to detect the faces from the images, then these detected faces have been used in face recognition.

Once our detection process is done, now I have applied the LBPH (Local binary pattern histogram) recognizer on images. Using LBPH images are converted into Local binary patterns, further these pattern images are used to create the histograms, then i train our model. Further when i input an image, it’s Histogram is compared with trained images histograms. A threshold value is set if the distance between the two histograms is greater than the threshold then the best match is the output. In this model I'm able to get an accuracy of 71% on train and 95% on validation.

In the repository, the files such as face_train.ipynb contains the code for the training of the model, then i have saved the trained model as face_model.yml which is further used in face_recogntion, also there are labels.npy and features.npy files which i got from face_train.ipynb and it contain information of trained labels and features. Face_recogniton.ipynb file contains the code for recognition of the image, in this I also try to find out the label of the unseen image.

