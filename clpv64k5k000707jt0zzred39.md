---
title: "Brightness Adaptation"
datePublished: Thu Dec 07 2023 12:22:26 GMT+0000 (Coordinated Universal Time)
cuid: clpv64k5k000707jt0zzred39
slug: brightness-adaptation
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1701951725841/d36a3dc4-82de-438b-b49a-b5e9d128fab9.png

---

Digital images represent light as discrete intensities, but our eyes perceive brightness in a non-linear way. For example, a small increase in very bright light might not seem as noticeable as the same increase in dim light.

Our eyes can adapt to different levels of brightness, but they can't handle the entire range of intensities all at once. Instead, they adjust sensitivity, focusing on a specific level of brightness. This adjustment is called brightness adaptation.

Imagine a graph where light intensity is on one axis and perceived brightness is on the other. This graph shows that the eye's ability to perceive brightness follows a logarithmic function. It means our perception of brightness changes more for lower light changes and less for higher light changes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701951164887/029dc9d2-8f8a-48de-8fcf-f8e83c881d72.png align="center")

### Weber Ratio

The Weber ratio is a concept used to measure the sensitivity of the human eye to changes in brightness or intensity. It's named after Ernst Weber, a 19th-century psychologist who contributed to the understanding of sensory perception.

The Weber ratio helps us understand how sensitive our eyes are to detect changes in brightness against a background of constant illumination.

The Weber ratio (ΔI/I​) is the smallest noticeable change (ΔI) in the intensity of light (brightness) compared to the background intensity (I). It's expressed as a ratio or percentage.

Imagine you're looking at a screen with a constant level of brightness. Now, a small additional light is added to the screen. The Weber ratio measures the smallest additional light (ΔI) that you can notice against the background light level (I).

A smaller Weber ratio means that very slight changes in brightness are noticeable against the background, indicating high sensitivity to changes.

A larger Weber ratio means a larger change in brightness is needed for detection, suggesting lower sensitivity to changes.

This ratio is widely used in various fields, including psychology, physiology, and image processing, to understand human perception thresholds. In image processing, it helps determine how finely different intensity levels need to be represented for the human eye to distinguish them.

For instance, let's say you're in a dimly lit room (background intensity I \=50 units) and someone increases the light by 5 units (ΔI=5 units). If you can notice this change consistently, the Weber ratio would be 5/50=0.1 or 10%. This means you can perceive a 10% change in brightness against the initial background.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701951647256/6d2464fb-550b-4217-b05e-edc36bc4f846.png align="center")

### Mach Bands

Mach bands are a visual phenomenon related to human perception of brightness or intensity along the edges where two contrasting areas meet. Named after physicist Ernst Mach, these bands illustrate how our eyes perceive contrast at boundaries between regions of different intensities.

Mach bands appear as exaggerated bright or dark bands along the edges where two areas of different brightness levels meet. For instance, when a lighter area borders a darker one, the lighter area may appear even brighter at the border, and the darker area seems even darker.

The perception of Mach bands is due to the way our visual system processes information at boundaries of different intensities. It's not actually an alteration of the physical light, but rather an illusion created by our eyes and brain.

Our visual system enhances the contrast at the edges between light and dark areas. When light transitions to dark (or vice versa), our perception exaggerates the difference, making the lighter side seem even brighter and the darker side appear even darker than they truly are.

Mach bands illustrate how our eyes and brain interpret contrast at edges. This phenomenon is often utilized in image processing and display technologies to enhance the perceived sharpness or contrast in images.

One practical example is in digital images or printed materials where borders between colors or shades can seem more pronounced than they actually are. This effect is often deliberately used in graphic design to create a sense of depth or emphasis.

Mach bands suggest that our eyes amplify the perceived intensity or brightness differences at boundaries to aid in the perception of objects' edges and shapes.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701951615749/6a018838-f55e-4322-a604-8612e3541790.png align="center")

In essence, the eye's perception of brightness isn't solely determined by light intensity. Factors like adaptation levels, context, and optical illusions play a significant role in how we perceive images.