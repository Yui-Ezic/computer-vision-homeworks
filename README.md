# Computer vision homeworks

## Lesson 2

[Jupyther notebook](lesson-2/homework/Homework.ipynb)

Implemented color balancing algorithms:

- **White patch**
  ![White patch example](lesson-2/homework/results/white-patch.png)
- **Gray world**
  ![Gray world example](lesson-2/homework/results/gray-world.png)
- **Scale-by-max**
  ![Scale-by-max example](lesson-2/homework/results/scale-by-max.png)
  > This image is not suitable for this algorithm because only the blue channel changes slightly, and the overall appearance of the image remains almost the same.

## Lesson 3

[Jupyther notebook](lesson-3/homework/Homework.ipynb)

Implemented unsharp masking with gaussian blur:

![Unsharp masking](lesson-3/homework/results/unsharp-masking-by-gauss.png)

## Lesson 4

[Jupyther notebook](lesson-4/homework/Homework.ipynb)

Detect lane lines:

![Detected lane lines](lesson-4/homework/results/detected-lane-lines.png)

## Lesson 5

[Jupyther notebook](lesson-5/homework/Homework.ipynb)

Image quantization with different color paliters:

Original image:

![Original image](lesson-5/data/kodim23.png)

Left image is optimally quantized, right is with Floyd-Steinberg Dithering

- **2 gray tone colors**

![4 colors](lesson-5/homework/results/2-colors.png)

- **4 gray tone colors**

![4 colors](lesson-5/homework/results/4-colors.png)

- **16 gray tone colors**

![4 colors](lesson-5/homework/results/16-colors.png)

- **256 gray tone colors**

![4 colors](lesson-5/homework/results/256-colors.png)

- **5 pure colors** (black, white, red, green, blue)

![5 pure colors](lesson-5/homework/results/5-colored-colors.png)

If you enlarge the image, you can see that there are actually 5 colors (left - original, right - quantized).

![5 pure colors](lesson-5/homework/results/5-colors-scale-1.png)
![5 pure colors](lesson-5/homework/results/5-colors-scale-2.png)

## Lesson 6

[Jupyther notebook](lesson-6/homework/Homework.ipynb)

Using the Harris corner detector to detect the corners of a document.

Original image:

![Original document](lesson-6/data/document.jpg)

At first find all corners, than filter it to keep only document corners.

![Detected corners of document](lesson-6/homework/results/detected-document-corners.png)

## Lesson 7

[Jupyther notebook](lesson-7/homework/Homework.ipynb)

Use perspective transform to rectify document image:

![Rectified document](lesson-7/homework/results/rectified.png)

## Lesson 8

[Jupyther notebook](lesson-8/homework/Homework.ipynb)

**Otsu’s Thresholding** to separate document text from background:

![Binarized document](lesson-8/homework/results/otsu-thresholded.png)

The result is not very good, because this image is not suitable for Otsu’s Thresholding. There is more than two clusters of pixels. One of the reasons is uneven lightning of the image.

So instead of Otsu’s Thresholding we should use more advanced methods, like [Sauvola Thresholding](https://wahabaftab.com/Sauvola-Thresholding-Integral-Images/) which calculate threshold for each pixel instead of one global threshold, or K-means.

**Sauvola Thresholding**

![Sauvola 5](lesson-8/homework/results/sauvola-5.png)
![Sauvola 15](lesson-8/homework/results/sauvola-15.png)

Sauvola threshold with k=0.2 and n=15 still not perfect, but better than Otsu’s Thresholding. And I think that if you experiment, you can choose more optimal coefficients to get better results with Sauvola Thresholding.
