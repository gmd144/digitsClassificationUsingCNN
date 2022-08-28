# Digit Classification using MNIST dataset

The MNIST database (Modified National Institute of Standards and Technology database) <a href="#1">[1]</a> is a large database of handwritten digits that is commonly used for training various image processing systems. 

The MNIST database contains 60,000 training images and 10,000 testing images.<a href="#3">[3]</a> Half of the training set and half of the test set were taken from NIST's training dataset, while the other half of the training set and the other half of the test set were taken from NIST's testing dataset.<a href="#4">[4]</a> The original creators of the database keep a list of some of the methods tested on it.<a href="#2">[2]</a> In their original paper, they use a support-vector machine to get an error rate of 0.8%.<a href="#5">[5]</a>

<strong>References</strong>

<ol>
<a href="http://yann.lecun.com/exdb/mnist/" target="_blank"><li id="1">"THE MNIST DATABASE of handwritten digits". Yann LeCun, Courant Institute, NYU Corinna Cortes, Google Labs, New York Christopher J.C. Burges, Microsoft Research, Redmond.</li></a>
<a href="http://yann.lecun.com/exdb/mnist/" target="_blank"><li id="2">LeCun, Yann; Cortez, Corinna; Burges, Christopher C.J. "The MNIST Handwritten Digit Database". Yann LeCun's Website yann.lecun.com. Retrieved 30 April 2020</li></a>
<a href="https://doi.org/10.1016%2Fj.imavis.2004.03.008" target="_blank"><li id="3">Kussul, Ernst; Baidyk, Tatiana (2004). "Improved method of handwritten digit recognition tested on MNIST database". Image and Vision Computing. 22 (12): 971–981</li></a>
<a href="http://mleg.cse.sc.edu/edu/csce822/uploads/Main.ReadingList/KNN_fastbyClustering.pdf" target="_blank"><li>Zhang, Bin; Srihari, Sargur N. (2004). "Fast k-Nearest Neighbor Classification Using Cluster-Based Trees" (PDF). IEEE Transactions on Pattern Analysis and Machine Intelligence. 26 (4): 525–528</li></a>
<a href="http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf" target="_blank"><li>LeCun, Yann; Léon Bottou; Yoshua Bengio; Patrick Haffner (1998). "Gradient-Based Learning Applied to Document Recognition" (PDF). Proceedings of the IEEE. 86 (11): 2278–2324. doi:10.1109/5.726791. Retrieved 18 August 2013</li></a>
</ol>


# Project Structure
## Classification using the Feed Forward Neural Network

I have used three <a href="https://keras.io/api/layers/core_layers/dense/" target="\_blank">dense</a> layers to build the model. Since the images are 28x28 grayscale, so I have reshaped them to single dimension and normalized them so the pixel values are between 0 and 1. I used the Adam optimizer and the categorical_crossentropy as the loss function and the accuracy to evaluate my model. After training for 10 epochs I was able to get 98% accuracy on training set and 96.8% accuracy on test set.

## Classification using the CNN

I used two [Conv2D](https://keras.io/api/layers/convolution_layers/convolution2d/) with maxpooling layer afterwards. Since I am using the Conv2D layers so no need to reshape the images, but still their values need to be normalized between 0 and 1. By using the same optimizer, loss function and evaluation metric. After training the model for 15 epochs I was able to achieve 98.9% accuracy on train set and 99.6% accuracy on test set.

I also crafted a very small dataset to test the model and that data set can be accessed <a href="https://drive.google.com/drive/folders/1-EzOmdXmAiJF5JMZIVX3A_n_dTI-fdud?usp=sharing" target="_blank">here</a>

Some of the example images are shown below

![example image of handwritten 1](https://drive.google.com/file/d/1-NdWWHU2DRuNMBm9ZHNMqeh7TcMdhBT9/view?usp=sharing)

<img src="https://drive.google.com/file/d/1-NdWWHU2DRuNMBm9ZHNMqeh7TcMdhBT9/view?usp=sharing" alt="example image of handwritten 1">

![example image of handwritten 2](https://drive.google.com/file/d/1-riq9jRMD15PILTJK9BtL8A9qlnz1Ks3/view?usp=sharing)

<img src="https://drive.google.com/file/d/1-riq9jRMD15PILTJK9BtL8A9qlnz1Ks3/view?usp=sharing" alt="example image of handwritten 2">

![example image of handwritten 5](https://drive.google.com/file/d/1-RNxCfaJftwKnOQ-PzJOz9Grdp_UWINY/view?usp=sharing)

<img src="https://drive.google.com/file/d/1-RNxCfaJftwKnOQ-PzJOz9Grdp_UWINY/view?usp=sharing" alt="example image of handwritten 5">

# LICENSE

MIT
