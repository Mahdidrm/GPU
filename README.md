# Installing GPUs for Python on Windows 10

Are you looking for a quick, convenient, and easy way to use #GPU on your Python often?
Here is a complete and simple explanatory way to do it!


![](https://github.com/Mahdidrm/GPU/blob/main/1.jpeg?raw=true)


Introduction
-
As a deep learning researcher, one of the difficult steps of our job is to train models, for example in my projects on emotion recognition, to train a CNN model using Fer2013 dataset which has more than 37,000 images via a CUP Core i5, I should forget a whole day of my time (training and testing) it's because we decided to use another solution, GPU!

In the following steps which were tested on a Dell laptop with the configuration below, the result is exactly what we wanted. training the model with the same dataset only took 40 minutes!
```
GPU: Nvidia Geforce RTX 2060 with 6GB memory 
CPU: Core i7  with 12MB cache 
RAM: 16GB DDR4 
OS: Windows10

```

Steps
-

- Step 0.1: Install Anaconda:

As we know, Anaconda has very good abilities to create and manage the environments and most coding platforms like Spyder, Jupyter and ... Also it has very fast terminals on each environment for installing modules with Conda keyword. It must therefore be installed!

You can download it using this link:

https://www.anaconda.com/products/individual

- Step 0.2: Check your graphics card! 

Your computer's graphics processor must also support Tensorflow, to do this, find your graphics card model in `` CUDA-Enabled GeForce and TITAN Products``. If the point mentioned on your graphics card is more than 3.5, it means it supports TF.

- Step 0.3: Update your graphics card.
It is necessary to go to your laptop company's website and update your graphics card.


- Step 1: Install Microsoft Visual Studio version 2019:

As a first step, download the version of the Microsoft Visual Studio community from this link:
https://visualstudio.microsoft.com/vs/community/

only after auto-extracting donloaded file, as it is shown in the window below, don't select anything and just click the install button.


![](https://github.com/Mahdidrm/GPU/blob/main/2.png?raw=true)





- 
