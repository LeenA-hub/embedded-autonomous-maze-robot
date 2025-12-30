# embedded-autonomous-maze-robot

## Project Overview
This project is an embedded systems robot that can autonomously follow a line, navigate through a maze, learn the correct path, and successfully retrace its route back to the starting point.

Once the robot is started, it operates entirely on its own. It uses onboard sensors to detect lines, intersections, and obstacles, and makes real-time decisions based on its environment without any human control.

A demo video is included showing the robot completing the maze from start to finish.

ffmpeg -i "IMG_9043 (1).mp4" -vf scale=480:-2 -an -b:v 400k -preset ultrafast output_under_10mb.mp4


## What the Robot Does
- Follows a guidance line using line sensors
- Detects intersections and junctions in the maze
- Makes decisions at each intersection
- Detects dead ends using bumper switches
- Turns around and recovers from incorrect paths
- Stores correct path decisions in memory
- Uses stored decisions to navigate the maze in reverse
- Completes the maze autonomously once activated

## How It Works
The robot continuously reads data from its line sensors to stay aligned with the path.  
When it reaches an intersection, it chooses a direction and continues forward.

If the robot encounters a dead end, the front bumper is triggered. The robot then:
1. Stops and performs a 180° turn
2. Retraces its path to the previous intersection
3. Selects the alternate direction
4. Stores the correct decision in memory

Once the robot reaches the final destination, it reverses direction and uses the stored path decisions to navigate back through the maze without errors.

The navigation logic is implemented using a state machine, allowing the robot to respond reliably to sensor input in real time.

## Hardware and Technologies
- HCS12 Microcontroller
- Assembly Language
- Line-following sensors (photodetectors)
- DC motors and motor driver circuitry
- Front and rear bumper switches
- Embedded state machine control logic

## Demo
🎥 A video demonstration is included that shows:
- Line following behavior
- Intersection handling
- Dead-end detection and recovery
- Full maze completion and return path

## What This Project Demonstrates
- Embedded systems programming
- Low-level hardware interaction
- Sensor-based decision making
- State machines and control logic
- Autonomous system design
- Debugging and iterative development

## Possible Improvements
- Faster path optimization after learning
- Smoother motor control
- Improved sensor filtering
- Support for larger or more complex mazes


