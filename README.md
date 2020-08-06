## Inputs

-  **dataroot** - the path to the root of the dataset folder. We will talk more about the dataset in the next section
-  **workers** - the number of worker threads for loading the data with the DataLoader
-  **batch_size** - the batch size used in training. The DCGAN paper uses a batch size of 128
-  **image_size** - the spatial size of the images used for training. This implementation defaults to 64x64. If another size is desired,
the structures of D and G must be changed. See `here <https://github.com/pytorch/examples/issues/70>`__ for more details
-  **nc** - number of color channels in the input images. For color images this is 3
-  **nz** - length of latent vector
-  **ngf** - relates to the depth of feature maps carried through the generator
-  **ndf** - sets the depth of feature maps propagated through the discriminator
-  **num_epochs** - number of training epochs to run. Training for longer will probably lead to better results but will also take 
much longer
-  **lr** - learning rate for training. As described in the DCGAN paper, this number should be 0.0002
-  **beta1** - beta1 hyperparameter for Adam optimizers. As described in paper, this number should be 0.5
-  **ngpu** - number of GPUs available. If this is 0, code will run in CPU mode. If this number is greater than 0 it will run on that 
number of GPUs
 
 ## Original code is from https://github.com/Natsu6767/DCGAN-PyTorch