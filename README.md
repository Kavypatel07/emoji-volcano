# 🌋 Ultimate Emoji Volcano

> **A physics-based emoji simulation featuring streak mechanics, boss modes, and glassmorphism UI.**

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Tech](https://img.shields.io/badge/tech-HTML5%20%7C%20CSS3%20%7C%20JS-blue.svg)
![Physics](https://img.shields.io/badge/physics-Matter.js-orange.svg)

---

## 📸 Demo

![Project Screenshot](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExM3R6eWJueHByZnh5Znh5Znh5Znh5Znh5/placeholder.gif)
*(The Volcano Mode in action: 10x Streak leads to an eruption!)*

## 🚀 Overview

This is not just a "rain" effect. It is a full interactive physics playground built with **Matter.js**. 

Users interact with a centralized **Glassmorphism Control Panel** containing 10 distinct emojis. Clicking builds a "Streak." Reaching a **10x Streak** triggers **"Boss Mode" (Volcano)**, where the UI transforms, and emojis erupt from the bottom of the screen using randomized velocity vectors.

## ✨ Features

### 🎮 Gamified Mechanics
* **Streak System:** Tracks consecutive clicks on the same emoji.
* **Combo Meter:** Dynamic counter with gradient text that reacts to your clicking speed.
* **Boss Mode (Volcano):** Reach a 10x streak to trigger a massive physics eruption.
* **Focus State:** When Volcano activates, non-active buttons fade away to spotlight the action.

### 🎨 Premium UI/UX
* **Glassmorphism:** Apple-style frosted glass buttons with complex `box-shadow` layering and `backdrop-filter`.
* **Responsive Grid:** A perfectly centered 5x2 grid that adapts to screen sizes.
* **Visual Feedback:** Buttons glow gold during "Boss Mode" and have tactile hover/active states.

### ⚛️ Physics Engine
* **Gravity & Collisions:** Emojis have weight, friction, and restitution (bounciness).
* **Stacking:** Emojis pile up on the floor and interact with each other.
* **Performance:** Automatic garbage collection removes physics bodies after 8 seconds to prevent memory leaks.

---

## 🛠️ Tech Stack

* **Core:** Vanilla HTML5, CSS3, JavaScript (ES6+).
* **Physics Engine:** [Matter.js](https://brm.io/matter-js/) (via CDN).
* **Assets:** [Microsoft Fluent Emojis](https://github.com/microsoft/fluentui-emoji) (via JSDelivr CDN).

---

## 🏃‍♂️ Quick Start

No build tools or Node.js required. This is a pure static site.

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/yourusername/emoji-volcano.git](https://github.com/yourusername/emoji-volcano.git)
    ```
2.  **Open `ultimate_rain.html`** in any modern web browser.
3.  **Start Clicking!**

---

## ⚙️ Customization

### Changing the Emojis
The buttons are defined in the HTML `div` grid. To change an emoji, simply update the `onclick` parameter and the `img src`.

```html
<div class="glass-btn" onclick="handleClick(this, 'URL_TO_PIZZA_IMAGE.png')">
    <img src="URL_TO_PIZZA_IMAGE.png" alt="Pizza">
</div>
```

### Adjusting Physics
Tweak the createEmojiBody function in the <script> tag:

```JavaScript
restitution: 0.6, // Higher = More Bouncy (0.0 to 1.0)
friction: 0.002,  // Lower = Slippery (Ice-like)
density: 0.04,    // Higher = Heavier objects
```
