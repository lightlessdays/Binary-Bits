---
title: "The Light Spectrum"
datePublished: Thu Dec 07 2023 12:35:58 GMT+0000 (Coordinated Universal Time)
cuid: clpv6lz5x000908kyhxgibfmo
slug: the-light-spectrum
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1701952540956/554974f2-882c-4606-b764-3b9d75f4c888.png

---

Sir Isaac Newton discovered the spectrum of colors within sunlight by passing it through a prism, showing a range from violet to red. Visible light, perceived by humans, constitutes a small portion of the broader electromagnetic spectrum, with radio waves on one end and gamma rays on the other.

The electromagnetic spectrum can be expressed in terms of wavelength, frequency, or energy. Wavelength and frequency are related by the speed of light, while energy is proportional to frequency. The visible spectrum spans approximately 0.43 to 0.79 millimeters, divided into colors from violet to red.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701952345545/a9c6949c-5da1-4c01-a960-cf6647f4446e.png align="center")

**Wavelength**  
Formula: *λ*⋅*f*\=*c*  
*λ* (lambda) = Wavelength of the electromagnetic wave (meters)  
*f* = Frequency of the wave (Hertz) = 1/time period  
*c* = Speed of light

**Energy of Electromagnetic Waves:**  
Formula: *E*\=*h*⋅*f*  
*E* = Energy of the wave (in Joules or electron volts)  
ℎ = Planck's constant  
*f* = Frequency of the wave (Hertz)

The perceived color of an object is determined by the wavelengths of light it reflects. Objects reflecting balanced light across visible wavelengths appear white, while those favoring specific wavelengths exhibit colors. For instance, green objects reflect light primarily in the 500 to 570 nanometer range.

Light without color is termed monochromatic or achromatic, with its only attribute being intensity. Monochromatic light spans from black to gray to white, forming the grayscale, often used to describe monochromatic images.

Descriptions of chromatic light involve radiance, luminance, and brightness. In addition to frequency, three other quantities are used to describe a chromatic light source: radiance, luminance, and brightness. Radiance is the total amount of energy that flows from the light source, and it is usually measured in watts (W). Luminance, measured in lumens (lm), gives a measure of the amount of energy an observer perceives from a light source. For example, light emitted from a source operating in the far infrared region of the spectrum could have significant energy (radiance), but an observer would hardly perceive it; its luminance would be almost zero. Finally, brightness is a subjective descriptor of light perception that is practically impossible to measure. It embodies the achromatic notion of intensity and is one of the key factors in describing color sensation.

Imaging primarily relies on electromagnetic wave radiation. However, alternate methods like ultrasonic imaging (using reflected sound), electron microscopy (using electron beams), and software-generated synthetic images also contribute to digital imaging. However, the limitation is that the wavelength of electromagnetic waves needed to observe an object must be comparable to or smaller than the object's size. For instance, studying small objects like water molecules would require high-energy ultraviolet or low-energy X-ray bands.

Sometimes, the range of values spanned by the gray scale is referred to as the dynamic range, a term used in different ways in different fields. Here, we define the dynamic range of an imaging system to be the ratio of the maximum measurable intensity to the minimum detectable intensity level in the system. As a rule, the upper limit is determined by saturation and the lower limit by noise, although noise can be present also in lighter intensities. The figure below shows examples of saturation and slight visible noise. Because the darker regions are composed primarily of pixels with the minimum detectable intensity, the background in the figure is the noisiest part of the image; however, dark background noise typically is much harder to see.

The dynamic range establishes the lowest and highest intensity levels that a system can represent and, consequently, that an image can have.

Closely associated with this concept is image contrast, which we define as the *difference in intensity between the highest and lowest intensity levels in an image*.

The contrast ratio is the ratio of these two quantities. When an appreciable number of pixels in an image have a high dynamic range, we can expect the image to have high contrast. Conversely, an image with low dynamic range typically has a dull, washed-out gray look.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701952950677/aecba462-77a5-4a77-8f31-bd27c5ffcc76.png align="center")

I have already explained sampling and quantization.

*fst*​ represents an image function with continuous variables *s* and *t*. This continuous function is converted into a digital image *fxy*​ with discrete coordinates *x* and *y*, containing *M* rows and *N* columns.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953156016/be6d925c-08c1-4aea-899e-aa2db53f16df.png align="center")

The digital image structure, with the origin at the top left, forms a right-handed Cartesian coordinate system, rotated by 90 degrees. The center of an image (*M*×*N*) is found by dividing *M* and *N* by 2 and rounding down to the nearest integer.

Digitization involves decisions about *M*, *N*, and the number of discrete intensity levels, denoted by *L*. Often, *L* is an integer power of two due to digital storage and hardware considerations.

**Image contrast** is the difference in intensity between the highest and lowest intensity levels in an image.

The number of bits (*b*) required to store a digital image is given by *b*\=*MNk*, where *M* and *N* are dimensions and *k* is the number of discrete intensity levels.

Images with 2^*k* possible intensity levels are referred to as "k-bit images." For example, a 256-level image is called an 8-bit image.