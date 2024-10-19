**Language**: 
- [中文](README.zh.md)
- [English](README.md)

# Spherical Image Arrangement

This project creates a dynamic spherical arrangement of images, allowing for customizable parameters to adjust the visual layout. The images are displayed on a 3D sphere, giving a unique presentation style for showcasing visuals.

## Features

- **Spherical Layout**: Images are arranged on a sphere, providing a 3D visual effect.
- **Orbital Animation**: Through the automaticly arrange with the scripts, accomplish the horizontally orbital animation.
- **Customizable Parameters**: Adjust the layout by modifying variables such as layer amount, sphere radius, and image size.
- **Animated Transition**: Images rotate around the sphere, creating an engaging user experience.

## Getting Started

To use this project, simply clone the repository and open the HTML file in your browser. You can customize the following parameters in the script section of Html:

### Parameters

- **imgUrls**: An array containing URLs of images to be displayed on the sphere. Add your image URLs here.
  
  ```javascript
  const imgUrls = [
      "https://via.placeholder.com/80x80",
      // Add more image URLs as needed
  ];

  const topImgUrl = "https://via.placeholder.com/80x80"; //The image at the sphere north pole
  const lowImgUrl = "https://via.placeholder.com/80x80"; //The image at the sphere south pole
  
- **manipulation**: The other parameters that can be changed.

    ```javascript
    let layerAmount = 7; // Latitude layers (only allows odd numbers)    
    let sphereRadius = 300; // Sphere radius
    let gapDistance = 20; // Gap distance, but each layer is multiplied by 0.5 to create an angular effect
    let gapProportion = 0.5; // Gap change rate between latitude layers
    let imgSideDecrease = 6; // px, Decrease in image size for each layer
    let imageSide = 80; // Image size on the equator, px
    let animationTimeStart = 30; // s
    let timeProportion = 1.2; // The multiplier rate of animation time from the equator to the poles
    let startDegreeCD = 10; // Difference in rotateY degrees at the start of the animation per layer, deg
    // the above part is where you can change as a property of the sphere.

## Warnings:
- **Load Lagging**: Setting the `layerAmount` or `sphereRadius` to a large value may result in slower loading times. Please adjust these parameters with caution to ensure optimal performance.
- **Odd Layer**: Which is on the TODO list now. You can only set odd number for layerAmount, and I will solve that as immediately as posible.

# To-Do List
- [ ] **Even Layer**: 
  - Implement support for an even number of layers. This adjustment will allow for more flexible configurations and enhance the overall balance of the design.
- [ ] **Smoother Gap**: 
  - Introduce an incremental adjustment to `gapDistance` for each layer, avoiding the need for a manipulated proportion. This will create a more natural transition between layers and improve the visual flow.
- [ ] **Smoother Size**: 
  - Refine the size adjustment of images to ensure a more visually appealing transition between layers. The goal is to create a seamless experience where size differences are less noticeable.

- [ ] **Match for Radius**: 
  - Adjust the radius parameters for each layer to ensure uniformity across the sphere. This will help in achieving a consistent appearance and enhance the overall aesthetic of the 3D representation.

- [ ] **Match for Time**: 
  - Synchronize the animation timings for different layers to create a cohesive movement effect. This includes fine-tuning the animation duration and delay settings to enhance the fluidity of transitions.

- [ ] **Match for Degree**: 
  - Ensure that the rotational degrees for each layer are consistent with the intended design. This will involve recalibrating the rotation angles to achieve the desired visual alignment and symmetry throughout the sphere.

  
