# Self-Supervised Image Denoising For Real Raw Images with Double Pathway BSNs
The task of camera raw image denoising has become a crucial part of the application of object recognition and segmentation (i.e. security systems). Current image restoration techniques primarily involve the use of the self-supervised N2V algorithm due to its convenience. This project uses a summation over four irregularly shaped masks in the BSN that is fed into two separate pathways, which outputs further learn from each other via L2 loss. In particular, we proposed two novel masks to generate two sets of noisy input images to train two separate UNets. The noisy outputs then learned the masked pixels from each other, resulting in high PSNR and SSIM.

# U-Net
Access the model through the arch_unet.py file.

# Raw Data
Generate sample data using dataset_tool_raw.py on the raw SIDD dataset, which can be downloaded at https://www.eecs.yorku.ca/~kamel/sidd/.

# Training
Train your model through the train_sidd_b2u_n2n_ema_hav.py or train_sidd_b2u_n2n_ema_sav.py files with different mask shapes. Noises are Gaussian by default.

# Testing
Test your model through the test_sidd.py file.
