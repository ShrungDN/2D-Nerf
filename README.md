# 2D-Nerf

This project is an attempt to perform super resolution of images by using concept of NeRF and Positional Encoding. In order to do this, a neural network is overfit on an image, i.e. the neural network learns the image representation in its weights. The following GIFs show how well a neural network can learn to regenerate an image. 

- The left most image is the ground truth image. 

- The middle image is the regenerated image without using positional encoding. 

- The right image is the regenerated image using positional encoding. 

<p align="center">
32 x 32 x 3 image results:
</p>

<p align="center">
![cat_32x32_PE10_epoch5000](https://github.com/ShrungDN/2D-Nerf/assets/87622226/1289bd47-d651-434c-b9fe-e01924089e42)
</p>

<p align="center">
64 x 64 x 3 image results:
</p>

<p align="center">
![cat_64x64_PE10](https://github.com/ShrungDN/2D-Nerf/assets/87622226/8e975e26-3428-4719-9be9-b166a627b893)
</p>

- After a neural network learns the representation of the image, the sub-pixel values can be queried from it, the results obtained are below:


<p align="center">
32 x 32 x 3 image results:
</p>

<p align="center">
![cat_32x32_PE10SR2_epoch5000](https://github.com/ShrungDN/2D-Nerf/assets/87622226/2cd5e956-aa7b-4d81-9c88-826f378063e4)
</p>

<p align="center">
64 x 64 x 3 image results:
</p>

<p align="center">
![cat_64x64_PE10SR2_epoch5000](https://github.com/ShrungDN/2D-Nerf/assets/87622226/786b6fb9-2838-4433-870d-5c18332f6637)
</p>

- The regenerated image is very noisy. This is due to the fact that high frequency sine and cosine functions are used to overfit the image - this causes the change in values in sub-pixel locations to change drastically instead of smoothly, which results in the noise obtained in the new image.
