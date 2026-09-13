# Icy Tower 

## Game Design Document

| Field | Value |
|---|---|
| Status | Pending lecturer approval through the designated course GDD Google Sheet |
| Team | Rom Meir and Daniel Freund |
| Genre | Single-player 2D vertical endless platformer |
| Target platform | Android Mobile |
| Engine | Unity 6, 6000.3.21f1, 2D |
| Display | Portrait, 1080 x 1920 reference resolution, 9:16 |
| Expected session length | Approximately 3–5 minutes per run, endless until the player falls |
| Document version | v0.1, 2026-09-13 |

---

## 1. High Concept

The game is a single-player 2D vertical platformer inspired by the classic game Icy Tower.

The player controls a character that continuously jumps upward from platform to platform inside an endless tower.

The main objective is to climb as high as possible, survive for as long as possible, and achieve the highest score.

The player mainly controls horizontal movement while jumping happens automatically after landing on a platform.

As the player climbs higher, the game gradually becomes faster and more difficult. New platform types, collectibles, and challenges are introduced during the run.

Before starting the game, the player can choose between three different playable characters.

### Design Pillars

1. **Simple controls, skill-based gameplay**  
   The basic controls should be easy to understand, while accurate movement and landing require skill.

2. **Continuous upward progression**  
   The player always has a clear goal: climb higher and improve the score.

3. **Increasing difficulty**  
   The game becomes more difficult as the player progresses.

4. **Replayability**  
   Short sessions, high scores, character selection, combos, and collectibles encourage players to try again.

5. **Mobile-first design**  
   The game is designed for portrait mobile gameplay with simple touch controls.

---

## 2. Reference and Inspiration

### Primary Reference

The main gameplay inspiration is the classic game **Icy Tower**.

### Taking

The project takes inspiration from:

- Vertical platform climbing
- Automatic jumping
- Horizontal movement control
- Endless upward progression
- Increasing difficulty
- Score based on height and performance
- Fast restart after losing

### Changing

Our version will include:

- Three selectable playable characters
- Mobile touch controls
- Multiple special platform types
- Coins or collectibles
- Combo mechanics
- Visual effects
- Changing environments as the player climbs
- Modern mobile UI
- Power-ups if development time allows

### Not Taking

The project will not use:

- Original Icy Tower characters
- Original Icy Tower artwork
- Original Icy Tower audio
- Original levels
- Copyrighted assets from the original game

All assets used in the project will be original or properly licensed.

### Visual Direction

The game will use a colorful and readable 2D visual style.

The environment can change as the player climbs higher.

Possible visual areas:

- Tower entrance
- City
- Clouds
- Sky
- Space or fantasy-themed upper area

The three playable characters will have clearly different visual appearances.

---

## 3. Core Game Loop

```mermaid
flowchart TD

    A[Main Menu] --> B[Choose Character]

    B --> C[Start Run]

    C --> D[Jump and move between platforms]

    D --> E[Climb higher and gain score]

    E --> F{Player still alive?}

    F -- Yes --> G[Difficulty increases]

    G --> D

    F -- No --> H[Game Over]

    H --> I[Show Score and High Score]

    I --> J{Play Again?}

    J -- Yes --> C

    J -- No --> A
