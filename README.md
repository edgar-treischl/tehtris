# Tehtris 🎮

A Tetris-like game built with vanilla **HTML, CSS, and JavaScript** to teach kids how web games work.

## 🎯 What is This?

**Tehtris** is an educational project that demonstrates core game development concepts:
- **Game State Management** - Tracking what's happening (start, playing, paused, game over)
- **Collision Detection** - Detecting when pieces hit walls or land
- **Rendering** - Drawing graphics on canvas
- **Input Handling** - Responding to keyboard controls
- **Game Loop** - Updating the game continuously

Perfect for beginners learning HTML, CSS, and JavaScript!

## 🚀 How to Play

1. Open `index.html` in your web browser (or serve locally)
2. Read the controls on the start screen
3. Click **Start Game**
4. Use arrow keys, spacebar, and P to play

### Controls
- **← →** - Move left/right
- **↓** - Soft drop
- **↑** - Rotate piece
- **SPACE** - Hard drop
- **P** - Pause/Resume
- **Q** - Quit to start screen

## 📁 Project Structure

```
tehtris/
├── index.html       # Game HTML (UI elements)
├── style.css        # Styling (colors, layout, buttons)
├── tetra.js         # Main game controller (state machine, input)
├── board.js         # Board configuration & initialization
├── pieces.js        # Tetromino definitions
├── rules.js         # Game logic (collision, rotation, scoring)
├── ui.js            # Canvas drawing functions
└── audio/           # Background music & sound effects
```

## 🧠 Learning Concepts

### **Modular Code**
Each file has ONE job:
- `tetra.js` = controls game flow
- `rules.js` = game logic
- `ui.js` = drawing only
- `board.js` = data structures

### **ES6 Modules**
Uses `import/export` to keep code organized:
```javascript
import { pieces } from './pieces.js';
import { collide, merge, clearLines } from './rules.js';
```

### **Canvas API**
Drawing with JavaScript:
```javascript
ctx.fillStyle = "cyan";
ctx.fillRect(x, y, size, size);
```

### **Game Loop**
Updates 60+ times per second:
```javascript
setInterval(() => {
  drop();          // Update
  update();        // Render
}, dropInterval);
```

### **State Machine**
Game always in one state:
- `"start"` → Start screen
- `"playing"` → Active game
- `"paused"` → Paused game
- `"gameover"` → Game over screen

## 🎮 Running Locally

**Option 1: Simple HTTP Server**
```bash
python3 -m http.server 8000
# Visit http://localhost:8000
```

**Option 2: Python SimpleHTTPServer (older)**
```bash
python -m SimpleHTTPServer 8000
```

**Option 3: Node.js**
```bash
npx http-server
```


## 📖 History

The `history/` folder contains development snapshots step by step to rebuild.


