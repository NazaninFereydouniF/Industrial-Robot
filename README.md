# 🤖 Industrial Robot — OOP in Python
> A clean, beginner-friendly simulation of an Industrial Welding Robot with **Composition** and **Dependency Injection**.
![Python](https://img.shields.io/badge/Python-3.13-blue?style=flat-square&logo=python) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square&logo=jupyter) ![OOP](https://img.shields.io/badge/Paradigm-OOP-green?style=flat-square) ![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square) ![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)
---
## 📖 Overview
This project simulates a simple **Industrial Robot** with a rotating `Body` and a movable `Arm`.
It demonstrates two key OOP designs in Python:
1. **Composition** — `IndustrialRobot` creates its own `Body` and `Arm`
2. **Dependency Injection** — `Body` and `Arm` are injected from outside
Perfect for learning **classes, encapsulation, and composition**.
---
## ✨ Features
- 🔄 Rotate body left / right with custom degrees
- 🦾 Move arm up / down with custom distance (cm)
- 🔥 Simulate welding operation
- 🧱 Track state: `rotation` and `position`
- 🧩 Two designs: Composition vs. Injection
- 📓 Interactive Jupyter Notebook demo
---
## 🗂️ Project Structure
```text
industrial-robot/
├── Industrial Robot.ipynb  # Main notebook + demo
├── README.md               # Documentation
└── LICENSE                 # MIT License
```
---
## ⚙️ Classes
| Class | Responsibility | Attributes | Methods |
|-------|----------------|------------|---------|
| `IndustrialRobot` | Facade controller | `body`, `arm` | `rotate_body_left()`, `rotate_body_right()`, `move_arm_up()`, `move_arm_down()`, `weld()` |
| `Body` | Rotation logic | `rotation` | `rotate_left()`, `rotate_right()` |
| `Arm` | Movement + welding | `position` | `move_up()`, `move_down()`, `weld()` |
---
## 🚀 Getting Started
**Requirements:** Python `3.10+` + Jupyter / VS Code
```bash
git clone https://github.com/NazaninFereydouniF/Industrial-Robot
cd industrial-robot
jupyter notebook "Industrial Robot.ipynb"
```
---
## 💡 Usage Example
```python
robot = IndustrialRobot()
robot.rotate_body_left()
robot.move_arm_up(15)
robot.move_arm_up(15)
robot.rotate_body_right(20)
robot.move_arm_down(5)
robot.weld()
print(robot.body.rotation)  # 10
print(robot.arm.position)   # 25
```
**Output:**
```text
Rotating body 10 degress to the left...
Moving arm 15 cm up...
Moving arm 15 cm up...
Rotating body 20 degress to the right...
Moving arm 5 cm down...
Welding...
```
---
## 🧠 OOP Concepts
- `class` and `__init__` constructors
- Encapsulation of state and behavior
- **Composition:** Robot *has-a* Body and Arm
- **Injection:** `IndustrialRobot(body, arm)` for testability
- Introspection with `vars(robot)`
---
## 🛣️ Roadmap
- [ ] Add `Gripper` class
- [ ] Add limits and validation
- [ ] Add `pytest` tests
- [ ] Convert to `robot.py` module
---
## 🤝 Contributing
Fork the repo, open an issue or submit a pull request — contributions welcome!
---
## 📄 License
Distributed under the **MIT License**. See `LICENSE` for details.
---
⭐ If this helped you learn OOP, please give it a star!
