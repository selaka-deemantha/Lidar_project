
# 3D Lidar Scanner
<div align="center">

# 3D LiDAR Scanner

**A cost-effective, single-motor 3D LiDAR scanner for generating high-resolution spiral point clouds.**

</div>

![Lidar Scanner](Notes/full.png)

---

## 📖 Overview

This project presents a groundbreaking 3D LiDAR scanner designed to offer a cost-effective solution for generating high-resolution point clouds using a single laser module. Utilizing a TF Mini-S laser module, our scanner implements a distinctive cylindrical cam mechanism, which allows it to achieve both horizontal and vertical scanning movements with only one stepper motor. This innovative design produces a spiral-shaped point cloud, providing an affordable alternative to traditional industrial LiDAR systems, which are often expensive and complex. The system features a custom-designed PCB incorporating an AVR microcontroller and an A4988 motor controller, ensuring precise control over the stepper motor. Although the scanner operates at a slower speed compared to industrial counterparts, it significantly reduces costs and makes advanced 3D scanning accessible for students, researchers, and enthusiasts. Comprehensive documentation, including SolidWorks designs, PCB schematics, and source code, is provided to facilitate further development and customization. We are also planning to develop a software interface that will enable users to adjust scanning speed, resolution, and visualize the point clouds in real-time, enhancing the overall functionality and usability of the scanner.

## ✨ Key Features

- **Low-Cost Design**: Built with affordable and readily available components.
- **Single-Motor Operation**: An innovative cylindrical cam mechanism drives both horizontal and vertical motion with one stepper motor.
- **Spiral Scanning**: Generates a unique spiral point cloud to capture 3D data.
- **Custom PCB**: A dedicated PCB with an ATmega328P microcontroller for robust and reliable control.
- **Open Source**: All design files, schematics, and source code are provided for further development and customization.

## ⚙️ How It Works

The scanner's core is the cylindrical cam mechanism. As the stepper motor rotates the main body horizontally, the cam follower moves along the groove of the stationary cylindrical cam. This groove is designed to guide the LiDAR sensor vertically, tilting it up and down. The combination of continuous horizontal rotation and controlled vertical tilting results in a spiral scanning path, allowing the single laser module to capture a full 3D environment.

The ATmega328P microcontroller executes a control loop that:
1.  Manages the stepper motor's acceleration, constant velocity, and deceleration phases for smooth rotation.
2.  Reads distance data from the TF Mini-S LiDAR sensor via UART.
3.  Transmits the processed distance data to a computer for visualization and storage.

![Exploded View](Notes/full_inside.png)

## 🛠️ Hardware

### Components
- **LiDAR Sensor**: TF Mini-S
- **Microcontroller**: ATmega328P
- **Motor Driver**: A4988 Stepper Motor Driver
- **Motor**: NEMA 17 Stepper Motor (or similar)
- **Serial Communication**: FT232RL USB to TTL Serial Adapter
- **Custom PCB**: See the `PCB/` directory for Eagle/KiCad files.

!PCB

## 🚀 Future Development

We are planning to develop a software interface (e.g., using Python or Processing) that will enable users to:
- Adjust scanning speed and resolution.
- Visualize the point cloud in real-time.
- Export the point cloud data in standard formats (e.g., .ply, .xyz).

## 🤝 Contributors

- Dineth Perera
- Seleka Deemantha

## 📄 License

This project is open-source. We encourage you to use, modify, and share it. Consider adding a license file (e.g., MIT, Apache 2.0) to define the terms of use.
