# The UnderScanner
## Quick Intro
Welcome to my personal project: building a **handheld LiDAR scanner**!  
This system is designed primarily for **mapping caves** and combines advanced hardware, real-time SLAM algorithms, and a custom mobile app for remote control and visualization.
Though my goal is to map caves it can also map **any human size environment**.

**So far**, I have assembled the hardware, installed the OS, set up the middleware (ROS), installed the necessary drivers, and configured the system.
For development purposes, I currently have a mouse, keyboard, and screen connected to the Jetson so I can manually launch, stop, and save scans.
When I start a scan, it runs a SLAM algorithm and opens an RViz window to visualize the map as it’s being created.

**The final goal** is to map caves, so I eventually need to eliminate the mouse, keyboard, and screen.
Since carrying my phone during cave explorations is no big deal, I decided to control the scanner using an Android app.
I already started developing the app, and several features are working:

  - It can connect to a Flask server running on the SBC.

  - It can download scan files (.pcd) from the SBC to the phone.

  - It can visualize the point clouds in a custom 3D viewer built into the app.

This basic system is working.
Now, I want to implement real-time visualization of the scanning process in the app.


## 🚀 Project Overview
### Scanner Unit
- **LiDAR Sensor:** Livox Mid-360
- **Processing Unit:** Jetson Orin Nano Developer Kit
- **Middleware:** ROS (Robot Operating System)

The system captures 3D point cloud data in real time, runs SLAM algorithms to create maps on the fly.

---

🛠 Current Progress:

✅ **Hardware Assembly**  
✅ **Operating System Installation**  
✅ **Middleware (ROS) Setup**  
✅ **Driver Installation**  
✅ **System Configuration**  

For development, a mouse, keyboard, and monitor are connected to the SBC. Scans are manually started, stopped, and saved through this setup.

When a scan is active:

- A SLAM algorithm runs in real-time.
- RViz visualizes the evolving map.

---

### 📱 Mobile App

Since traditional input devices are impractical during cave explorations, I am developing a **custom Android app** to remotely control the scanner.

🛠 Current mobile app features:

- 📡 **Connects** to a Flask server running on the Jetson.
- 📥 **Downloads** completed scan files (`.pcd`) directly to the phone.
- 🛰 **Visualizes** point clouds in a **custom 3D viewer** inside the app.

---

## 🔮 Next Steps

- 🖼 **Implement real-time visualization** of the scan progress directly in the mobile app.
- 📶 **Enhance** wireless stability and latency for smoother remote control.
- Add a **battery** to make it portable ans start to scan bigger areas
- **Implement** RTAB-Map for bigger scans

---

## 🌌 Final Goal

> **Create a fully portable handheld LiDAR system for cave mapping**, controlled entirely via a smartphone.
> **Implement different post processing pipelines**:
  - point cloud -> surfaces
  - point cloud warp with existing 2D maps
> **Enhance visualisation**, add sensor path and others

---

## 📸 Sneak Peek

Check my [Instagram profile](https://www.instagram.com/3d_slam/)

---

## 🧠 Technologies Used

- ROS (Robot Operating System)
- Flask (for server communication)
- Android (Kotlin/Java) Mobile Development
- Livox SDK
- RViz for visualization directly on SBC
- OpenGL for visualization on Android App
- SLAM algo [Add github link]

---

## 🤝 Contributions

This is a personal project, but I’m always open to advice, code reviews, or collaboration ideas! Feel free to reach out.

---

## 📬 Contact

If you're interested in this project or have any questions, feel free to reach out!


Made with ❤️ by Théotime Dmitrašinović
