# 基于 Canvas 粒子系统的非线性视觉叙事研究
# (Non-linear Visual Narrative Research based on Canvas Particle System)

![GitHub top language](https://img.shields.io/github/languages/top/QianShark/love_code?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/QianShark/love_code?style=flat-square)

## 1. 摘要 (Abstract)
本项目实现了一个基于 HTML5 Canvas API 的高动态粒子渲染系统。通过建立离散粒子群（Particle Swarm）与几何参数方程（Parametric Equations）之间的映射关系，项目展示了一系列具有情感内涵的视觉变换。该系统具有高帧率、响应式布局以及基于 CSS3 的渐变视觉增强等特性。



---

## 2. 核心技术实现 (Technical Implementation)

### 2.1 粒子动力学模型 (Particle Dynamics)
系统核心由 `Particle` 类驱动，每个粒子对象包含：
* **插值运动**: 利用速度矢量 $vx, vy$ 实现从当前位置到目标坐标（Destination）的平滑过渡。
* **相位模拟**: 通过正弦函数 $Math.sin(phase)$ 模拟粒子闪烁的透明度变化。
* **形态演变**: 粒子被建模为可旋转的菱形，增强了视觉的折射感。

### 2.2 几何变换算法 (Geometric Algorithms)
项目通过不同的数学模型实时重算 2800 个粒子的目标点：
* **心形线 (Heart)**: 基于经典的参数方程构建实心映射。
* **花卉 (Flower)**: 采用五瓣玫瑰曲线模型。
* **彩虹 (Rainbow)**: 建立多重同心圆环带（Band Width）的随机分布函数。
* **云朵 (Sunset)**: 基于五圆堆叠（Five-Blob Stacking）算法实现的具象化图形。

---

## 3. 运行环境与安装 (Deployment Guide)

### 3.1 环境要求
* 现代浏览器 (Chrome, Edge, Firefox, Safari)
* 支持 HTML5 Canvas 2D Context

### 3.2 快速启动
```bash
# 1. 克隆本项目
git clone [https://github.com/QianShark/love_code.git](https://github.com/QianShark/love_code.git)

# 2. 进入目录
cd love_code

# 3. 运行项目
# 直接在浏览器中打开 memory.html 即可