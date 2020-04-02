# COVID-19GAN
COVID-19 Generative Adversarial Network 

![Teaser image](./grid5.png)

COVID-19GAN is a StyleGAN2 generative advasarial network trained on the 'COVID-19 image data collection' Cohen et al. (2020). The goal of COVID-19GAN is to generate photorealistic images chest x-rays of COVID-19 patients from a modified dataset of the 'COVID-19 image data collection' images. 

# Requirements

The following requirements are derived from StyleGAN2 requirements. For more information visit: https://github.com/NVlabs/stylegan2. 

Both Linux and Windows are supported.
Linux is recommended for performance and compatibility reasons.
64-bit Python 3.6 installation. 
Anaconda3 with numpy 1.14.3 or newer.
TensorFlow 1.14 or 1.15 with GPU support. 
The code does not support TensorFlow 2.0.
On Windows, you need to use TensorFlow 1.14 — TensorFlow 1.15 will not work.
One or more high-end NVIDIA GPUs, NVIDIA drivers, CUDA 10.0 toolkit and cuDNN 7.5. 
To reproduce the results reported in the paper StyleGAN2, you need an NVIDIA GPU with at least 16 GB of DRAM.
Docker users: use the provided StyleGAN2 Dockerfile to build an image with the required library dependencies.

# Dataset 

'COVID-19 image data collection' from Cohen et al. (2020) have been cleaned for compatibility with StyleGAN2. All images have been converted to greyscale, cropped to chest and rescaled to 256x256, 512x512, 1024x1024 and 2048x2048. The 1024x1024 dataset has been segmented into 16x256x256, titled alpha to xi. The average 1024x1024 COVID-19 chest x-ray reveals that segments epsilon, varepsilon, theta and vartheta offer the most promise for applying StyleGan2 to simulate artificial COVID-19 chest x-rays. Subsequently these 4 datasets have been refined though manual filtering.

# Colab
The following notebook COVID-19GAN.ipynb run on Colab provides access to the COVID-19GAN. You may need to modify some paths for it to work. 


# Contact
George Cann, Department of Space and Climate Physics (Mullard Space Science Laboratory), University College London.
Email: george.cann.15@ucl.ac.uk. 

# Citation
```
1. George Cann
COVID-19GAN, arXiv:TBC, 2020
https://github.com/ghcann/COVID-19GAN
```

```
@article{cann_covid-19gan,
  title={COVID-19GAN},
  author={George Cann},
  journal={arXiv},
  url={https://github.com/ghcann/COVID-19GAN},
  year={2020}
}
```

```
2. Joseph Paul Cohen and Paul Morrison and Lan Dao
COVID-19 image data collection, arXiv:2003.11597, 2020
https://github.com/ieee8023/covid-chestxray-dataset
```
```
@article{cohen2020covid,
  title={COVID-19 image data collection},
  author={Joseph Paul Cohen and Paul Morrison and Lan Dao},
  journal={arXiv 2003.11597},
  url={https://github.com/ieee8023/covid-chestxray-dataset},
  year={2020}
}
```

```
3. Tero Karras, Samuli Laine, Miika Aittala, Janne Hellsten, Jaakko Lehtinen, Timo Aila
Analyzing and Improving the Image Quality of StyleGAN
https://github.com/NVlabs/stylegan2
```

```
@article{Karras2019stylegan2,
  title   = {Analyzing and Improving the Image Quality of {StyleGAN}},
  author  = {Tero Karras and Samuli Laine and Miika Aittala and Janne Hellsten and Jaakko Lehtinen and Timo Aila},
  journal = {CoRR},
  volume  = {abs/1912.04958},
  year    = {2019},
}
```

# Acknowledgements

The author would like to thank NVlabs, Tero Karras, Samuli Laine, Miika Aittala, Janne Hellsten, Jaakko Lehtinen, Timo Aila and Joseph Paul Cohen and Paul Morrison and Lan Dao. 
