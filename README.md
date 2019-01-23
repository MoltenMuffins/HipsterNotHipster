# HipsterNotHipster
The entirety of the project can be found in the jupyter notebook in this repo. You may use the following link to <https://tinyurl.com/hipster100> to quickly refer to this repo.

### Problem Statement
This project attempts to create one class image classifier via transfer learning on top of VGG-Face as a final project submission for the December iteration of the Deep Learning Jump Start Workshop conducted by Red Dragon AI. The dataset used is self generated using a bulk image downloading tool (fatkun) while the VGG-Face weights for tensorflow are kindly provided by Sefik at https://sefiks.com/2018/08/06/deep-face-recognition-with-keras/. While the choice of topic "Hipster vs Not Hipster" seems rather whimsical, my intention with the project was to try to captilize on the ability of neural networks to generate features independently and see if it can replicate subjective human categorization.

### Possible Issues and Actions Taken
*   The prevalence of beards in contemporary hipster culture leads to many of the 'hipster' positive examples showing beards. My attempt to mitigate this involves including sufficient examples of non-hipsters with beards (eg. muslim men). 
*   Confirmation bias is also present as the training examples are created by me and hence the classifier would be directly affect by my own perceptions of what constitutes a hipster. The accuracy of the model in use thus varies from person to person.
*  I did not have a rubric for classifying hipsters and allocated labels to images solely based on my own gut feeling which could cause inconsistency in the labeling.
* Due to my fixation on beards, I neglected to include examples of the female gender in this run of the project. A third iteration of this project would include the female gender, or better yet include a spectrum of genders.

### Summary of Results
My initial hypothesis would be that the imagenet model with weights would perform favorably as I felt the clothes and accessories on the person would be a key component of identifying a hipster. An earlier iteration of this project involved using the standard VGG-16 model with imagenet weights, and produced results around *~0.50*.

My second approach is contained in this notebook. It uses the VGGface model which essentially is a VGG model trained on celebrity faces. The process of implementing this model took longer (mainly due to time spent trying to understand the VGGface topology and finding a source for VGGface weights as the relevant github repo has outdated code that can't be run) but produces slightly better results of *~0.67*. 

This current build seems to work well and suggests that whether one is a hipster has more to do with one's facial features and hair rather than their dressing. I expect that this model could exhibit improvements in performance if given a larger dataset. For a third iteration, a larger dataset would definitely be required. In order to increase the efficiency of labeling, I might look into builing an application or tool modeled after tinder where one could simply swipe left or right to label images. This would greatly speed up the dataset creation process for this project and any other future endeavors.

