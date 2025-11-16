# Zuq Solvee - Challenge Tracker - A Framer Motion Learning Project

<p align="center">
  <img alt="React" src="https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB"/>
  <img alt="Framer Motion" src="https://img.shields.io/badge/Framer%20Motion-FF0088?style=for-the-badge&logo=framer&logoColor=white"/>
  <img alt="Vite" src="https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white"/>
</p>

Welcome to Zuq Solvee, a React Challenge Tracker! This project is a hands-on application built to explore and master the animation capabilities of the **Framer Motion** library in a React environment. The application itself is a simple tool for adding, tracking, and managing personal challenges.

The primary goal of this project was to implement a wide range of animations to create a fluid, dynamic, and engaging user experience.

## Features

- **Welcome Page**: A landing page with beautiful scroll-driven animations.
- **Add Challenges**: Users can add new challenges through an animated modal.
- **Track Challenges**: View challenges in three categories: "Active", "Completed", and "Failed".
- **Dynamic UI**: The entire interface is packed with animations, from simple button feedback to complex layout transitions.

## Learning Framer Motion: Concepts Implemented

This project served as a playground for learning various Framer Motion hooks and components. Here’s a breakdown of the key concepts you'll find in the code:

### 1. Core Motion Components

- **`<motion.{html_element}>`**: Used extensively for animating basic elements. You can see this in `Header.jsx` for button hover effects (`whileHover`) and in `ChallengeItem.jsx` for list item animations.
- **Animation Props**: `initial`, `animate`, and `exit` props are used to define an element's state for entry, active, and exit animations. This is a cornerstone of animations in `Modal.jsx` and `Challenges.jsx`.

### 2. `AnimatePresence`

- Used to animate components when they are added to or removed from the React tree. This is crucial for:
  - The appearance and disappearance of the `NewChallenge` modal in `Header.jsx`.
  - Animating the list of challenges in `Challenges.jsx` when the filter tabs are switched.
  - Showing and hiding the description in `ChallengeItem.jsx`.

### 3. Layout Animations

- **`layout` prop**: This powerful prop is used in `ChallengeItem.jsx` (`<motion.li layout>`) to automatically animate an item's position when the list is re-ordered or filtered.
- **`layoutId`**: Creates a "magic move" or shared layout animation effect. This is beautifully demonstrated in `ChallengeTabs.jsx`, where the active tab indicator smoothly slides from one tab to another.

### 4. Scroll-Triggered Animations

- **`useScroll` hook**: Used in `Welcome.jsx` to track the vertical scroll position (`scrollY`).
- **`useTransform` hook**: This hook maps the scroll position to different animation values. In `Welcome.jsx`, it's used to create a stunning parallax effect on the header images and text as the user scrolls down the page.

### 5. Advanced Animation Control

- **`useAnimate` hook**: Provides imperative control over animations. In `NewChallenge.jsx`, it's used to trigger a "shake" animation on invalid form fields.
- **`staggerChildren`**: A transition property used to create a staggered animation effect for child elements. You can see this in `NewChallenge.jsx` to animate the appearance of the challenge images one after another.
- **Variants**: Pre-defined animation states that can be referenced by name. They help in keeping the code clean and are used in `Modal.jsx` and `NewChallenge.jsx`.

## How to Run This Project Locally

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/Murzuq/Zuq-Solvee.git
    ```

2.  **Navigate to the project directory:**

    ```sh
    cd Zuq-Solvee
    ```

3.  **Install dependencies:**

    ```sh
    npm install
    ```

4.  **Start the development server:**
    ```sh
    npm run dev
    ```

The application will be available at `http://localhost:5173` or any available port.

## Project Structure

- `src/components/`: Contains all the individual React components. Each component is designed to be as reusable as possible.
- `src/pages/`: Contains the main page components that are rendered by React Router.
- `src/assets/`: Contains static assets like images.
- `src/store/`: Contains the React Context for managing the state of the challenges.

---

This project was a fantastic learning experience and a great demonstration of how Framer Motion can elevate a standard React application into something truly special. Feel free to explore the code to see how each animation was crafted!
