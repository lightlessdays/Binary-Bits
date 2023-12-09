---
title: "Filters in Image Processing"
datePublished: Sat Dec 09 2023 05:54:03 GMT+0000 (Coordinated Universal Time)
cuid: clpxn4str000308l54xcl43ja
slug: filters-in-image-processing
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1702101223605/6dd14301-3eb4-4771-8410-75830f4a3744.png

---

Smoothing filters are used to reduce abrupt changes in intensity, often associated with random noise in images. By averaging nearby pixel values, these filters help reduce noise and create a more consistent, smoothed appearance.

Smoothing is commonly applied to reduce noise before tasks like image resampling to prevent aliasing issues. It helps in creating a more uniform image without distortion caused by overly sharp transitions.

Smoothing filters are effective in reducing irrelevant details or fine structures in an image. These details, smaller compared to the filter kernel size, are considered "irrelevant" and can be smoothed out.

In images with limited intensity levels, smoothing filters help in reducing false contours or artificial boundaries that arise due to inadequate gradation in intensity levels.

Smoothing filters work in combination with other image enhancement techniques such as histogram processing and unsharp masking to refine and improve image quality.

Linear spatial filtering involves convolving an image with a filter kernel. Smoothing kernels applied through convolution cause blurring in the image. The extent of blurring is determined by the kernel's size and coefficients.

Lowpass filters (smoothing filters) are fundamental as they serve as the basis for other essential filters in image processing like sharpening, bandpass, and bandreject filters. These filters are derived from lowpass filters.

Ultimately, smoothing filters play a crucial role in noise reduction, detail suppression, and image enhancement by blurring sharp transitions and irrelevant details, thereby improving image quality and aiding various image processing tasks.

based on the method applied, filters can be categorized as

1. **Linear filters**
    

Linear filtering is the filtering method where the value of output pixel is linear combinations of the neighboring input pixels. It can be done with convolution operation. For example, mean/average filters or Gaussian filter.

2\. **Non-Linear filters**

Non-linear filter is a filter whose output is not a linear function of its input. Non-linear filtering cannot be done with convolution or Fourier multiplication. Median filter is a simple example of a non-linear filter.

Combinedly, we have filters of types:

1. **Linear spatial filter**
    
2. **Linear frequency filter**
    
3. **Non-linear spatial filter**
    
4. **Non-linear frequency filter**
    

Now, let us discuss about some common filters in image processing and computer vision and their use.

### **Mean filter**

It is linear spatial filter mainly used for smoothing, noise reduction or blurring. It helps reducing the amount of intensity variation between neighboring pixels. The mean filter works by moving through the image pixel by pixel, replacing each value with the average grey level values of neighboring pixels, including itself. There exist two types of mean filters.

#### **a) Average filter**

The average filter uses all the coefficients in the kernel matrix the same.

![](https://miro.medium.com/v2/resize:fit:229/1*Qzm9cr2DS_pYY9Mux27q6w.png align="left")

Sample Average filter kernel

#### **b) Weighted-average filter**

In this, pixels are multiplied by different coefficients. The center pixel is multiplied by a higher value than an average filter.

The sample kernel for the average filter can be represented as

![](https://miro.medium.com/v2/resize:fit:875/1*hpalIbr2hfHRgS7SBjLNCA.png align="left")

The main drawback of this filter is that a single pixel with a high intensity value in the neighborhood is going to affect the average. Another point is that when the filter convolutes with edge values, we get blurred edges.

## **Order statistics filter**

This corresponds to non-linear spatial filters. It is based on the ordering of the pixels in the image. It replaces the value of the center pixel with the value determined by a ranking result. These filters avoid the kernel and convolution. Edges are better preserved in this type of filtering. Different types of order statistics filters are:

#### **1\. Minimum filter**

The minimum filter is one of the morphological filters. It is also called a **dilation filter**. The dark values present in an image are enhanced by the minimum filter. When the minimum filter is applied to a digital image it picks up the minimum value of the neighborhood pixels under the filter window and assigns it to the current pixel. A pixel with the minimum value means the darkest pixel from the window.

When the minimum filter is applied, the object boundaries present in an image are extended.

**2\. Maximum filter**

The maximum filter is also called the **erosion filter**. It works opposite to the minimum filter. When a maximum filter is applied, the darker objects present in the image are eroded. The maximum filter replaces each pixel value of a digital image with the maximum value(i.e., the value of the brightest pixel) of its neighborhoods.

Applying the maximum filter removes the negative outlier noise present in a digital Image.

#### **3\. Median filter**

The Median filter is a non-linear filter that is most commonly used as a simple way to reduce noise in an image. Here the pixel value is replaced by the median value of the gray level neighboring pixels. It claims noise reduction over Gaussian and edges are kept relatively sharper.

Median filters are particularly effective in the presence of impulse noise, also called salt-and-pepper noise.

## **Gaussian filter**

It is another linear spatial filter used for smoothing, noise reduction, or blurring. Gaussian filtering is more effective at smoothing images. It works similarly to human visual perception when processing images. The kernel coefficients diminish with increasing distance from the kernel’s center. Normally, the kernel matrix is considered symmetric and the size of the filter is odd. The values inside the kernel are computed by the Gaussian function, which is as follows:

![](https://miro.medium.com/v2/resize:fit:301/1*MoT2ChnYDx172IS8Avhg7A.png align="center")

Two-dimensional Gaussian function

In the Gaussian kernel, central pixels have a higher weighting than those on the periphery. The kernel for the Gaussian filter can be represented as

![](https://miro.medium.com/v2/resize:fit:169/1*pc1LYKdVQL8651vcucWxOA.png align="center")

The general form of Gaussian kernel (c&lt;a&lt;b)

A 3×3 Gaussian Kernel with standard deviation = 1, is as shown below.

![](https://miro.medium.com/v2/resize:fit:355/1*XWY_4IomfB4QmE4NAuft4w.png align="center")

source: geeksforgeeks

This filter is not particularly effective at removing salt and pepper noise.

## **Derivative filter**

The purpose of this linear spatial filter is just the opposite of the smoothing spatial filter. It helps in sharpening the digital image. Its main focus is the removal of blurring and highlighting of the edges. It is based on the first and second-order derivative for each group of pixel values considered in the x and y directions. Derivative filters provide a quantitative measurement for the rate of change in pixel brightness information present in a digital image.

When a derivative filter is applied to a digital image, the resulting information about brightness change rates can be used to enhance contrast, detect edges and boundaries, and measure feature orientation. Derivative filters are also called **gradient filters**.

A 3x3 first derivative filter for the x-direction is

![](https://miro.medium.com/v2/resize:fit:875/1*i27PtTv0sCAHbdeLv9BOpQ.png align="left")

3x3 DFDX filter

## **Low pass filter**

It is a linear frequency domain filter mechanism. A low pass filter removes the high-frequency components and keeps low-frequency components. It is used for smoothing the image. A low pass filter can be represented as **G(x,y)=H(x,y).F(x,y)** where F(x,y) is the Fourier Transform of the original image and H(x,y) is the Fourier Transform of the filtering mask.

## **High pass filter**

High pass filter works in the opposite manner of low pass filter. It removes the low-frequency components and keeps the high-frequency components. It is used for sharpening the image. A high pass filter is given by the equation **G\*(x,y)=1-G(x,y)** where G(x,y) is the low pass filtering output.

## **Bandpass filter**

Bandpass filter removes the very low-frequency and very high-frequency components and keeps the moderate range band of frequencies. Bandpass filtering is used to enhance edges by reducing the noise.

## **Butter-worth filter**

It is considered a variation of ideal low/high pass filters. In image processing, we use butter-worth low-pass filters for image smoothing. It removes high-frequency noises from the images. The transfer function of the Butterworth low pass filter is as follows

![](https://miro.medium.com/v2/resize:fit:303/1*BDpkTDRm7uNypSA7xAqYDA.png align="center")

D(x,y) is the Euclidean Distance from any point (x,y) to the origin of the frequency plane.D0 is a positive constant. The filter passes all the frequencies less than the D0 value without attenuation. Similarly, Butterworth high pass filters are designed for image sharpening in the frequency domain. The transfer function of the Butter-worth high pass filter is

![](https://miro.medium.com/v2/resize:fit:303/1*MjyvAuZuaeIxfQFhYCggWQ.png align="center")

A butter-worth filter is less applied to images since it operates only on the frequency domain. The butter-worth filter of higher orders suffers from ringing artifacts.