# SRCNN with sub-pixel conv VS plain bicubic interpolation on image super resolution

Respectively implement SRCNN  integrated with sub-pixel convolutions and plain bicubic interpolation on image dataset, analyze their effects and characteristics.


The image datasets we adopted are LR_bicubic/X4 dataset (set as features) and DIV2K_train_HR dataset from DIVERSE 2K resolution high quality images (set as targets).
To compute conveniently, resize each LR image into [h, w] as [339,  510], HR image into [1356, 2040] So HR image size is 4 times of LR image size


We set two comparison experiments for the image super-resolution:

  1th: Use SRCNN to super-resolution with sub-pixel convolution to upscale X4 at the 3rd layer of SRCNN, compute PSNR of <predictions, targets> in test set, 
  
  2th: Use plain bicubic directly onto test set, compute PSNR of  <bicubiced features, targets>

  then we compare PSNR plottings and one image processed by two means 



For SRCNN, referenced Learning a deep convolutional network for image super-resolution. 2014, for sub-pixel convolutions, referenced Real-time single image and video super-resolution using an efficient sub-pixel convolutional neural network. 2016


After train and test, we find the best epoch that has the best average PSNR value, save the model weights into best_model.weight,  load the model and upscale one image and save it into result/ folder.




This project is completed by @tahamousavi_92 and me.


