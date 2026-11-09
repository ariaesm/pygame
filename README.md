# Race Car — a Pygame dodging game

A small 2D arcade game written with [Pygame](https://www.pygame.org/): drive the car left and right and dodge the falling blocks. Every block you pass raises your score, and the blocks fall faster every 5 points. Hitting a block or the edge of the road ends the run.

## Features

- Start menu with clickable **Play** / **Quit** buttons
- Increasing difficulty: obstacle speed goes up every 5 blocks dodged
- Background music and a crash sound effect
- Live "Dodged" score counter

## Getting started

Requires Python 3.8+.

```bash
git clone https://github.com/ariaesm/pygame.git
cd pygame
pip install -r requirements.txt
python race_car.py
```

## Controls

| Key | Action |
| --- | --- |
| ← / → | Move the car |
| Mouse | Click the menu buttons |

## Project structure

```
race_car.py      # game loop, rendering, collision detection
assets/
  car.png        # player sprite
  music.ogg      # background music
  crash.wav      # crash sound
```

## How it works

The game runs a classic loop at 60 FPS: read input → update the car and obstacle positions → check for collisions with simple rectangle overlap → redraw the screen. When the obstacle leaves the screen it respawns at a random x position and the score goes up; every fifth point the fall speed increases.

## License

[MIT](LICENSE)
