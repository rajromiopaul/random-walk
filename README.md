# 🐢 Turtle Random Walk

A Python script that uses the built-in `turtle` graphics library to draw a colorful, random-direction path on screen — a classic **random walk** visualization.

## What It Does

The turtle moves across the canvas in a continuous loop, alternating between:
1. **Changing direction** — randomly picking from 0°, 90°, 180°, or 270°
2. **Moving forward** — advancing 20 units in the current direction

Each step is drawn in a randomly chosen color with a thick pen, producing a vivid, winding trail.

## Preview

The output looks like a brightly colored maze-like scribble that grows indefinitely across the screen.

## Requirements

- Python 3.x
- No external libraries needed — `turtle` and `random` are part of the Python standard library

## How to Run

```bash
python turtle_walk.py
```

> A graphics window will open and the turtle will start drawing immediately. Close the window to stop.

## Code Overview

```python
import random
from turtle import Turtle

tim = Turtle()
colors = ["red", "blue", "green", "yellow", "purple", "orange", "pink", "teal"]
```

| Parameter | Value | Description |
|-----------|-------|-------------|
| `tim.width(12)` | 12px | Pen thickness |
| `tim.speed('fast')` | fast | Drawing speed |
| Step size | 20 units | Distance moved per forward step |
| Directions | 0, 90, 180, 270 | Possible turn angles (right turns) |

## How It Works

The script uses a simple counter `n` to alternate between two actions on each loop iteration:

- When `n == 1` → call `change_direction()`, reset `n` to 0
- When `n == 0` → move forward 20 units, set `n` to 1

The `change_direction()` function turns the turtle **right** by a random multiple of 90°, keeping all movement axis-aligned (up, down, left, right).

## Customization Ideas

- **Change colors** — add or remove color names from the `colors` list
- **Change step size** — modify the `20` in `tim.forward(20)` for longer or shorter steps
- **Change pen width** — adjust `tim.width(12)` for thinner or thicker lines
- **Change speed** — set `tim.speed()` to `'slow'`, `'normal'`, `'fast'`, or `'fastest'`
- **Add a background color** — use `tim.getscreen().bgcolor("black")` for a dark canvas

## License

Free to use and modify. No attribution required.
