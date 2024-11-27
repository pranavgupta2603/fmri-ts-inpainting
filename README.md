# Inpainting multi-variate timeseries data of Brain fMRI

- There are 424 parcels each with 842 timesteps(imagine a rectangle) in each file.

- In this code, I am taking 41 files and randomly sampling 128x128 data from the entire 424x842.

- I mask 128x20 from the right of the 128x128 which you'll see below in the code

- I train a GAN with a UNet structure that reconstructs the entire 128x128 image, including the masked bit.

- The intuition is that by giving any 128x108 data (128 parcels, each with 108 timesteps), you can forecast 20 more timesteps for each of the 128 parcels

- This is a new method for multivariate timeseries forecasting
