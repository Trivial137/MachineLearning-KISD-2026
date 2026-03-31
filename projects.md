# Proposed projects

All participants of the course should present a project to get a final grade. You can invent your own projects, possibly connected to your research, 
but if you have problems finding a project topic I give you here few ideas. **You can prepare your projects in the groups.**

* **Classification of medical images**
  Take Chest X-Ray Images (Pneumonia) from kaggle https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia and classify them (healthy vs. sick) using convolutional neural network. I would suggest to use one of the pretrained Keras networks https://keras.io/api/applications/ to get the best results.

 * **GradCam**
   The use of GradCam approach described here https://keras.io/examples/vision/grad_cam/ allows us to find, which part of an images is most important for classification. You can try to have a look which part of an X-ray image from the previous project decides about classification result (but you can use any other images). 

 * **Localize objects on pictures**
Generate images with few objects of class 1 (for example squares) and few of class 0 (for example triangles) on one image. The task is to localize all class 1 objects in this image.
The U-Net takes an image as an input and outputs a heatmap of the same size — a grayscale image where bright spots indicate predicted object locations. During training, the ground-truth heatmap is constructed by placing a Gaussian blob at each known object center location, so the network learns to associate image patterns with the probability map: "there is an object here." The U-Net architecture is ideal for this task because its encoder compresses the image to understand what is present, while the decoder with skip connections reconstructs full spatial resolution to pinpoint where — preserving precise localization. At inference, the predicted heatmap is post-processed with a simple peak-finding algorithm (peak_local_max) to extract discrete center coordinates from the continuous probability map.

* **Generative network**
Try to generate some simple objects using GAN or Diffusion Models (some very simple images, could be artificially generated images or Fashion MNIST dataset. You can restrict the Fashion MNIST dataset to few types of clothes).

* **Autoncoder**
Using an autoencoder try to perform best mapping of Fashion MNIST on 2D map. Use autoencoder to detect outliers. 
