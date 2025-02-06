# Installing ROS Noetic and ROS2 Humble with Documentation on GitHub

## 1. Installing ROS Noetic

### **Prerequisites**
Before installing ROS Noetic, ensure you have Ubuntu 20.04.

### **Steps**
1. **Add ROS GPG keys:**
   ```bash
   sudo apt update
   sudo apt install curl
   curl -sSL 'http://repo.ros2.org/repos.key' | sudo apt-key add -
   ```

2. **Add ROS repositories:**
   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   ```

3. **Update packages and install ROS Noetic:**
   ```bash
   sudo apt update
   sudo apt install ros-noetic-desktop-full
   ```

4. **Set up ROS environment:**
   ```bash
   echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

5. **Install additional tools:**
   ```bash
   sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
   ```

6. **Initialize rosdep:**
   ```bash
   sudo rosdep init
   rosdep update
   ```

7. **Verify installation:**
   ```bash
   roscore
   ```

---

## 2. Installing ROS2 Humble

### **Prerequisites**
Ensure you have Ubuntu 22.04.

### **Steps**
1. **Add ROS2 GPG keys:**
   ```bash
   sudo apt update && sudo apt install curl -y
   sudo curl -sSL 'http://repo.ros2.org/repos.key' | sudo apt-key add -
   ```

2. **Add ROS2 repositories:**
   ```bash
   sudo sh -c 'echo "deb http://packages.ros.org/ros2/ubuntu $(lsb_release -cs) main" > /etc/apt/sources.list.d/ros2-latest.list'
   ```

3. **Update packages and install ROS2 Humble:**
   ```bash
   sudo apt update
   sudo apt install ros-humble-desktop
   ```

4. **Set up ROS2 environment:**
   ```bash
   echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
   source ~/.bashrc
   ```

5. **Verify installation:**
   ```bash
   ros2 run demo_nodes_cpp talker
   ```
