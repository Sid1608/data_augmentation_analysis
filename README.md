## Data Augmentation Techniques Used
### Zooming:
- Zoom Augmentation will randomly zoom the image and adds new pixels for the image
### Flipping:
- Flipping means rotating an image on a horizontal or vertical axis.
- In a horizontal flip, the flipping will be on the vertical axis, In a Vertical flip, the flipping will be on the horizontal axis.
- Flipping rearranges the pixels while protecting the features of the image
- Vertical flipping is not meant for some photos, but it can be useful in cosmology or for microscopic photos.
- Horizontal axis flipping is much more common than flipping the vertical axis. This augmentation is one of the easiest to implement and has proven useful on datasets such as CIFAR-10 and ImageNet. On datasets involving text recognition such as MNIST or SVHN, this is not a label-preserving transformation.
### Rotation:
- Random Rotate is a useful augmentation in particular because it changes the angles that objects appear in your dataset during training
- A source image is randomly rotated clockwise or counterclockwise by some number of degrees, changing the position of the object in the frame.
- Random rotation can improve your model without you having to collect and label more data.
- Rotation augmentations are done by rotating the image right or left on an axis between 1° and 359°. The safety of rotation augmentations is heavily determined by the rotation degree parameter. Slight rotations such as between 1 and 20 or − 1 to − 20 could be useful on digit recognition tasks such as MNIST, but as the rotation degree increases, the label of the data is no longer preserved post-transformation.
### Shear :
- The image will be distorted along an axis, mostly to create or rectify the perception angles…
- It's usually used to augment images so that computers can see how humans see things from different angles

### Shift:
- Shifting the entire pixels of an image from one position to another position is called shift augmentation. We have two types of shift augmentation:- Horizontal shift augmentation and Vertical shift augmentation
- A shift to an image means moving all pixels of the image in one direction(horizontally or vertically) 
- Some of the pixels will be clipped and there will be a region where new pixel values will be specified.

### Cropping:
- Cropping images can be used as a practical processing step for image data with mixed height and width dimensions by cropping a central patch of each image. Additionally, random cropping can also be used to provide an effect very similar to translations. The contrast between random cropping and translations is that cropping will reduce the size of the input such as (256,256) → (224, 224), whereas translations preserve the spatial dimensions of the image. Depending on the reduction threshold chosen for cropping, this might not be a label-preserving transformation. Hence this method is not useful for MNIST and SVHN datasets.
