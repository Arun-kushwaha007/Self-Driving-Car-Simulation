# 📘 Self-Driving Car Simulation

## 🚗 Overview

**Self-Driving Car Simulation** is a browser-based project that demonstrates the fundamentals of neural networks, genetic algorithms, and sensor-based control systems. Built entirely with vanilla JavaScript, it provides an interactive environment where AI-controlled cars learn to navigate roads and avoid obstacles, all visualized in real-time.

---

## 📝 Project Description

This simulation features:
- **AI Cars:** Controlled by a simple feedforward neural network and evolved using a genetic algorithm.
- **Manual Car:** User-controllable for direct comparison and experimentation.
- **Real-Time Visualization:** See sensor data, neural network activity, and car behavior as it happens.

The project is designed as an educational tool to make abstract machine learning concepts tangible and engaging.

---

## 🎯 Features

- **Self-Driving AI:** AI cars learn to drive and avoid collisions.
- **Neural Network Engine:** Custom, dependency-free feedforward neural network.
- **Genetic Algorithm:** Save and mutate the "best" car's brain for evolutionary learning.
- **Real-Time Visualization:** View sensors, road, traffic, and neural network structure/activation.
- **Manual Control:** Drive a car using keyboard arrow keys.
- **Collision Detection:** Polygon-based, efficient and accurate.
- **Local Storage Persistence:** Save and load the best neural network brain.

---

## 🛠️ Tech Stack

- **Languages:** HTML5, CSS3, JavaScript (ES6+)
- **Frameworks/Libraries:** None (vanilla JavaScript)
- **Tools:**
  - HTML5 Canvas for rendering and visualization
  - Browser Local Storage for saving model progress

---

## 📂 Setup & Usage

### Installation

No installation required! The project runs directly in any modern web browser.

1. **Clone the repository:**
   ```sh
   git clone <repository-url>
   ```
2. **Navigate to the project directory:**
   ```sh
   cd <repository-directory>
   ```
3. **Open `index.html` in your browser.**

### Usage Guide

- The simulation starts automatically.
- **Manual Car:** Use arrow keys to drive the blue car.
- **AI Cars:** Observe as grey cars learn to drive.
- **Save Progress:** Click the 💾 icon to save the best-performing car's brain.
- **Discard Progress:** Click the 🗑️ icon to clear saved brain data.

---

## 🧠 Core Computer Science Concepts

### Object-Oriented Programming (OOP)

- **Classes & Encapsulation:**  
  - `Car` ([client/items/car.js]): Manages car state and actions.
  - `Sensor` ([client/controller/sensor.js]): Handles ray-casting sensors.
  - `NeuralNetwork` ([client/network/network.js]): Implements the car's brain.
  - `Road` ([client/items/road.js]): Manages road geometry and drawing.
- **Composition:**  
  - Cars are composed of sensors and neural networks for modularity.

### Algorithms

- **Feedforward Neural Network:**  
  - Processes sensor readings to control car movement.
- **Genetic Algorithm:**  
  - Selection: The car that travels farthest is considered "best."
  - Mutation: New cars are generated as mutated versions of the best brain.
- **Ray Casting & Line Intersection:**  
  - Sensor rays detect obstacles using computational geometry.

### Data Structures

- **Arrays:**  
  - 1D: Traffic cars, road borders, sensor readings, neurons.
  - 2D: Neural network weights.

### Architecture

- **Modular Design:**  
  - Clean directory structure (`items`, `controller`, `network`, `utils`) for separation of concerns and maintainability.

---

## ✅ Testing

Currently, there are no automated tests. Verification is performed visually by running the simulation and observing car behavior.

---

## 📄 License

This project is open-source and available for educational and personal use. See [LICENSE](LICENSE) for details.

---

## 🙌 Contributing

Contributions are welcome! Please open issues or submit pull requests to help improve the project.

---

## 📬 Contact

For questions or feedback, please open an issue on GitHub or contact the project maintainer.

---

Enjoy exploring and learning with the Self-Driving Car Simulation!