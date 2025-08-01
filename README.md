# Dog Holiday Run 🐶🏃‍♂️ - A JavaScript 2D Game Engine Showcase

[![Live Demo](https://img.shields.io/badge/Demo-Play%20Now-green?style=flat&logo=google-chrome)](https://arun-kushwaha007.github.io/Dog-Hoiday-Run/)
[![GitHub stars](https://img.shields.io/github/stars/Arun-kushwaha007/Dog-Hoiday-Run?style=social)](https://github.com/Arun-kushwaha007/Dog-Hoiday-Run/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Arun-kushwaha007/Dog-Hoiday-Run?style=social)](https://github.com/Arun-kushwaha007/Dog-Hoiday-Run/network)

**Dog Holiday Run** is a vibrant, 2D side-scrolling adventure game built from the ground up with vanilla JavaScript, HTML, and CSS. While it's a fun game to play, its primary purpose is to serve as a comprehensive showcase of modern JavaScript features and fundamental computer science concepts applied to game development.

This project is an excellent resource for developers looking to understand how to build a game engine using object-oriented principles and design patterns, without relying on external game frameworks.

---

## 🚀 Live Demo

Experience the game in your browser now!

**[➡️ Play Dog Holiday Run](https://arun-kushwaha007.github.io/Dog-Hoiday-Run/)**

---

## 🕹️ How to Play

-   **Movement**: Use the **Arrow Keys** (`ArrowLeft`, `ArrowRight`, `ArrowUp`, `ArrowDown`) to move the player.
-   **Rolling Attack**: Press the **Spacebar** to enter the "Rolling" state. In this state, you can defeat enemies by colliding with them.
-   **Objective**: Your goal is to defeat enemies and score points. Be careful! If an enemy hits you when you are not in the "Rolling" state, you will lose a life.

---

## ✨ Features

-   **Dynamic Player States**: Seamlessly switch between states like sitting, running, jumping, falling, and rolling.
-   **Diverse Enemies**: Encounter multiple types of enemies, each with unique movement patterns.
-   **Parallax Scrolling**: A multi-layered background that creates an illusion of depth and immersion.
-   **Particle System**: Dynamic particle effects for actions like running (dust), attacking (fire), and landing (splash).
-   **Collision Detection**: Real-time collision detection between the player and enemies.
-   **Score and Lives System**: Track your score and remaining lives to challenge yourself.
-   **Responsive Controls**: Fluid and responsive player controls for an enjoyable gameplay experience.

---

## 🛠️ Technical Deep Dive

This project is a practical demonstration of several key programming concepts.

### Object-Oriented Programming (OOP) Principles

The entire codebase is structured around OOP principles, making it modular, scalable, and easy to maintain.

-   **Encapsulation**: Each component of the game (`Player`, `Enemy`, `Background`, `UI`) is a self-contained class that bundles its own data (properties) and behavior (methods). This hides the internal complexity and exposes a clean interface.
-   **Inheritance**: The project uses a base `Enemy` class to define common properties and methods for all enemies. Specific enemy types (`FlyingEnemy`, `GroundEnemy`, `ClimbingEnemy`) then `extend` this base class, inheriting its functionality while adding their own unique behaviors.
-   **Polymorphism**: Each enemy subclass provides its own implementation of the `update` method. This allows the game loop to treat all enemies polymorphically, calling the same `update` method on each one without needing to know its specific type.
-   **Composition**: The `Background` class is composed of multiple `Layer` instances. This "has-a" relationship allows for the creation of a complex parallax scrolling system by combining simpler objects.

### Software Design Patterns

-   **State Pattern**: The player's behavior is managed by a sophisticated State Pattern. Instead of using a large `if/else` or `switch` statement, each player state (e.g., `Sitting`, `Running`, `Jumping`) is encapsulated in its own class. The `Player` class holds a reference to the current state object and delegates all state-specific actions to it. This makes it incredibly easy to add new states or modify existing ones without touching the `Player` class logic.

### Modern JavaScript (ES6+) Features

-   **ES6 Modules**: The codebase is organized into modules using `import` and `export` statements. This improves code organization and prevents pollution of the global namespace.
-   **ES6 Classes**: The `class` syntax is used extensively to create clean and readable object-oriented structures.
-   **Arrow Functions, `let`, and `const`**: The project uses modern JavaScript syntax for more concise and predictable code.

### Core Game Development Concepts

-   **Game Loop**: The `main.js` file contains a classic game loop, driven by `requestAnimationFrame`, which ensures smooth and efficient rendering by syncing with the browser's refresh rate.
-   **Sprite Animation**: The game achieves animation by cycling through frames of a sprite sheet. The `Player` and `Enemy` classes contain logic to manage frame indices and animation speed.
-   **Collision Detection**: The `Player` class features an axis-aligned bounding box (AABB) collision detection system to check for interactions with enemies.
-   **Particle System**: A simple yet effective particle system (`particles.js`) is used to generate visual effects like dust trails, fire, and water splashes, adding a layer of polish to the game.

---

## 🚀 Installation & Setup

No complex build steps are required to run this project locally.

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Arun-kushwaha007/Dog-Hoiday-Run.git
    ```

2.  **Navigate to the Directory:**
    ```bash
    cd Dog-Hoiday-Run
    ```

3.  **Open in Browser:**
    -   Simply open the `index.html` file in your favorite web browser.

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for new features, improvements, or bug fixes, feel free to open an issue or submit a pull request.

---

## ©️ Credits

-   **Developed by**: [Arun Kushwaha](https://github.com/Arun-kushwaha007)
-   **Project inspired by**: Franks Laboratory - JavaScript Game Development Course

---

## 📜 License

This project is open source and available for personal and educational use.

---

Enjoy the run! 🐕✨
