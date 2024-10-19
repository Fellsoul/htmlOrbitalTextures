**Language**: 
- [中文](README.zh.md)
- [English](README.md)

# Html Orbital Textures
该项目创建了一个动态的图像球形排列，允许自定义参数以调整视觉布局。图像显示在一个 3D 球体上，为展示视觉效果提供了独特的展示风格。

## 样式
- **球形布局**：图像排列在一个球体上，提供 3D 视觉效果。
- **轨道动画**：通过脚本自动排列，实现水平轨道动画。
- **可自定义参数**：通过修改变量来调整布局，例如层数、球半径和图像大小。
- **动画过渡**：图像围绕球体旋转，创造吸引人的用户体验。

## 如何引用改样式
要使用此项目，只需克隆此代码库并在浏览器中打开 HTML 文件。您可以在 HTML 的脚本部分自定义以下参数：

### 参数介绍以及调整
- `imgUrls`：一个包含要在球体上显示的图像 URL 的数组。可以在此处添加您的图像 URL。

    ```javascript
    const imgUrls = [
        "https://via.placeholder.com/80x80",
        // 根据需要添加更多图像 URL
    ];
    
    const topImgUrl = "https://via.placeholder.com/80x80"; // 球体北极的图像, 默认X轴旋转90°形成平铺
    const lowImgUrl = "https://via.placeholder.com/80x80"; // 球体南极的图像, 默认X轴旋转90°形成平铺

- `manipulation`: 可以更改的其他参数.
    ```javascript
      let layerAmount = 7; // 纬度层（仅允许为奇数）
      let sphereRadius = 300; // 球半径
      let gapDistance = 20; // 间隔距离，但每层会乘以 0.5 以创建角度效果
      let gapProportion = 0.5; // 纬度层之间的间隔变化率
      let imgSideDecrease = 6; // px，每层图像大小的减少
      let imageSide = 80; // 赤道上的图像大小，px
      let animationTimeStart = 30; // s
      let timeProportion = 1.2; // 从赤道到两极的动画时间乘数
      let startDegreeCD = 10; // 动画开始时每层的 rotateY 公差，deg
    // the above part is where you can change as a property of the sphere.

## 警告:
- **加载延迟**: 将 layerAmount 或 sphereRadius 设置为较大值可能导致加载时间变慢。请谨慎调整这些参数以确保最佳性能。
- **奇数层**: 目前只能设置奇数层数的 layerAmount，我会尽快解决这个问题。

# To-Do List
- [ ] **偶数层**: 
  - 实现对偶数层数的支持。这一调整将允许更灵活的配置，并增强整体设计的平衡性。
- [ ] **平滑间隔**: 
  - 在每层的 gapDistance 上引入逐步调整，避免需要操控比例。这将创造更自然的层间过渡，改善视觉流畅度。
- [ ] **平滑大小**: 
  - 优化图像的大小调整，以确保各层之间的过渡更具视觉吸引力。目标是创建一个无缝的体验，使大小差异不那么明显。

- [ ] **匹配半径**: 
  - 调整每层的半径参数，以确保球体的一致性。这将帮助实现一致的外观，增强 3D 表现的整体美感。

- [ ] **匹配时间**: 
  - 自动更改不同层的动画总时长，以创建自动的动画时间。这包括微调动画持续时间和延迟设置，以增强过渡的流畅性。

- [ ] **匹配度数**: 
  - 确保每层的旋转度数与设计意图一致。这将涉及重新校准旋转角度，以实现所需的视觉对齐和对称性。

  
