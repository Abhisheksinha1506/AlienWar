# 🎮 AlienWar Survival Game

A retro-style browser-based survival game built with p5.js where you navigate a grid-based world while avoiding relentless alien invaders. Survive as long as possible in this fast-paced, visually appealing game!

![Game Screenshot](https://via.placeholder.com/600x400/1a1a1a/00ff00?text=AlienWar+Survival+Game)

## 🎯 Gameplay

**Objective**: Survive as long as possible by avoiding alien invaders in a dynamic grid environment.

**Controls**:
- **Arrow Keys**: Move in four directions
- **Hold Keys**: Continuous movement with smooth animation
- **R Key**: Restart game after game over

**Game Elements**:
- 🟦 **Player** (Blue): Your character that you control
- 🔴 **Aliens** (Red): Hunt you down with AI pathfinding
- ⬜ **Walls** (Gray): Obstacles that block movement
- ⭐ **Starfield**: Animated background for atmosphere

## ✨ Features

### 🎨 Visual Design
- **Retro Aesthetic**: Dark theme with neon green accents
- **Smooth Animations**: Fluid player movement with interpolation
- **Visual Effects**: 
  - Animated starfield background
  - Hit flash effects when aliens are nearby
  - Pulsing alien graphics
  - Score scaling animations

### ⚙️ Customization
- **Grid Size Options**:
  - Small (10x10) - Easy navigation
  - Medium (20x20) - Balanced gameplay
  - Large (30x30) - Challenging survival
- **Game Speed Settings**:
  - Slow (45ms) - Relaxed pace
  - Normal (30ms) - Standard difficulty
  - Fast (15ms) - High-intensity action

### 🎮 Game Mechanics
- **Intelligent AI**: Aliens use pathfinding to hunt the player
- **Strategic Movement**: Navigate around walls and obstacles
- **Dynamic Spawning**: New aliens spawn from grid edges
- **Collision Detection**: Precise hit detection for game over
- **Continuous Movement**: Hold keys for smooth, responsive controls

## 🚀 Quick Start

### Prerequisites
- Any modern web browser (Chrome, Firefox, Safari, Edge)
- No additional software installation required

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/alienwar-survival-game.git
   cd alienwar-survival-game
   ```

2. **Open the game**:
   - Double-click `index.html` or
   - Open `index.html` in your web browser
   - Or serve locally: `python -m http.server 8000` then visit `http://localhost:8000`

3. **Start playing**:
   - Choose your preferred settings
   - Click "Apply" to start
   - Use arrow keys to move and survive!

## 🛠️ Technical Details

### Tech Stack
- **p5.js v1.4.2** - Graphics and animation framework
- **HTML5 Canvas** - Smooth rendering and visual effects
- **CSS3** - Retro styling and responsive design
- **Vanilla JavaScript** - Game logic and state management

### Architecture
```
AlienWar Survival Game/
├── index.html          # Main game file (HTML + CSS + JS)
└── README.md          # This documentation
```

### Key Components

#### Game State Management
```javascript
// Core game variables
let GRID_SIZE = 20;           // Grid dimensions
let CELL_SIZE = 30;           // Cell pixel size
let UPDATE_INTERVAL = 30;     // Game update frequency
let grid = [];                // 2D game world
let player = { x, y, displayX, displayY }; // Player object
let aliens = [];              // Enemy positions
let score = 0;                // Current score
```

#### Grid System
- **Character-based**: Uses symbols for game elements
  - `'W'` = Wall (obstacle)
  - `'P'` = Player
  - `'A'` = Alien
  - `'.'` = Empty space

#### Movement System
- **Smooth Interpolation**: Player position smoothly animates to target
- **Collision Detection**: Prevents movement through walls
- **Boundary Checking**: Keeps player within grid limits
- **Cooldown System**: Prevents excessive movement when holding keys

#### AI Pathfinding
```javascript
// Alien movement logic
if (Math.abs(dx) > Math.abs(dy)) {
  newX += dx > 0 ? 1 : -1;  // Prioritize horizontal movement
} else if (dy !== 0) {
  newY += dy > 0 ? 1 : -1;  // Then vertical movement
}
```

## 🎯 Game Strategies

### Beginner Tips
1. **Stay Centered**: Avoid getting cornered by aliens
2. **Use Walls**: Walls can block alien movement
3. **Plan Routes**: Think ahead about escape paths
4. **Watch Patterns**: Observe alien movement patterns

### Advanced Techniques
1. **Lure Aliens**: Use walls to create bottlenecks
2. **Quick Reactions**: Master continuous movement for fast escapes
3. **Grid Awareness**: Always know your position relative to edges
4. **Risk Assessment**: Balance survival time vs. risk-taking

## 🎨 Customization

### Modifying Game Settings
Edit the JavaScript variables in `index.html`:

```javascript
// Game difficulty
let UPDATE_INTERVAL = 30;     // Lower = faster aliens
let MOVE_DELAY = 10;         // Lower = faster player movement

// Visual settings
const MAX_CANVAS_WIDTH = 600; // Maximum canvas size
let CELL_SIZE = 30;          // Cell pixel size
```

### Adding New Features
The modular code structure makes it easy to add:
- New enemy types
- Power-ups
- Different grid layouts
- Sound effects
- Mobile touch controls

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Development Setup
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes
4. Test thoroughly in different browsers
5. Commit your changes: `git commit -m 'Add amazing feature'`
6. Push to the branch: `git push origin feature/amazing-feature`
7. Open a Pull Request

### Suggested Improvements
- [ ] Add sound effects and background music
- [ ] Implement mobile touch controls
- [ ] Add different alien types with unique behaviors
- [ ] Create power-ups and special abilities
- [ ] Add a high score system with local storage
- [ ] Implement different game modes (time attack, survival, etc.)
- [ ] Add particle effects for explosions and movement
- [ ] Create a level progression system

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **p5.js Team** - For the amazing graphics library
- **Processing Foundation** - For the creative coding inspiration
- **Open Source Community** - For the tools and resources that made this possible

## 📞 Support

If you encounter any issues or have questions:

1. **Check the Issues** page for known problems
2. **Create a new Issue** with detailed information
3. **Join our Discussions** for community help

---

**Enjoy the game and may the odds be ever in your favor!** 🚀👾

*Built with ❤️ using p5.js* 