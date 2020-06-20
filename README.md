# Predicting Bike Sharing Patterns

In this project I've used a dataset having the number of riders for each hour of each day from January 1 2011 to December 31 2012, and used it to train a neural network which can predict the bike sharing patterns.

    *This is the first project of Udacity's Deep Learning Nanodegree Program*
    

## Prerequisites

The Code is written in Python 3.6.5 . If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip. 

To install pip run in the command Line
```
python -m ensurepip -- default-pip
``` 
to upgrade it 
```
python -m pip install -- upgrade pip setuptools wheel
```
to upgrade Python
```
pip install python -- upgrade
```
Additional Packages that are required are: [Numpy](http://www.numpy.org/), [Pandas](https://pandas.pydata.org/), [MatplotLib](https://matplotlib.org/), [Pytorch](https://pytorch.org/), PIL and json.\
You can donwload them using [pip](https://pypi.org/project/pip/)
```
pip install numpy pandas matplotlib pil
```
or [conda](https://anaconda.org/anaconda/python)
```
conda install numpy pandas matplotlib pil
```
In order to intall Pytorch head over to the Pytorch site select your specs and follow the instructions given.

## Viewing the Jyputer Notebook

In order to better view and work on the jupyter Notebook I encourage you to use [nbviewer](https://nbviewer.jupyter.org/) . You can simply copy and paste the link to this website and you will be able to edit it without any problem. Alternatively you can clone the repository using 
```
git clone https://github.com/rishabhchhillar/Predicting-Bike-Sharing-Patterns/
```
then in the command Line type, after you have downloaded jupyter notebook type
```
jupyter notebook
```
locate the notebook and run it.

## Hyperparameters

The strategy here is to find hyperparameters such that the error on the training set is low, but we're not overfitting to the data. If we train the network too long or have too many hidden nodes, it can become overly specific to the training set and will fail to generalize to the validation set. That is, the loss on the validation set will start increasing as the training set loss drops.

**Number of iterations**
This is the number of batches of samples from the training data we'll use to train the network. The more iterations we use, the better the model will fit the data. However, this process can have sharply diminishing returns and can waste computational resources if we use too many iterations. We want to find a number here where the network has a low training loss, and the validation loss is at a minimum. The ideal number of iterations would be a level that stops shortly after the validation loss is no longer decreasing.

**Learning rate**
This scales the size of weight updates. If this is too big, the weights tend to explode and the network fails to fit the data. Normally a good choice to start at is 0.1. If the network has problems fitting the data, we should try reducing the learning rate. Note that the lower the learning rate, the smaller the steps are in the weight updates and the longer it takes for the neural network to converge.

**Number of hidden nodes**
In a model where all the weights are optimized, the more hidden nodes we have, the more accurate the predictions of the model will be. (A fully optimized model could have weights of zero, after all.) However, the more hidden nodes we have, the harder it will be to optimize the weights of the model, and the more likely it will be that suboptimal weights will lead to overfitting. With overfitting, the model will memorize the training data instead of learning the true pattern, and won't generalize well to unseen data.

## Authors

* **Rishabh Chhillar**
* **Udacity**

## License

This project is licensed under the MIT License - see the (LICENSE.md) file.
