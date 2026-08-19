# AprilTag & ArUco Print Studio — DESIGN.md

## 1. 设计读取 (Design Read)

> **读取为**：工业/科研级视觉标定工程工具（Web Studio），面向机器人算法工程师、SLAM/无人机研究员与高校视觉实验室，用**精密航电/深空遥测（Precision Avionics / Dark Telemetry）**视觉语言，倾向 Linear/Raycast 式极简暗色工程设计系统。

---

## 2. 拨盘设定 (Dial Settings)

| 拨盘参数 | 数值 | 中文人话解释 |
|---|---|---|
| **VARIANCE (视觉冒险度)** | **6 / 10** | 航电精密仪器感、仪表盘式紧凑网格布局，打破常规表单模板，但不做浮夸非对称，确保严谨度。 |
| **MOTION (动效强度)** | **5 / 10** | 刻度平滑吸附、状态呼吸指示灯、参数联动微弹动，拒绝拖沓动画，保证高响应性。 |
| **DENSITY (信息密度)** | **7 / 10** | 驾驶舱级数据排布，参数、矩阵、实时预览与代码同屏联动，层级分明。 |

---

## 3. 色彩与材质规范 (Color & Material System)

### 3.1 主题色彩（深空遥测系）
- **Background Dark**: `#070a12` (深空黑曜石底色)
- **Surface Panel**: `#0e1424` (仪表控制台面板底色)
- **Border & Grid**: `#1e293b` / `rgba(255, 255, 255, 0.07)` (极细精密坐标网格)
- **Primary Telemetry Accent**: `#10b981` (遥测荧光绿 — 代表数据有效与校验通过)
- **Secondary Tactical Accent**: `#06b6d4` (战术青蓝 — 代表光学参数与坐标轴)
- **Warning / Attention**: `#f59e0b` (精密琥珀黄 — 提示缩放与打印警告)

### 3.2 字体排印
- **UI 界面字体**: `Inter, system-ui, -apple-system, sans-serif`
- **数据/参数/代码字体**: `JetBrains Mono, SF Mono, Menlo, monospace`

---

## 4. 关键组件工艺

1. **Virtual Print Canvas (虚拟印务台)**:
   - 拟真 A4/A3/Letter 纸张白底投影，配备暗色标尺与 100mm 实物校准条。
   - 网格动态排版，自动计算裁切线（Scissor Guides）与角点十字瞄准标（Crosshairs）。
2. **Real-World Screen Scale Calibrator (屏幕实物校准器)**:
   - 仿真标准银行卡（85.60 mm）比例滑块，毫秒级动态换算物理 DPI，实现显示器 1:1 像素映射。
3. **Code Telemetry Console (代码遥测控制台)**:
   - 实时根据所选 Tag ID、字典与毫米尺寸同步生成 Python/OpenCV/ROS2 驱动配置。
