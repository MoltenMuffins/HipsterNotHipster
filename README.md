# HipsterNotHipster
The entirety of the project can be found in the jupyter notebook in this repo. You may use the following link to <https://tinyurl.com/hipster100> to quickly refer to this repo.

### Problem Statement
This project attempts to create a one class image classifier (unary classification problem) via transfer learning on top of VGG-Face as a final project submission for the December iteration of the Deep Learning Jump Start Workshop conducted by Red Dragon AI.

Possible issues:
*   The prevalence of beards in contemporary hipster culture leads to many of the 'hipster' positive examples showing beards. My attempt to mitigate this involves including sufficient examples of non-hipsters with beards (eg. muslim men). 
*   Confirmation bias is also present as the training examples are created by me and hence the classifier would be directly affect by my own perceptions of what constitutes a hipster.
*  I did not have a rubric for classifying hipsters and allocated labels to images solely based on my own gut feeling which may result in incorrect labeling.


My initial hypothesis would be that the imagenet model with weights would perform favorably given that accessories are a key component of being a hipster. An earlier version of this project involved using the standard VGG-16 model with imagenet weights, and produced results around *~0.50*.

The VGGface implementation took longer (mainly due to time spent trying to understand VGGface topology and finding a source for VGGface weights as the relevant github repo has outdated code that can't be run) but produces slightly better results of *~0.67*. 

The current build seems to work well and would likely improve in performance if given a larger dataset. In the meantime, I will work on methods to shorten the database building process before coming back to the project.
