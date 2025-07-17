---
inclusion: always
---

# Chess Game Context & Features

## Game Concept
Kiro Chess Battle III is a geopolitical chess game where global conflicts are resolved through strategic chess matches instead of warfare.

## Alliance System

### NATO Alliance
- **United States** (Trump): Economic Sanctions - restricts opponent moves
- **United Kingdom** (Sunak): Special Forces - extra strategic move
- **France** (Macron): Diplomatic Retreat - safely withdraw pieces
- **Italy, Israel, Ukraine**: Passive alliance synergy boosts

### Russian Alliance  
- **Russia** (Putin): Blitzkrieg - two attacks in one turn
- **China** (Xi Jinping): Trade Negotiations - temporary piece shields
- **North Korea** (Kim Jong-un): Missile Strike - remove opponent pawns
- **Iran, Burkina Faso, Belarus**: Passive alliance synergy boosts

## Technical Implementation
- Session-based game state management
- AJAX-powered real-time updates
- Minimax AI with configurable depth (currently 3)
- Special abilities system integrated with chess logic
- Performance monitoring via CSV logging

## Key Game States
- `board`: 8x8 chess board representation
- `turn`: Boolean (True=white/light, False=black/dark)
- `movedStatus`: Castling eligibility tracking
- `enPassant`: En passant move tracking
- `captureStatus`: Captured pieces tracking
- `aiColor`: AI player color assignment

## Game Modes
1. **Local Play**: Two human players
2. **AI Play**: Human vs AI with alliance abilities