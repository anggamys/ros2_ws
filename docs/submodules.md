# Adding a New Submodule

## Overview

This guide explains how to add and develop new packages as Git submodules within a ROS 2 Humble workspace.

### Adding a Package as a Submodule from Scratch

To create a new ROS 2 package and include it as a Git submodule in your workspace, follow these steps:

1. Navigate to the `src` directory of your ROS 2 workspace:

   ```bash
   cd ~/ros2_ws/src
   ```

2. Create a new package using the appropriate ROS 2 command.  
   For details, refer to [docs/usage.md](docs/usage.md).

3. Initialize the new package as a Git repository and push it to GitHub:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <repository-url>
   git push -u origin main
   ```

   > Replace `<repository-url>` with the URL of your GitHub repository.

4. Remove the package from the current workspace (cached only) and re-add it as a Git submodule:

   ```bash
   git rm -r --cached <package_name>
   git submodule add <repository-url> <package_name>
   ```

   > Replace `<repository-url>` with the GitHub repository URL and `<package_name>` with your package directory name.
