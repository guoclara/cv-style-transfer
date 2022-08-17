# Artistic Style Transfer Computer Vision Final Project

## First Model: CNN
<img width="579" alt="Screen Shot 2022-08-17 at 3 17 46 PM" src="https://user-images.githubusercontent.com/48026886/185224318-a29463ae-2801-4b35-a998-8712dda5649b.png">
Using 1 image for style and 1 image for content, we trained a conventional CNN to transfer solely the style of the style image to the content image. We took the first convolutional layer of the 5 blocks of vgg to calculate style loss and the second convolutional layer of the blocks to calculate content loss and created a weighted sum to serve as the loss to train our CNN.

**Results:**

<img width="400" alt="Screen Shot 2022-08-17 at 4 41 02 PM" src="https://user-images.githubusercontent.com/48026886/185238970-e17c421a-5a20-42e0-b2b5-bce634d09c2a.png"><img width="418" alt="Screen Shot 2022-08-17 at 4 43 46 PM" src="https://user-images.githubusercontent.com/48026886/185239420-0cfaba22-c2a7-43e7-adb4-992ca7410ff7.png">


## Second Model: Autoencoder
<img width="640" alt="Screen Shot 2022-08-17 at 3 17 57 PM" src="https://user-images.githubusercontent.com/48026886/185224350-8ed1f15d-1bcd-4132-81ab-fb4cf01da974.png">

We used vgg19 as the encoder and created our own decoder. In between the encoder and decoder, we pass the image through an adaptive instance normalization layer that normalizes batches of content images to have the same mean and variance as its respective batch of style images in attempt to transfer style, which was not as successful.
