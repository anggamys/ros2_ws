# Dokumentasi ROS

## Deskripsi

## Instalasi

### Projek baru (Package baru)

1. Masuk ke folder workspace

   ```bash
   cd ~/ros2_ws/src
   ```

2. Buat package baru

   Untuk membuat package baru dengan menggunakan ament_cmake (C++), gunakan perintah berikut:

   ```bash
   ros2 pkg create --build-type ament_cmake --license Apache-2.0 <package_name>
   ```

   > Gantilah `<package_name>` dengan nama package yang diinginkan.

   Untuk membuat package baru dengan menggunakan ament_python (Python), gunakan perintah berikut:

   ```bash
   ros2 pkg create --build-type ament_python --license Apache-2.0 <package_name>
   ```

   > Gantilah `<package_name>` dengan nama package yang diinginkan.

3. Build package

   Jika package sudah dibuat, kita perlu membangun package tersebut agar dapat digunakan. Gunakan perintah berikut untuk membangun package.

   Build semua package yang ada di dalam workspace:

   ```bash
   colcon build
   ```

   Build package tertentu:

   ```bash
   colcon build --packages-select <package_name>
   ```

   > Gantilah `<package_name>` dengan nama package yang ingin dibangun.
   > Pastikan untuk menjalankan perintah ini di dalam folder workspace (misalnya `~/ros2_ws`).
