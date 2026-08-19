# AprilTag & ArUco Print Studio

> **Precision Visual Fiducial Marker Generator & Scaled 1:1 PDF Print Sheet Studio for Robotics, SLAM, and Computer Vision.**

---

## 🎯 为什么做这个产品（软柿子打法）？

在机器人（ROS/ROS2）、无人机视觉降落、SLAM 建图、相机标定和高校实验室中，每周都有大量研究员和工程师搜索打印 **AprilTag**（tag36h11 等）和 **ArUco** 标定板。

目前搜索排名前列的工具（如部分 github.io 上的静态单页）存在严重缺陷：
1. **只能单张生成粗糙图片**，无法一页排版多个标签；
2. **缺乏物理尺寸标定**：用户打印出来的标签尺寸不准，导致机器人 3D 深度测距产生严重误差；
3. **无裁切线与标尺**：缺少 100mm 校验尺和辅助十字线；
4. **无一键代码导出**：没有对应的 OpenCV / ROS2 读取代码。

**AprilTag Print Studio** 纯前端 100% 矢量实现，零云端成本，秒开离线可用，彻底碾压同类工具体验。

---

## 🚀 核心功能亮点

- **全系列字典支持**：
  - **AprilTag**: tag36h11 (587 tags, 机器人标准), tag25h9, tag16h5, tagCircle21h7, tagStandard41h12
  - **ArUco**: 4x4, 5x5, 6x6, 7x7 (50 ~ 1000 IDs) 及 ArUco Original (1024 IDs)
- **100% 物理毫米实尺打印**：输入 50mm 即生成严格 50.0mm 矢量 PDF，绝无缩放失真。
- **A4 / A3 / US Letter 多标签拼版**：单页自动排版 4 / 6 / 12 / 24 个标签，带虚线裁切线。
- **100mm 校验标尺**：每张打印纸顶部内置 100mm 实物校准尺，杜绝“适合页面”缩放陷阱。
- **屏幕 1:1 比例尺校准**：通过银行卡/身份证校准屏幕 DPI，在显示器上 1:1 预览实际大小。
- **ROS 2 & OpenCV 代码生成器**：实时生成 Python / C++ 检测代码。
- **100% 本地隐私与 PWA 离线支持**：无需网络，野外/无网实验室均可稳定使用。

---

## 📦 免费部署指南（0 成本）

### 方案 A：Cloudflare Pages（推荐，国内访问极快）
1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/) -> **Workers & Pages** -> **Create application** -> **Pages**。
2. 选择 **Direct Upload**（直接上传）或连接你的 GitHub 仓库。
3. 上传 outputs 文件夹内的所有文件（或将整个仓库部署）。
4. 获得永久免费二级域名：https://apriltag-studio.pages.dev/。

### 方案 B：GitHub Pages
1. 创建 GitHub 仓库 apriltag-print-studio。
2. 将 outputs 内的文件 push 到仓库根目录。
3. 仓库 **Settings** -> **Pages** -> Branch 选择 main / root -> Save。
4. 获得免费站点：https://username.github.io/apriltag-print-studio/。
