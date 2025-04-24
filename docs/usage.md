# Documentation

## Overview

This guide provides instructions for using and developing ROS 2 Humble packages within an existing workspace.

Official reference: [https://docs.ros.org/en/humble/](https://docs.ros.org/en/humble/)

## Package Development

### Creating a New Package

Navigate to the `src` directory of your workspace:

```bash
cd ~/ros2_ws/src
```

#### Python Package

To create a Python-based package:

```bash
ros2 pkg create --build-type ament_python --license Apache-2.0 <package_name>
```

#### C++ Package

To create a C++-based package:

```bash
ros2 pkg create --build-type ament_cmake --license Apache-2.0 <package_name>
```

> Replace `<package_name>` with your desired package name.

## Building the Workspace

To build the entire workspace:

```bash
colcon build
```

To build a specific package only:

```bash
colcon build --packages-select <package_name>
```

> Replace `<package_name>` with the name of the package you want to build.
