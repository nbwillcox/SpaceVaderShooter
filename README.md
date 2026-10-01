# SpaceVaderShooter

A free, retro-flavored space shooter with modern neon graphics and a head nod to classic fixed-shooter invader games. A marching armada descends on your planet: slide left and right, hide behind crumbling shields, shoot the invaders before they reach the ground, and take down giant Overlord bosses.

**Play it in your browser:** https://nbwillcox.github.io/SpaceVaderShooter/ *(live once GitHub Pages is enabled for this repo)*

Everything is generated in code: sprites are vector-drawn on the fly, and all sound effects and music are synthesized with the Web Audio API. There are no image or audio files and no build step. A sibling of [SpaceGalaShooter](https://github.com/nbwillcox/SpaceGalaShooter) and [SpaceCentiShooter](https://github.com/nbwillcox/SpaceCentiShooter), with the same look and feel.

## Controls

| Action | Keys |
| --- | --- |
| Move (left/right only) | `←` `→` or `A` `D` (mouse position also steers) |
| Fire (hold to auto-fire) | `Space` or left mouse button |
| Smart bomb | `B`, `X`, `↑` or right mouse button |
| Pause | `P` or `Esc` |

## Gameplay

- The formation marches side to side and **drops a row at every edge**. The fewer invaders left, the faster they march. If any invader reaches the planet line, **it is instant game over**.
- **Shields:** four pixel-erosion bunkers chip away from enemy bombs, your own shots, and anything that marches into them. They rebuild fully at the start of every wave.
- **Invaders:**
  - Three row types worth 30 / 20 / 10 points: Scouts, Raiders and Brutes.
  - **Armored** invaders take 2 to 3 hits as waves climb.
  - **Bombers** drop a three-way spread.
  - **Commanders** shield every invader around them until you take them out. They are always the lowest in their column, so you can reach them.
- **Bombs:** the lowest invader in a column drops them: straight needles, wobbling zigzag bombs, and slow plunger shells that gouge the shields.
- **Flyby mothership** crosses the top now and then for a big randomized score and a guaranteed power-up.
- From wave 6, formations switch from the classic block to diamonds, chevrons, split blocks, rings and pyramids.
- **Power-ups** drop from glowing carrier invaders, the mothership and bosses:
  - **W** weapon tier: single → double → spread → piercing lances (a hit drops you one tier)
  - **D** wingman drone (up to 2)
  - **S** shield bubble
  - **B** smart bomb
- Chain kills for a score multiplier (up to x8) and clear a wave without being hit for a Perfect bonus.
- Every 5th wave is an **Overlord**: a giant armored invader that marches and drops like the formation. Shoot off its turrets, cannons, beam emitters and launchers, take out the generators to drop the core shield, then destroy the core before it crushes the shields and reaches the planet. Five unique bosses, scaling up each loop.
- Local top-10 high scores with arcade-style 3-letter initials (stored in your browser).

## Run locally

It is plain HTML/CSS/JS. Either open `index.html` directly, or serve the folder:

```bash
python -m http.server 8000
```

then visit http://localhost:8000. Desktop browsers with keyboard/mouse only for now.

## License and attribution

Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): free to play, share and remix **non-commercially**, as long as you give credit and **link back to this repository**: https://github.com/nbwillcox/SpaceVaderShooter

This is an original game inspired by classic arcade shooters. It uses no assets, names or code from any existing game.
