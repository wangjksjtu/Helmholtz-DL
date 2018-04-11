## The Helmholtz Method: *Using Perceptual Compression to Reduce ML Complexity*

![Helmholtz Reinterpretation](https://github.com/wangjksjtu/Helmholtz-DL/blob/master/docs/Reinterpretation.pdf)

### Introduction
This work is based on our [arXiv tech report](https://arxiv.org/abs/). We proposed a fundamental answer to a frequently asked question in multimedia computing and machine learning: Do artifacts from perceptual compression contribute to error in the machine learning process and if so, how much?. You can also check our [project webpage](http://berkeley.edu/helmholtz-dl) for a deeper introduction.


Our approach to the problem is a reinterpretation of the Helmholtz Free Energy formula from physics to explain the relationship between content and noise when using sensors (such as cameras or microphones) to capture multimedia data. Extensive experiments show that, at the right quality level, perceptual compression is actually not harmful but contributes to a significant reduction of complexity of the machine learning process. Our work provides insights into the reasons for the success of deep learning.

In this repository, we release code and data for conducting perceptual compression while maintaining, or sometimes even improving, overall performance. Additionally, compressed models usually results in faster convergent speed. 

### Requirements

* **Tensorflow 1.4.0**
* **Keras 2.1.5**
* Python 2.7
* CUDA 8.0+ (For GPU)
* Python Libraries: numpy pandas, h5py, pillow, imageio, librosa and librosa
* [lame](http://lame.sourceforge.net/) tool (for MP3 compression)

The code has been tested with Python 2.7, Tensorflow 1.4.0, CUDA 8.0 and cuDNN 5.1 on Ubuntu 14.04. But it may work on more machines (directly or through mini-modification), pull-requests or test report are well welcomed.

### Usage
To train a model to classify images in CIFAR-10
  
    cd cifar
    python train.py

Log files and network parameters will be saved to `log` folder in default. 

To see HELP for the training script:

    python train.py -h

### Citation
If you find our work useful in your research, please consider citing:

	@article{helmholtz,
	  title={The Helmholtz Method: Using Perceptual Compression to Reduce Machine Learning Complexity},
	  author={},
	  journal={arXiv preprint arXiv:1804.xxxxx},
	  year={2018}
	}
   
### Acknowledgements
This code is based on the previous works ([All-Conv-Keras](https://github.com/MateLabs/All-Conv-Keras)，[panotti](https://github.com/drscotthawley/panotti)). Many thanks to the authors.

### License
Our code is released under MIT License.
