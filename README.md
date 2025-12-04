# 🌌Y2K PARTICLE CORE // WALLPAPER EDITION

> **"Experience the Geometry of System Sound."**
>
> 一个深度优化的 WebGL 动态壁纸引擎。基于 **Three.js** 高性能渲染，通过 **Wallpaper Engine API** 直接捕获系统底层音频流，在桌面上重现《星际穿越》般的四维空间体验。

------

## ⚡️ 核心功能 (Key Capabilities)

### 1. 🧬 系统音频同步 (System Audio Sync)

不再需要手动上传文件或麦克风。引擎直接挂钩系统声卡输出：

- **LOW (0-60Hz):** 驱动 **Radial Explosion (径向爆发)**。贝斯与鼓点越重，粒子向外扩散的动能越大。
- **MID (250-2000Hz):** 驱动 **Vortex Torque (涡流扭矩)**。人声与旋律会产生旋转引力，扭曲空间几何。
- **HIGH (2000Hz+):** 驱动 **High-Freq Shimmer (高频微颤)**。高音触发粒子表面的高光闪烁。

### 2. 🖥️ 桌面原生体验 (Native Integration)

专为 **Wallpaper Engine** 优化：

- **静默启动:** 无需任何点击或权限弹窗，开机即运行。
- **鼠标交互:** 点击桌面任意空白处即可切换几何形态。
- **性能优化:** 针对长时间运行优化，降低 GPU 闲置占用。

### 3. 📐 9种超验数学形态 (Transcendental Geometries)

内置 9 套参数化方程生成器，点击鼠标即可无缝变形 (Morphing)：

| **交互** | **形态名称**         | **数学原理**          |
| -------- | -------------------- | --------------------- |
| `Click`  | **WORMHOLE**         | 动态时空隧道          |
| `Click`  | **DATA_HELIX**       | 破碎的 DNA 双螺旋     |
| `Click`  | **CYBER_GRID**       | 正弦波地形矩阵        |
| `Click`  | **STARGATE**         | 复杂多层环面结构      |
| `Click`  | **NEBULA_KNOT**      | 高维扭结投影          |
| `Click`  | **MOBIUS_STRIP**     | 单面拓扑循环          |
| `Click`  | **LORENZ_ATTRACTOR** | 混沌吸引子 (蝴蝶效应) |
| `Click`  | **HYPER_TORUS**      | 4D 环面 3D 投影       |
| `Click`  | **FIBONACCI_SPHERE** | 黄金分割点阵球体      |

### 4. 🎛️ 极简 HUD 界面

- **Visual Spectrum:** 桌面右上角保留极简的三频段频谱分析条。
- **Visual Style:** 采用 "Share Tech Mono" 字体与全息磨砂玻璃材质，融入桌面背景。

------

## 📂 项目结构 (Structure)

Plaintext

```
Y2K_Visualizer/
├── index.html       # 核心壁纸入口 (包含 Logic, Shader, UI)
├── project.json     # Wallpaper Engine 配置文件
├── preview.jpg      # (可选) 壁纸预览图
└── README.md        # 说明文档
```

------

## 🚀 安装指南 (How to Install)

1. **准备文件**: 确保文件夹中包含 `index.html` 和 `project.json`。
2. **打开软件**: 启动 **Wallpaper Engine** (Steam)。
3. **编辑器**: 点击底部的 **"Wallpaper Editor" (壁纸编辑器)**。
4. **导入**:
   - 点击 "Create Wallpaper" (创建壁纸)。
   - 选择 "Open Project Folder" 并定位到本项目文件夹。
   - 或者直接选择 `index.html` 打开。
5. **应用**: 点击编辑器左上角的 "File" -> "Apply Wallpaper"。



您也可以通过Python在网页端运行进行预览

```cmd
python -m http.server 8000
```

运行成功后访问 http://localhost:8000/AudioVisualization.html 页面即可

通过点击页面上的 START_SYSTEM_CAPTURE 进行共享（点击共享整个屏幕+点击同时共享系统音频）

------

## ⚙️ 高级配置 (Configuration)

在 `index.html` 代码中，您可以修改顶部的常量来定制性能：

JavaScript

```
// 修改粒子总数 (降低此数值可显著减少 GPU 占用)
// 推荐: Laptop (20000), Desktop (36000), High-End (60000)
const COUNT = 32000; 

// 修改辉光强度 (Bloom)
bloomPass.strength = 1.8;

// 修改自动旋转速度
let rotSpeed = 0.001;
```

------

## ❓ 常见问题 (Troubleshooting)

**Q: 粒子不随音乐跳动？**

- A: 1. 确保 Wallpaper Engine 设置中 "Audio Recording" (音频录制) 已开启。
  2. 确保系统音量不是静音。
  3. 某些音频增强软件（如 Nahimic, Sonic Studio）可能会拦截音频流，尝试关闭它们。

**Q: 只有黑色背景，没有粒子？**

- **A:** 这通常是因为 GPU 驱动不支持某些 WebGL 特性。尝试在 Wallpaper Engine 设置中将 "Web Framework" 切换为 "Chromium" 或更新显卡驱动。

**Q: GPU 占用过高？**

- **A:** 在 `index.html` 中将 `const COUNT` 的数值改小（例如 15000），或者降低 `renderer.setPixelRatio` 的数值。

------

## 🛠 技术栈 (Tech Stack)

- **Render Engine:** [Three.js r160](https://threejs.org/)
- **Audio System:** Wallpaper Engine Audio Listener API
- **Post-Processing:** UnrealBloomPass (High Performance)
- **Shader Language:** WebGL GLSL (Custom Vertex/Fragment Shaders)

------

## 📜 版权 (License)

**MIT License**

Copyright (c) 2025 **Boran Made**

Permission is hereby granted, free of charge, to any person obtaining a copy

of this software and associated documentation files (the "Software"), to deal

in the Software without restriction, including without limitation the rights

to use, copy, modify, merge, publish, distribute, sublicense, and/or sell

copies of the Software, and to permit persons to whom the Software is

furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all

copies or substantial portions of the Software.
