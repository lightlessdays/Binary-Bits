---
title: "Histogram Equalization"
datePublished: Fri Dec 08 2023 05:17:25 GMT+0000 (Coordinated Universal Time)
cuid: clpw6dukg000108l2fk5cfl3d
slug: histogram-equalization
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1702012604087/53d7573d-8e24-469e-bd2a-5d993051e685.png

---

There are several methods for extracting data from an image. The image and essential information must be kept in mind when selecting a technique. This article focuses on “Histogram Equalization,” one of the ways to extract information from an image

Let’s say we have an image shown below.

![](https://editor.analyticsvidhya.com/uploads/40484university.png align="center")

The image contains a few trees, buildings, and lights but everything seems blackish. Can we make the image more clear so that more details become visible which are not visible right now (maybe by performing some operations on it)? The answer is yes, and that’s what we are going to do today. You must have guessed correctly that it is possible with histogram equalization. It is an algorithm used for enhancing an image in such a way that it becomes more pleasant to Human eyes. Before diving into an algorithm it’s important to understand what is the histogram.

## **What is Histogram?**

A histogram is a graphical representation of certain data similar to a bar chart. Let us start with a non-technical example to understand the same.

I asked some of my friends if they understood “What does histogram mean?” after showing them a definition of the Histogram. Here are the responses I received.

![](https://editor.analyticsvidhya.com/uploads/86720table.png align="center")

We can plot this information using the following graph. It shows the frequency of three different answers (Yes, no & somewhat) which is 5, 15, and 7 respectively.

![](https://editor.analyticsvidhya.com/uploads/93967What%20is%20Histogram.png align="center")

The graph shown above is nothing but the Histogram of the data given in the table.

So, histograms change as the data change and they give us a visual representation of how the data is spread. They show the frequency distribution of an attribute present in the data.

An image is nothing but an array of pixels. In RGB format it can be considered as a 3D array (3 overlapping 2D arrays of Red, Green and Blue components of the image). If the image size is axbx3 then it contains several rows, b number of columns and total a\*b pixels in one colour array/frame. Here, 3 represents 3 frames for the colours Red, Green and Blue. For the sake of understating, we are going to convert it into a grayscale image. A grayscale image is a 2D array where pixel values are a combination of white and black colours only. An image histogram is the distribution of image pixels’ values. Data type uint8 (which is mostly used) represents that each pixel is represented using 8 bits. As a consequence, pixels can achieve values between 0 and 255 ( 2<sup>8</sup> = 256). Now, let’s take a look at the image Histogram for the image shown at the start of the article.

![](https://editor.analyticsvidhya.com/uploads/84914histogram%20before%20equalization.png align="center")

The x-axis and y-axis represent the intensity of pixels and the number of pixels respectively. As discussed, pixels can take any value ranging from 0 to 255. The higher the pixel value brighter the pixel. As shown in the colour graph parallel to the x-axis: high and low pixel values represent white and black colours respectively.

As can be seen in the histogram, most of the pixels have intensity values between 0 to 50. The little part of the image that the human eye can recognize as white is also black (Not completely). In other words, the black part of the image is black and the white part of the image is not white but it is “less black”. What if we can represent the white part with higher intensity while not affecting the black part (much)? By doing so we can achieve more contrast in the image. This technique is nothing but, Histogram Equalization. Now we will look into mathematical representation for the same.

The goal is to achieve a uniform pdf distribution as shown below.

![](https://editor.analyticsvidhya.com/uploads/16091hitogram_equalization.png align="left")

Here L is the maximum value a pixel can achieve. Pr(r) is the probability density function (PDF) of the image before equalization. Ps(s) is PDF of the image after performing equalization. Ps(s) is an equalized histogram that is uniformly distributed among all the possible values. The transfer function shown below converts Pr(r) to Ps(s).

![](https://editor.analyticsvidhya.com/uploads/46797eq1.png align="center")

Now, the differentiation of s concerning r is

![](https://editor.analyticsvidhya.com/uploads/45868eq2.png align="center")

Relation between Pr(r) and Ps(s) can be achieved as

![](https://editor.analyticsvidhya.com/uploads/60687eq3.png align="center")

So, as can be seen, Ps(s) is a normalized distribution. We can say that equalization of the histogram can be achieved by an assumed transfer function.

![](https://editor.analyticsvidhya.com/uploads/72385comparision.png align="left")

We can see that contrast in an image can be increased by equalizing its histogram. The new image we get from the equalized histogram has higher contrast and details than the original one. Let’s take a close look at the new image.

![](https://editor.analyticsvidhya.com/uploads/70328equalized%20image.png align="left")

There are variations of the histogram equalization.

### Global Histogram Equalization

Global histogram equalization (GHE) is the most simple type of histogram equalization. As the name suggests, here, the algorithm is applied to the whole image. This is the same one discussed throughout this article. However, there is a problem with this technique. If the image already has very high contrast (it consists of both very bright and very dark parts), then small details will get removed while equalizing it. In other words, GHE is not suitable for images having a histogram that is distributed at both extremes of pixel values. We can see the effect in the image shown below.

![](https://editor.analyticsvidhya.com/uploads/82817limit1.png align="left")

### Local Histogram Equalization

![](https://editor.analyticsvidhya.com/uploads/36968local.png align="center")

In Local histogram equalization (LHE), the algorithm is applied to a local group of pixels of the image. First of all, the image is divided into equal small regions that are known as tiles. Then the algorithm is applied to each tile, separately. This solves the problem raised by GHE. But it faces another problem. As can be seen in the image, tiles are visible due to high contrast at the edges. Due to this problem, this is the least used algorithm.

### Uses of Histogram Equalization

* I**mprove image contrast:** Histogram equalization can make images brighter and easier to see by redistributing the pixel values in the image. This is especially useful for low-contrast images.
    

* **Reveal details hidden by poor contrast:** It can also make it possible to see details in images that are hidden by poor contrast. This can be helpful for medical imaging, security surveillance, and photography.
    

* **Improve image processing and computer vision results:** It can improve the accuracy of image processing and computer vision algorithms, such as object detection and tracking algorithms, image classification algorithms, and image segmentation algorithms.
    

* **Enhance medical images:** It is a popular technique for enhancing medical images, such as X-rays, MRI scans, and CT scans. By improving the contrast of medical images, histogram equalization can make it easier for doctors to diagnose diseases and make better treatment decisions.
    

* **Improve photo quality:** It can also be used to improve the quality of photographs. For example, it can be used to make photos that are too dark or too bright look more natural and balanced. It can also be used to enhance the colours in a photo.