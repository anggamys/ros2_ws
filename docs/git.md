# Adding a New Submodule

## Overview

This document provides instructions on how to add a new submodule from GitHub or from new local directories to the ROS 2 workspace. Submodules are useful for managing dependencies or including external repositories within your workspace.

## Adding a Submodule from GitHub

1. Navigate to the root of your ROS 2 workspace:

   ```bash
   cd ros2_ws/src
   ```

2. Use the following command to add a new submodule:

   ```bash
   git submodule add <repository-url> <package_name>
   ```

   > Replace `<repository-url>` with the URL of the GitHub repository you want to add, and `<package_name>` with the desired name for the package.

3. After adding the submodule, initialize and update it:

   ```bash
   git submodule update --init --recursive
   ```

4. Commit the changes to your workspace:

   ```bash
   git commit -m "Add submodule <package_name>"
   ```

5. Push the changes to your remote repository:

   ```bash
   git push origin main
   ```

## Adding a Submodule from a Local Directory

1. Navigate to the root of your ROS 2 workspace:

   ```bash
   cd ros2_ws/src
   ```

2. You can use a ready directory package or create a new one. If you have a ready directory package, you can continue with the following steps.

3. Create a new repository from your GitHub account.
4. Initialize the new repository in your local directory:

   ```bash
   git init
   ```

   > Follow the instructions on GitHub to push your local repository to the remote repository.

5. After initializing the repository, and successfully pushing it to GitHub, you can add it as a submodule in your ROS 2 workspace.

6. Remove the existing package directory if it exists and cache git:

   ```bash
   rm -rf <package_name>
   git rm --cached <package_name>
   ```

   > Replace `<package_name>` with the name of the package you want to add.

7. Add the new submodule:

   ```bash
   git submodule add <repository-url> <package_name>
   ```

   > Replace `<repository-url>` with the URL of the newly created GitHub repository.

8. Initialize and update the submodule:

   ```bash
   git submodule update --init --recursive
   ```

9. Commit the changes to your workspace:

   ```bash
   git commit -m "Add submodule <package_name>"
   ```

10. Push the changes to your remote repository:

    ```bash
    git push origin main
    ```

## Notes

- Ensure that the submodule repository is public or that you have the necessary permissions to access it.
- If you encounter any issues with submodule initialization, you can try running `git submodule
update --init --recursive` again.
- When working with submodules, remember that they are separate repositories. You may need to manage them independently, including updating and committing changes within the submodule itself.
