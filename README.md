### Transfer Learning: from Cats & Dogs to American Sign Language

Learning derived from ImageNet dogs n cats on MobileNet transfered to American Sign Language classification.

Please click the video to hear sound or follow along with the transcript that's set just below the video.

![demo](https://user-images.githubusercontent.com/38410965/111880073-a2327600-897f-11eb-8728-7b9eba6a7b14.mp4)

#

> Hi.  This is Steve Depp.  Thank you for watching my demo video on transfer learning.  This week we’re using the ImageNet data set and the MobileNet architecture as represented in the Jupyter notebook from chapter 3 of the textbook. 

### Steve Depp - MSDS 462 - DV9    
### Transfer Learning    
- ImageNet dataset and MobileNet network architecture    
- Practical Deep Learning for Cloud, Mobile, and Edge, Chapter 3    
- keras_custom_classifier_with_transfer_learning.ipynb     

<img width="1091" alt="Building a Custom Classifier in Keras with Transfer Learning" src="https://user-images.githubusercontent.com/38410965/115973704-25b62880-a525-11eb-9c3a-56c770b0d55b.png">

#

> So, I’ve loaded my Google Drive with dog and cat folders and inside that with train and validate folders.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**Task 1: doggie or kitty**    
Google drive loaded     
- with dog and cat folders     
- inside train and validate folders    

<img width="1091" alt="dog - Google Drive" src="https://user-images.githubusercontent.com/38410965/115973733-51d1a980-a525-11eb-9328-e9aff39f5249.png">

#

> Colab retrieves the data.      

### ImageNet dataset and MobileNet network architecture - transfer learning

**Dog v Cat classification**    
Colab retrieves data    
500 images each for training and validating    

<img width="1091" alt="• Set up the configuration" src="https://user-images.githubusercontent.com/38410965/115973757-7594ef80-a525-11eb-83ca-33d6dacf606e.png">

#

> Keras augments the train and validation data.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**Dog v Cat classification**    
Keras augments the train and validation data    

<img width="1095" alt="oad and augment the data" src="https://user-images.githubusercontent.com/38410965/115973772-90fffa80-a525-11eb-8dfd-4e4d9036a0ed.png">

#

> Keras trains and validates the model this time as a multi class classification even though there’s only two categories.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**Dog v Cat classification**    
Keras trains and validates the model as multi-class classification     

<img width="1095" alt="Train and test" src="https://user-images.githubusercontent.com/38410965/115973790-ae34c900-a525-11eb-8788-e9d179797a1d.png">

#

> The test image comes out at 99.7% dog which is correct.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**Dog v Cat classification**    
test image 99.7% dog which is correct    

<img width="926" alt="Model Prediction" src="https://user-images.githubusercontent.com/38410965/115973798-c4db2000-a525-11eb-8479-f493f3198623.png">

#

> Alright. So, for task two, I’ve brought in my dataset from American Sign Language which has 200 images each, 26 letters, and loaded those into Google Drive.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**Task 2: American Sign Language**    
- 200 images each     
- 26 letters —> Google Drive     

<img width="915" alt="val Google Drive" src="https://user-images.githubusercontent.com/38410965/115973815-dc1a0d80-a525-11eb-9b8f-a655e9d8e5e0.png">

#

> So, the letter A.  Just to remind you that the hand can be close or far away; it can be in the shadows; it can be in the light.  And you can see that it brings out edges in the shadow that may not be representative of, you know, fingers, position, etc.  So, it can confuse a classification.    

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    

**A**    
- shadows are edges    
- ceiling is an edge    
- loads of and not much light    
- disk space10-15 kb     

<img width="791" alt="Pasted Graphic 21" src="https://user-images.githubusercontent.com/38410965/115973838-09ff5200-a526-11eb-99eb-2b3890316bc7.png">

#

> Anyway. So, Colab loads the data and augments it.  

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    
Colab    
- loads    
- augments    

<img width="915" alt="dog Google Drive" src="https://user-images.githubusercontent.com/38410965/115973853-24393000-a526-11eb-95de-ea094f87b133.png">

#

> After ten epochs, you 20% accuracy which is better than 1 in 26. So, actually I’m surprised how good it was after, you know, that many epochs.  

*[this [notebook](https://github.com/stevedepp/TransferLearningCatsDogs2ASL/blob/main/1_keras_custom_classifier_with_transfer_learning_10_epochs.ipynb) is the one shown that goes for 10 epochs]*

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    
10 epochs -- > 20 ish % accuracy > 1 in 26    

<img width="1129" alt="val - Google Drive" src="https://user-images.githubusercontent.com/38410965/115973864-3dda7780-a526-11eb-9aed-7a59c474272a.png">

#

> So, if you test it though: A is not doing too terribly well.  It gets 3.1%.  B gets 7.2%.  M gets 9.5%.  And V is the winner at 11.6%.  So, it thinks it’s a V.  Not really very close.  I mean, you could say that, yeah, it’s got two of the digits correct *[pinky and ring finger]*, but that’s about it.     

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    
model thinks     
￼
￼<img width="915" alt="0 03139458 0 0719717 0 02074774 0 0220159 0 04696643 0 01447384" src="https://user-images.githubusercontent.com/38410965/115973889-61052700-a526-11eb-9c15-ebc03d72b157.png">

<img width="781" alt="A = 0 0314" src="https://user-images.githubusercontent.com/38410965/115973893-66fb0800-a526-11eb-8888-188d1448566a.png">

#

> So, run it for longer.  Twenty epochs, it’s at 36% which is one in three or better than one in three.  

[*this [notebook](https://github.com/stevedepp/TransferLearningCatsDogs2ASL/blob/main/1_keras_custom_classifier_with_transfer_learning_100_epochs.ipynb) is the one shown that goes for 100 epochs*]

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    
20 epochs -- > 36 ish % accuracy > 1 in 3    

<img width="1003" alt="val - Google Drive" src="https://user-images.githubusercontent.com/38410965/115973907-78dcab00-a526-11eb-92e1-e95bafe5ba21.png">

#

> After a hundred epochs, we’re at 77% accuracy which is actually where my model got it to last year, and then at the beginning of this term when I showed you [this](FMNIST).  The validation accuracy is 100% which means it’s basically memorizing the validation data.  There are 180 training images and 20 of the validation images. So, it’s not surprising it memorizes the validation. 

### ImageNet dataset and MobileNet network architecture - transfer learning

**ASL classification**    
100 epochs -- > 77 % accuracy     
(validation accuracy = 100% )     

<img width="1003" alt="val - Google Drive" src="https://user-images.githubusercontent.com/38410965/115973916-8e51d500-a526-11eb-850b-82d5a2369e1f.png">

#    

> When you run it for the letter A, the same image, it gets 69.5% which is pretty good.       
Thank you for watching.      

### ImageNet dataset and MobileNet network architecture - transfer learning    

**ASL classification**    
A = 69.5%    

<img width="701" alt="val - Google Drive" src="https://user-images.githubusercontent.com/38410965/115973925-a0cc0e80-a526-11eb-87bf-3fc6485cb1cd.png">
