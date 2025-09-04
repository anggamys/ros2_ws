# ROS 2 Workspace

## Overview

This is a ROS 2 workspace that contains various packages and configurations for building and running ROS 2 applications.

This workspace is used for testing and development purposes. It includes packages for different functionalities, such as navigation, perception, and control.

You can see this specific workspace documentation in the [workspace documentation](docs/).

## How to Use

Pre-requisites:

- Ensure you have ROS 2 installed on your system. For installation instructions, refer to the [ROS 2 Installation Guide](https://docs.ros.org/en/humble/Installation.html).
- Make sure you have the necessary dependencies installed.

### Cloning the Workspace

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/anggamys/ros2_ws.git
   ```

2. Navigate to the workspace directory:

   ```bash
   cd ros2_ws
   ```

   > You need add the submodules to your workspace. If you have cloned the repository without submodules, you can add them by running:

   ```bash
   git submodule update --init --recursive
   ```

### Building the Workspace

For official build instructions, refer to the [ROS 2 Build Documentation](https://docs.ros.org/en/humble/Tutorials/Beginner-Client-Libraries/Colcon-Tutorial.html).

1. Install the necessary dependencies:

   ```bash
   sudo apt update
   sudo apt install -y python3-colcon-common-extensions
   ```

2. Build the workspace:

   ```bash
   colcon build --symlink-install
   ```

   > You can build specific packages by specifying their names:

   ```bash
   colcon build --symlink-install --packages-select <package_name>
   ```

   > Replace `<package_name>` with the name of the package you want to build.

3. Source the setup script:

   ```bash
   source install/setup.bash
   ```

### Running the Packages

For running the packages, refer to the individual package documentation. Generally, you can run a package using:

```bash
ros2 run <package_name> <executable_name>
```
