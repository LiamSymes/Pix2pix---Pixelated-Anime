Pix2Pix model and Pixelation code in Google Colabs.

Instructions for pixelating images:
1: Load Google Colab file (Pix2Pix_Pixelate.ipynb).
2: Edit filepaths in the existing code to match your system/directory. 
3: Edit the image resize values to your preferred image size.
4: Edit the pixelation value to modify how pixelated the images will become.
5: Run all the code and find images in your GDrive folder or the directory you changed it to be saved to.


Using the AnimePix2pix python code via Google Colabs: 
1: Load Google Colab file (AnimePix2Pix.ipynb).
2: Change directories where needed so the code can access the required folders. 
3: Change the n_epoch and n_epoch_decay to a lower amount to begin with (e.g. 10, 10) to ensure everything is working correctly.
4: After this, the default or recommended values are 100, 100. 
5. After the model is finished training, you can save the 'latest_net_G.pth' and 'latest_net_D.pth' files if you wish to save the latest trained version. 
6: To continue training, simply uncomment '--continue_train' and '--epoch_count' and then change the epoch_count to the epoch you wish to start from to continue training. Then up the amount of n_epochs and n_epochs_decay.
7: If you wish to save the entirety of results, use the last code block but ensure you update the destination_dir.




Tips for setting up Pix2Pix with your own images/datasets:

REFER TO OFFICIAL DOCUMENTATION FIRST: https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix/blob/master/docs/datasets.md#pix2pix-datasets

Tips:
-Obtain the two sets of images (pairs) you want to train Pix2Pix with (e.g. pixelated images, full resolution images)
-Put the images in two seperate folders named A and B, then create a 'test' and 'train' subfolder inside both. 
-Ensure that paired images have the exact same name, but are in each corresponding folder (e.g. A/test and B/test)
-Prioritise the images you want the model to transfer style in the order A to B. E.g. (Pixelated = A, full resolution = B)
-Have all paired images you want to train the model with in the 'train' subfolder in each A and B.
-Have all the paired images you want to test after the model has been trained in the 'test' subfolder in each A and B. 



