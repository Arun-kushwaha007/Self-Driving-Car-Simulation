# 📘 Self-Driving Car Simulation

[![Live Demo](https://img.shields.io/badge/Live_Demo-Visit_Here-brightgreen?style=for-the-badge&logo=github)](https://www.aryansoni.tech/projects/self-driving-car/index.html)

## General Overview

### Project Description

This project is a browser-based simulation of a self-driving car built from scratch without any external machine learning libraries. It features a car that learns to navigate a road with traffic by using a simple feedforward neural network and a genetic algorithm. The project includes a real-time visualization of the car's sensor data and the underlying neural network activity.

### What the project does

The simulation generates a population of cars ("AI" controlled) and one user-controllable car. The AI cars use sensors to perceive their environment and a neural network (their "brain") to make driving decisions (accelerate, turn, reverse). When cars crash, they are disabled. The simulation is designed to run over generations, where the "brain" of the most successful car can be saved and used to "mutate" a new generation of cars, demonstrating a simple form of a genetic algorithm.

### Why it was created / problem it solves

This project was created as an educational tool to demonstrate and understand the core concepts of neural networks, genetic algorithms, and sensor-based control systems in a visual and interactive way. It solves the problem of abstract machine learning concepts being hard to grasp by providing a concrete, hands-on application that can be run, modified, and observed directly in the browser.

### Core features and functionality

*   **Self-Driving AI:** AI-controlled cars learn to navigate roads and avoid obstacles.
*   **Neural Network Engine:** A simple, dependency-free feedforward neural network written in plain JavaScript.
*   **Genetic Algorithm:** The ability to save the "best" car's brain and use it to generate new, slightly mutated brains for the next generation of cars.
*   **Real-time Visualization:** The simulation visualizes the car's sensors, the road, traffic, and the neural network's structure and activation in real-time.
*   **Manual Control:** A user can control one car with the keyboard for comparison or for generating training data.
*   **Collision Detection:** Simple but effective polygon-based collision detection.
*   **Local Storage Persistence:** The best-performing neural network brain can be saved in the browser's local storage.

## 🛠️ Tech Stack

*   **Languages:** HTML5, CSS3, JavaScript (ES6+)
*   **Frameworks/Libraries:** None. This project is built with vanilla JavaScript to focus on the underlying algorithms.
*   **Tools:**
    *   HTML5 Canvas for rendering and visualization.
    *   Browser Local Storage for saving model progress.

## 📂 Setup & Usage

### Installation Instructions

No installation is required. The project is designed to run directly in any modern web browser.

1.  Clone the repository to your local machine:
    ```bash
    git clone https://github.com/Arun-kushwaha007/Self-Driving-Car-Simulation/
    ```
2.  Navigate to the project directory:
    ```bash
    cd Self-Driving-Car-Simulation
    ```

### Usage Guide

1.  Open the `index.html` file in a web browser.
2.  The simulation will start automatically.
3.  You can drive the blue car using the **arrow keys**.
4.  Observe the grey AI cars as they learn to drive.
5.  **Saving Progress:** Click the **Save** icon (💾) to save the brain of the best-performing car (the one that traveled the farthest) to your browser's local storage. On the next page load, new AI cars will be mutated versions of this saved brain.
6.  **Discarding Progress:** Click the **Trash** icon (🗑️) to clear the saved brain from local storage.

## 🧠 Core Computer Science Concepts Used

This project is a practical application of several fundamental computer science concepts.

### Object-Oriented Programming (OOP)

The entire codebase is structured using OOP principles, making it modular and easy to understand.

*   **Classes & Encapsulation:** The system is broken down into distinct classes, each encapsulating its own data and behavior.
    *   `Car` (`client/items/car.js`): Manages the car's state (position, speed, angle) and actions (moving, drawing, damage assessment).
    *   `Sensor` (`client/controller/sensor.js`): Encapsulates the logic for the car's ray-casting sensors.
    *   `NeuralNetwork` (`client/network/network.js`): Represents the car's brain, encapsulating all the logic for network layers, weights, biases, and the feedforward process.
    *   `Road` (`client/items/road.js`): Manages the geometry and drawing of the road.
*   **Composition:** The project favors composition over inheritance. A `Car` object is *composed* of a `Sensor` object and a `NeuralNetwork` object, creating a flexible and powerful relationship.

### Algorithms

*   **Feedforward Neural Network:** This is the core of the AI. The `NeuralNetwork.feedForward` method in `client/network/network.js` takes sensor readings as input and propagates them through the network's layers to produce an output, which dictates the car's controls. Each layer's calculation involves a weighted sum of inputs followed by a simple step activation function.
*   **Genetic Algorithm (Simplified):** The project uses key elements of a genetic algorithm for training.
    *   **Selection:** The `main.js` script identifies the "best" car (fittest individual) based on its survival distance.
    *   **Reproduction/Mutation:** The `NeuralNetwork.mutate` method takes a network and applies slight random changes to its weights and biases. When a "best brain" is saved, new cars are generated as mutated offspring of that brain, allowing the system to "evolve" better driving skills over time.
*   **Ray Casting & Line Intersection:** The `Sensor` class implements a ray-casting algorithm to perceive the environment. In `client/utils/utils.js`, the `getIntersection` function implements a standard line-segment intersection algorithm to calculate the exact point where a sensor ray collides with a road border or another car. This is a classic algorithm from **computational geometry**.

### Data Structures

*   **Arrays:** Arrays are the primary data structure used throughout the project.
    *   **1D Arrays:** Used to store a list of traffic cars, road borders, sensor readings, and the neurons in a network layer (`inputs`, `outputs`, `biases`).
    *   **2D Arrays (Arrays of Arrays):** Used in `client/network/network.js` to represent the `weights` connecting one layer of the neural network to the next.

### Architecture

*   **Modular Design:** The project is organized into a clean directory structure (`items`, `controller`, `network`, `utils`) that separates concerns. This makes the code easier to navigate, maintain, and debug. For example, all neural network logic is contained within the `network` directory.

## ✅ Testing

There are currently no automated tests for this project. Verification is done visually by running the simulation.

## 🤝 Contribution Guidelines

Contributions are welcome! Please feel free to fork the repository, make changes, and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

<!-- ## 📄 License -->

<!-- This project is licensed under the MIT License. See the `LICENSE` file for details. -->
