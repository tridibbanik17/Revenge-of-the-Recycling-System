<div align="center">

<h3 align="center">Revenge of the Recycling System</h3>

  <p align="center">
    Controls a Q-Arm and Q-Bot to sort and recycle containers in a simulated environment.
    <br />
     <a href="https://github.com/tridibbanik17/revenge-of-the-recycling-system">GitHub Repository</a><br>
     <a href="https://www.notion.so/Project-3-Revenge-of-the-Recycling-System-ff665bba9f1842199a552db23e39da63?pvs=4" target="_blank">Project Objectives, Contributions, and Reflection.</a>
  </p>
</div>


<div align="center">
  
_[Watch the video on how Q-Arm transfers a container from the servo table to Q-bot's hopper.](./ServoTable_to_Hopper.mp4)_

_[Watch the video on the deposit process of containers after the target bin color is detected by the color sensor.](./DepositContainers_to_TargetBin.mp4)_

_[Watch the video on the Q-bot following a yellow line using Infrared sensors.](./Q-Bot_Movements_using_IR_sensors.mp4)_

</div>

## Table of Contents

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#key-features">Key Features</a></li>
      </ul>
    </li>
    <li><a href="#architecture">Architecture</a></li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

This Python program simulates a recycling system using a Q-Arm and a Q-Bot within the Quanser Interactive Labs environment. The Q-Arm sorts containers based on their mass, material, and destination, while the Q-Bot transports and deposits them into designated recycling bins. The system operates in cycles, with the Q-Arm loading containers onto the Q-Bot until its hopper is full or a different type of container is detected. The Q-Bot then follows a yellow line to the appropriate bin and deposits the containers.

### Key Features

- **Automated Sorting:** The Q-Arm automatically sorts containers based on predefined criteria.
- **Autonomous Navigation:** The Q-Bot autonomously navigates using IR sensors to follow a yellow line.
- **Color-Based Bin Identification:** The Q-Bot uses color sensors to identify the correct recycling bin.
- **Simulated Environment:** The system operates within the Quanser Interactive Labs virtual environment.
- **Configurable Parameters:** Allows customization of servo table angles, bin configurations, and robot speeds.

## Architecture

The project utilizes the `Common.simulation_project_library` to interface with the Quanser Interactive Labs environment. The `main.py` script orchestrates the interaction between the Q-Arm, servo table, and Q-Bot.

- **Q-Arm:** Responsible for picking and placing containers based on their attributes.
- **Servo Table:** Dispenses containers for the Q-Arm to process.
- **Q-Bot:** Transports containers to the appropriate recycling bins using line following and color sensing.

### List of container attributes is given below:
| ID | Q-Lab Render | Material | Contamination | Recyclability  | Mass (g) | Target Bin    |
| -- | ------------ | -------- | ------------- | -------------- | -------- | ------------- |
| 01 | White bottle | Plastic  | Clean         | Recyclable     | \~9.25   | Bin03 (Blue)  |
| 02 | Red can      | Metal    | Clean         | Recyclable     | \~15.0   | Bin01 (Red)   |
| 03 | Blue bottle  | Paper    | Clean         | Recyclable     | \~10.0   | Bin02 (Green) |
| 04 | White bottle | Plastic  | Dirty         | Non-Recyclable | > 9.25   | Bin04 (White) |
| 05 | Red can      | Metal    | Dirty         | Recyclable     | > 15.0   | Bin01 (Red)   |
| 06 | Blue bottle  | Paper    | Dirty         | Non-Recyclable | > 10.0   | Bin04 (White) |

### Video Demonstration
Below is a video demonstration of the Quanser Virtual Simulation using Q-Bot and Q-Arm.

[![Virtual Simulation Using Q-Bot and Q-Arm](https://img.youtube.com/vi/XYgK-refaHk/0.jpg)](https://www.youtube.com/watch?v=XYgK-refaHk)
Click the thumbnail to watch the video on YouTube.

## Getting Started

### Prerequisites

- Python 3.x
- Quanser Interactive Labs
- `Common.simulation_project_library` (Ensure this is in the parent directory as indicated by `sys.path.append('../')`)

### Installation

1.  Clone the repository:
   ```sh
   git clone https://github.com/tridibbanik17/revenge-of-the-recycling-system.git
   cd revenge-of-the-recycling-system
   ```
2.  Ensure that the `Common.simulation_project_library` is accessible in the parent directory.
3.  Configure the `ip_address` and `project_identifier` variables in `main.py` to match your Quanser Interactive Labs setup.
4.  Adjust servo table and bin configurations in `main.py` as needed.
5.  Run the `main.py` script:
   ```sh
   python main.py
   ```

## Acknowledgments

- This README was created using [gitreadme.dev](https://gitreadme.dev) — an AI tool that looks at your entire codebase to instantly generate high-quality README files.
- Quanser Interactive Labs for providing the simulation environment and necessary libraries.
