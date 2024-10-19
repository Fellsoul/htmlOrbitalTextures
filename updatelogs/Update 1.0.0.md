# Changelog

## [1.0.0] - 2024-10-18
### Major Updates
- **Project Launch**: Initial release of the Spherical Image Arrangement project.
  
### New Features
- **Spherical Layout**: Implemented the arrangement of images on a 3D sphere, providing a unique visual effect.
- **Orbital Animation**: Added scripts for automatic arrangement, achieving horizontal orbital animation of images.
- **Customizable Parameters**: Allowed users to adjust layout by modifying variables such as layer amount, sphere radius, and image size.
- **Animated Transition**: Implemented image rotation around the sphere, enhancing user experience.

### Warnings and Limitations
- **Odd Layer Support**: Currently, only odd numbers for layerAmount are supported; even layer support will be added in future versions.
- **Performance Notice**: Setting large values for layerAmount or sphereRadius may lead to slower loading times.

### To-Do List
- Implement support for an even number of layers.
- Introduce incremental adjustments to gapDistance.
- Refine size adjustments of images for smoother transitions.
- Adjust radius parameters to ensure uniformity.
- Synchronize animation timings to enhance fluidity.
- Ensure rotational degree consistency across layers.
