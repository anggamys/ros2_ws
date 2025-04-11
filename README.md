# Personal ROS 2 Workspace

## Overview

Repository ini merupakan workspace pribadi ROS 2 Humble yang berisi berbagai package dan konfigurasi untuk pengembangan sistem berbasis ROS 2.

## Installation

1. Clone repository:

   ```bash
   git clone https://github.com/anggamys/ros2_ws.git
   ```

2. Inisialisasi submodule:

   ```bash
   git submodule update --init --recursive
   ```

3. Install dependency:

   ```bash
   rosdep install -i --from-path src --rosdistro humble -y
   ```

## Usage

Untuk panduan lengkap penggunaan dan pengembangan package, lihat [usage.md](usage.md).

### 1. Build workspace

```bash
colcon build
```

### 2. Source workspace

```bash
source install/setup.bash
```

### 3. Jalankan node

```bash
ros2 run package_name node_name
```

> Ganti `package_name` dan `node_name` dengan nama package dan node yang ingin dijalankan.
