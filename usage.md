# Documentation

## Overview

Panduan ini menjelaskan cara menggunakan dan mengembangkan package ROS 2 Humble di dalam workspace yang tersedia.

Referensi resmi: [https://docs.ros.org/en/humble/](https://docs.ros.org/en/humble/)

---

## Package Development

### Membuat Package Baru

Masuk ke folder `src`:

```bash
cd ~/ros2_ws/src
```

#### Python Package

```bash
ros2 pkg create --build-type ament_python --license Apache-2.0 package_name
```

#### C++ Package

```bash
ros2 pkg create --build-type ament_cmake --license Apache-2.0 package_name
```

> Ganti `package_name` dengan nama package yang diinginkan.

---

## Build Workspace

Build seluruh workspace:

```bash
colcon build
```

Build package tertentu saja:

```bash
colcon build --packages-select package_name
```

> Ganti `package_name` dengan nama package yang ingin dibuild.
