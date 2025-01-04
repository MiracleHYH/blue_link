# BlueLink

`BlueLink` 是一个基于 Flutter 开发的移动应用，旨在通过蓝牙连接和管理中枢设备（HUB）与终端设备（Sensor），实现设备配对、实时数据查看和管理功能。

---

## 功能特性

### 1. 蓝牙设备连接与管理

- **设备配对**：通过蓝牙 MAC 地址完成中枢设备与终端设备的配对。
- **实时数据查看**：
    - 中枢设备页面：查看已绑定的终端设备列表（如蓝牙 MAC、设备型号、设备名称等）。
    - 终端设备页面：实时查看传感器数据（如加速度、海拔、温度等）。

### 2. 动态蓝牙设备展示

- 首页自动扫描周围符合 `MLC` 前缀的蓝牙设备，并区分中枢设备和终端设备。

### 3. 二维码扫描支持

- 通过扫描设备二维码快速获取蓝牙 MAC 地址和设备型号，便于精确连接设备。

### 4. 多级蓝牙连接管理

- 支持中枢设备与终端设备的分级连接：
    - 中枢设备（HUB）：管理与多台终端设备的通信。
    - 终端设备（Sensor）：通过中枢设备进行间接连接，或直接连接用于设置与调试。

---

## 下载与安装

请根据您的设备架构选择合适的 APK 文件，或直接下载通用版本。

| 文件名                         | 适用架构       | 文件大小    | 下载链接                                                                                               |
|-----------------------------|------------|---------|----------------------------------------------------------------------------------------------------|
| app-arm64-v8a-release.apk   | ARM 64-bit | 12.9 MB | [下载](https://github.com/MiracleHYH/blue_link/releases/download/latest/app-arm64-v8a-release.apk)   |
| app-armeabi-v7a-release.apk | ARM 32-bit | 12.1 MB | [下载](https://github.com/MiracleHYH/blue_link/releases/download/latest/app-armeabi-v7a-release.apk) |
| app-x86_64-release.apk      | x86 64-bit | 13.4 MB | [下载](https://github.com/MiracleHYH/blue_link/releases/download/latest/app-x86_64-release.apk)      |
| **app-release.apk**         | **通用版本**   | 32.9 MB | [下载](https://github.com/MiracleHYH/blue_link/releases/download/latest/app-release.apk)             |

安装完成后，即可体验 `BlueLink` 的全部功能！

---

## 使用指南

### 1. 首页功能

- 自动扫描附近蓝牙设备，展示符合 `MLC` 前缀的设备列表。
- 支持通过浮动按钮扫描二维码快速获取设备信息。

### 2. 中枢设备（HUB）页面

- 蓝牙连接选定的中枢设备。
- 显示该中枢设备已绑定的终端设备列表，包括设备型号、序列号、蓝牙 MAC 地址等信息。

### 3. 终端设备（Sensor）页面

- 在保持中枢设备连接的同时，连接选定的终端设备。
- 查看实时数据并支持相关设置功能。

---

## 技术细节

- **开发框架**：Flutter
- **核心依赖**：
    - [`flutter_blue_plus`](https://pub.dev/packages/flutter_blue_plus)：用于蓝牙扫描、连接与通信。
    - [`mobile_scanner`](https://pub.dev/packages/mobile_scanner)：用于二维码扫描。
- **最低支持 Android 版本**：Android 5.0

---

## 联系我们

如有任何问题或建议，请通过 [Issues](https://github.com/MiracleHYH/blue_link/issues) 提交反馈。

感谢您的支持！✨