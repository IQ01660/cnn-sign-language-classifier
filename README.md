# Sign Language Classification

#### Please check sign-lang-final.ipynb for more info, as well as for the source code

## Dataset Source

https://www.kaggle.com/datamunge/sign-language-mnist

## Dataset Description
In this project I am using a dataset that contains images (actually their grayscale pixel values); each image represents a certain letter from A to Y in the sign language. The dataset does not contain any data on J or Z letters, as those have motion involved when translated into sign language. Images are 28 by 28 pixels, and there are a total of 34627 of them in the dataset.

If one is interested in learning more about this they can visit the following page where they can translate text into how it would look in the sign language: https://wecapable.com/tools/text-to-sign-language-converter/.

## Motivation
After doing some research on this topic, I did not find a lot of applications that would do the reverse, i.e. translate images of signs into what they mean in English. Therefore, I decided to utilize some image processing techniques along with different classification algorithms to accomplish this task, although only with digits for now.

## Goal
My goal in this project is to compare the accuracies on the test set of the following models: SVM, MLP, and CNN. I expect CNN to perform better than the two other models, as Convolutional Neural Networks have proved to be more efficient in image classification tasks. Another goal is to build some kind of majority-vote ensemble, where the decision of the model with the highest accuracy, will be "vetoed" if the other two models' predictions are the same and differ from that of the best performing model. I decided to go with this ensemble model instead of the usual majority-vote ensemble, due to - as will be seen below - low test accuracy of one of the models.

## Tensorflow
Note that this project uses tensorflow in order to build a CNN model; therefore, tensorflow needs to be installed using pip for example.

## Preparing the Dataset
Here, we take the csv files that contain train and test data for our application. Some basic imports of numpy and matplotlib.pyplot are also done and will be used along the way
