---
title: "Processing Signals in Digital Images"
datePublished: Thu Oct 26 2023 10:22:00 GMT+0000 (Coordinated Universal Time)
cuid: clo71bwns000b09mi9b96c4kh
slug: processing-signals-in-digital-images
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698315692940/9c5dd0c0-ca8d-4bb6-84e5-ba0d15555241.png
tags: image-processing

---

Digital image processing deals with the manipulation of digital images through a digital computer. It is a subfield of signals and systems but focuses particularly on images. DIP focuses on developing a computer system that is able to perform processing on an image. The input of that system is a digital image and the system processes that image using efficient algorithms and gives an image as an output. The most common example is Adobe Photoshop. It is one of the widely used applications for processing digital images.

## Types of Image Processing

There are two kinds of digital image processing: Analog Image Processing and Digital Image Processing.

### Analog Image Processing

Analog image processing is done on analog signals. It includes processing on two-dimensional analog signals. In this type of processing, the images are manipulated by electrical means by varying the electrical signal. A common example includes is the television image.

### Digital Image Processing

Digital image processing deals with developing a digital system that performs operations on a digital image. Digital image processing has dominated analog image processing with the passage of time due to its wider range of applications.

## What is an Image?

An image is nothing more than a two-dimensional signal. It is defined by the mathematical function f(x,y) where x and y are the two coordinates horizontally and vertically. The value of f(x,y) at any point gives the pixel value at that point of an image.

![Small Size World Famous Fries®: Calories & Nutrition | McDonald's](https://s7d1.scene7.com/is/image/mcdonalds/DC_202002_6050_SmallFrenchFries_Standing_832x472:1-3-product-tile-desktop?wid=765&hei=472&dpr=off align="left")

The above figure is an example of a digital image that you are now viewing on your computer screen. But actually, this image is nothing but a two-dimensional array of numbers ranging between 0 and 255.

<table><tbody><tr><td colspan="1" rowspan="1"><p>128</p></td><td colspan="1" rowspan="1"><p>30</p></td><td colspan="1" rowspan="1"><p>123</p></td></tr><tr><td colspan="1" rowspan="1"><p>232</p></td><td colspan="1" rowspan="1"><p>123</p></td><td colspan="1" rowspan="1"><p>321</p></td></tr><tr><td colspan="1" rowspan="1"><p>123</p></td><td colspan="1" rowspan="1"><p>77</p></td><td colspan="1" rowspan="1"><p>89</p></td></tr><tr><td colspan="1" rowspan="1"><p>80</p></td><td colspan="1" rowspan="1"><p>255</p></td><td colspan="1" rowspan="1"><p>255</p></td></tr></tbody></table>

Each number represents the value of the function f(x,y) at any point. In this case, the values 128, 230, and 123 each represent an individual pixel value. The dimensions of the picture are actually the dimensions of this two-dimensional array.

## Signal Processing

In the physical world, any quantity measurable through time over space or any higher dimension can be taken as a signal. A signal is a mathematical function, and it conveys some information.

A signal can be one dimensional or two-dimensional or higher dimensional signal. One dimensional signal is a signal that is measured over time. A common example is a voice signal.

The two-dimensional signals are those that are measured over some other physical quantities. An example of a two-dimensional signal is a digital image.

Anything that conveys information or broadcasts a message in the physical world between two observers is a signal. That includes speech (human voice) or an image as a signal. When we speak, our voice is converted to a sound wave/signal and transformed with respect to the time of to person we are speaking to. Not only this, but the way a digital camera works, as acquiring an image from a digital camera involves the transfer of a signal from one part of the system to the other.

Since capturing an image from a camera is a physical process. The sunlight is used as a source of energy. A sensor array is used for the acquisition of the image. So when the sunlight falls upon the object, the amount of light reflected by that object is sensed by the sensors, and a continuous voltage signal is generated by the amount of sensed data. In order to create a digital image, we need to convert this data into a digital form. This involves sampling and quantization.

Signal processing is an umbrella and image processing lies under it. The amount of light reflected by an object in the physical world (3D world) is passed through the lens of the camera and it becomes a 2D signal and hence results in image formation. This image is then digitized using methods of signal processing and then this digital image is manipulated in digital image processing.

![Is Digital really Analog?](https://media.licdn.com/dms/image/C4E12AQHT28-4NFrQpQ/article-cover_image-shrink_600_2000/0/1540568111801?e=2147483647&v=beta&t=WhrdAUEScou5tEl1Hn3DQwW9uRbfTgOundzCX8imips align="center")

### Analog Signals

A signal could be an analog quantity which means it is defined with respect to the time. It is a continuous signal. These signals are defined over continuous independent variables. They are difficult to analyze, as they carry a huge number of values. They are very accurate due to a large sample of values. In order to store these signals, you require an infinite memory because it can achieve infinite values on a real line. Analog signals are denoted by sin waves. The human voice is an example of an analog signal. When you speak, the voice that is produced travels through the air in the form of pressure waves and thus belongs to a mathematical function, having independent variables of space and time and a value corresponding to air pressure.

Another example is of sin wave.

![Sine Wave - Example, Breakdown, Example, Formula](https://cdn.corporatefinanceinstitute.com/assets/sine-wave.png align="center")

### Digital Signals

As compared to analog signals, digital signals are very easy to analyze. They are discontinuous signals. They are the appropriation of analog signals.

The word digital stands for discrete values and hence it means that they use specific values to represent any information. In a digital signal, only two values are used to represent something i-e: 1 and 0 (binary values). Digital signals are less accurate than analog signals because they are the discrete samples of an analog signal taken over some period of time. However digital signals are not subject to noise. So they last long and are easy to interpret. Digital signals are denoted by square waves.

Whenever a key is pressed from the keyboard, the appropriate electrical signal is sent to the keyboard controller containing the ASCII value of that particular key. For example, the electrical signal that is generated when keyboard key a is pressed, carries information of digit 97 in the form of 0 and 1, which is the ASCII value of character a.

### Conversion from Analogous to Digital Signal

A system is defined by the type of input and output it deals with. Since we are dealing with signals, in our case, our system would be a mathematical model, a piece of code/software, a physical device, or a black box whose input is a signal and it performs some processing on that signal, and the output is a signal. The input is known as excitation and the output is known as response.

![System](https://www.tutorialspoint.com/dip/images/system.jpg align="center")

In the above figure, a system has been shown whose input and output both are signals but the input is an analog signal. The output is a digital signal. It means our system is actually a conversion system that converts analog signals to digital signals.

But why do we need such a system? What is the need for conversion?

1. The first and obvious reason is that digital image processing deals with digital images, that are digital signals. So whenever the image is captured, it is converted into digital format and then it is processed.
    
2. The second and important reason is, that in order to perform operations on an analog signal with a digital computer, you have to store that analog signal in the computer. And in order to store an analog signal, infinite memory is required to store it. And since that's not possible, so that's why we convert that signal into digital format and then store it in a digital computer, and then perform operations on it.
    

Now let us look inside this system. To look inside this system we will need to understand two terms: Quantization and Sampling.

#### Sampling

Sampling as its name suggests can be defined as taking samples. Take samples of a digital signal over the x-axis. Sampling is done on an independent variable. In the case of this mathematical equation:

![Sampling](https://www.tutorialspoint.com/dip/images/sampling.jpg align="center")

Sampling is done on the x variable. We can also say that the conversion of the x-axis (infinite values) to digital is done under-sampling.

Sampling is further divided into up-sampling and down-sampling. If the range of values on the x-axis is less then we will increase the sample of values. This is known as upsampling and its vice versa is known as downsampling.

#### Quantization

Quantization as its name suggests can be defined as dividing into quanta (partitions). Quantization is done on the dependent variable. It is opposite to sampling.

In the case of this mathematical equation y = sin(x)

Quantization is done on the Y variable. It is done on the y-axis. The conversion of y-axis infinite values to 1, 0, -1 (or any other level) is known as Quantization.

These are the two basic steps that are involved in converting an analog signal to a digital signal.

The quantization of a signal has been shown in the figure below.

![Quantization](https://www.tutorialspoint.com/dip/images/quantization.jpg align="center")

### Types of Systems

Although it is not very important, there are two other kinds of systems as well: the continuous system and the discrete system.

#### Continuous Systems

The type of systems whose input and output both are continuous signals or analog signals are called continuous systems.

![Continuous Systems](https://www.tutorialspoint.com/dip/images/continuous_systems.jpg align="center")

#### Discrete Systems

The type of systems whose input and output both are discrete signals or digital signals are called digital systems.

![Discrete Signals](https://www.tutorialspoint.com/dip/images/discrete_signals.jpg align="center")