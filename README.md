# Installing GPU for Python on Windows 10

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

## Step 0.1: Install Anaconda:

- As we know, Anaconda has very good abilities to create and manage the environments and most coding platforms like Spyder, Jupyter and ... Also it has very fast terminals on each environment for installing modules with Conda keyword. It must therefore be installed!

- You can download it using this link:

https://www.anaconda.com/products/individual

## Step 0.2: Check your graphics card! 

- Your computer's graphics processor must also support Tensorflow, to do this, find your graphics card model in `` CUDA-Enabled GeForce and TITAN Products``. If the point mentioned on your graphics card is more than 3.5, it means it supports TF.

## Step 0.3: Update your graphics card.
It is necessary to go to your laptop company's website and update your graphics card.


## Step 1: Install Microsoft Visual Studio version 2019:

- As a first step, download the version of the Microsoft Visual Studio community from this link:

https://visualstudio.microsoft.com/vs/community/

- After downloading the file, double click on it and the window below will appear, there is no need to select anything, so just click the install button:

![](https://github.com/Mahdidrm/GPU/blob/main/2.png?raw=true)

- If you already have Microsoft Visual Studio, skip this step.

## Step 2: Install the CUDA Toolkit

- To download the latest version of Cuda, click here:

https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64&target_version=10&target_type=exelocal

- But it is recommended to install Cuda version 10.2 because we have tested it and it works great.

## Very important points!

1- When you want to install Cuda, go to the custom part and uncheck all the options except CUDA

2- If you install CUDA 10.2 and have trouble in detecting your GPU, you can downgrade CUDA to version 9. If you do this, don't forget the version 9 paths to install!

## Step 3: Install CUDNN version 7.2 or above:

Depending on your CUDA version, download the CUDNN from the list on the link below:

https://developer.nvidia.com/rdp/cudnn-archive

- You must have / create an account on the Nvidia website to have access to the download.

- After downloading cudnn, extract the zip file and open the folder to see 3 folders with the names lib, include and bin.

- Go to the CUDA folder on your computer which looks like:

```                                  C: / Program Files / NVIDIA GPU Computing Toolkit / CUDA / v 10.1

```
- And now paste the contents of each CUDNN folder separately into the corresponding folder (with the same name) in the CUDA folder. Also accept all comments and notifications.

```                          Bin in CUDNN into Bin in CUDA and include of CUDNN in include in CUDA and lib/x64 of CUDNN into lib/x64 of CUDA                            ```


## Step 4: Give your CUDA addresses:

- Now press the start key on your keyboard and search for ```edit the system environment variables``` in search box of start menu then hit enter. 

- As shown in the windows below, select go to ```enviroments variables``` then select the ```edit``` item.

![](https://github.com/Mahdidrm/GPU/blob/main/3.png)

- In this window, click on ```new``` and add the address of two CUDA ```bin``` and ```libvvn``` folders installed on your computer such as:

```                                C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v 10.1/bin                                                      ```

```                                C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v 10.1/ libnvvp                                                  ```
                             

![](https://github.com/Mahdidrm/GPU/blob/main/4.png?raw=true)

- And now, click Ok Ok OK... 

## Step 5: Create an environment for the GPU in Anaconda

- Open the Anaconda prompt and type this command:

```                                      conda create -n tensorflow_gpuenv python=3.6 tensorflow-gpu                                                               ```

```                                      conda activate tensorflow_gpuenv                                                                                         ```
                                  
- Now wait a few minutes to anaconda download and install the necessary packages. Then you will see your environment and the necessary packages.

- Very important: you have to install ```keras-gpu``` on! the conda code is:

```                                     conda install -c anaconda keras-gpu```

![](https://github.com/Mahdidrm/GPU/blob/main/5.png?raw=true)

- Also you can install Spyder and Jupyter with these codes:

```                                     conda install -c anaconda spyder                                                                                    ```
```                                     conda install -c anaconda jupyter                                                                                   ```
                


At the end, you can run Spyder or Jupyter and run your code, but don't forget to add this line:
```                                     import tensorflow as tf                                                                                             ```



Enjoy of your ## GPU

![](https://github.com/Mahdidrm/GPU/blob/main/7.png?raw=true)




Reference
-

Special thanks to Amir Hossein Mesbah:

https://virgool.io/@amir_msbh/%D8%A7%D8%AC%D8%B1%D8%A7%DB%8C-jupyter-notebook-%D8%A8%D8%B1-%D8%B1%D9%88%DB%8C-gpu-tkweik8tvgid

