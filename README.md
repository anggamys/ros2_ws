# Personal ROS 2 Workspace

## Overview

This repository is a personal ROS 2 Humble workspace that contains various packages and configurations used for developing ROS 2-based systems.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/anggamys/ros2_ws.git
   ```

2. Initialize submodules:

   ```bash
   git submodule update --init --recursive
   ```

3. Install dependencies:

   ```bash
   rosdep install -i --from-path src --rosdistro humble -y
   ```

## Usage

For detailed usage instructions and package development guides, refer to [docs/usage.md](docs/usage.md).

### 1. Build the workspace

```bash
colcon build
```

### 2. Source the workspace

```bash
source install/setup.bash
```

### 3. Run a node

```bash
ros2 run <package_name> <node_name>
```

> Replace `<package_name>` and `<node_name>` with the desired package and node name.
