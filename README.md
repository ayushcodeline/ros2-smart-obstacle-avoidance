![ROS2](https://img.shields.io/badge/ROS2-Humble-blue)
![Python](https://img.shields.io/badge/Python-3.10-yellow)
![Gazebo](https://img.shields.io/badge/Simulation-Gazebo-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)
ROS 2 Obstacle Avoidance (TurtleBot3)
Overview: An autonomous navigation project using ROS 2 Humble and Gazebo to detect and avoid obstacles in real-time.

DATA FLOW
LiDAR (/scan) → Logic Node → Velocity (/cmd_vel)

🛠️ Tech Stack
-OS/Framework: Ubuntu 22.04, ROS 2 Humble
-Simulation: Gazebo
-Hardware/Interface: TurtleBot3, Python (rclpy)

⚙️ How it Works
1.Subscribe: Listens to /scan for LiDAR laser distance data.
2.Process: Logic determines the distance to obstacles ahead.
3.Act: Publishes linear/angular velocity to /cmd_vel to move or turn the robot.

## 📂 Package Structure
obstacle_avoidance/
├── obstacle_avoidance/
│ ├── obstacle_avoidance_node.py
│ ├── init.py
├── package.xml
├── setup.py
├── README.md


---

## ▶️ How To Run

### 1️⃣ Source ROS 2

source /opt/ros/humble/setup.bash


### 2️⃣ Set TurtleBot Model

export TURTLEBOT3_MODEL=burger


### 3️⃣ Launch Gazebo

ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py


### 4️⃣ Build Workspace

cd ~/ros2_ws
colcon build
source install/setup.bash


### 5️⃣ Run Node

ros2 run obstacle_avoidance obstacle_avoidance


---

## 🎯 Output

- Robot moves forward
- Detects obstacles
- Turns automatically
- Fully autonomous reactive navigation

---

## 🔥 Future Improvements

- Add smarter left/right detection
- Implement PID control
- Add wall-following
- Integrate Nav2 stack

---

## 👨‍💻 Author

Ayush Yalasangi  
