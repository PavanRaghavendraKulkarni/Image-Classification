VGG 19 architecture 
A fixed size of (224 * 224) RGB image was given as input to this network which means that the matrix was of shape (224,224,3).
The only preprocessing that was done is that they subtracted the mean RGB value from each pixel, computed over the whole training set.
Used kernels of (3 * 3) size with a stride size of 1 pixel, this enabled them to cover the whole notion of the image.
spatial padding was used to preserve the spatial resolution of the image.
max pooling was performed over a 2 * 2 pixel windows with sride 2.
this was followed by Rectified linear unit(ReLu) to introduce non-linearity to make the model classify better and to improve computational time as the previous models used tanh or sigmoid functions this proved much better than those.
implemented three fully connected layers from which first two were of size 4096 and after that a layer with 1000 channels for 1000-way ILSVRC classification and the final layer is a softmax function.
