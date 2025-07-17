---
inclusion: always
---

# Django Chess Game Development Standards

## Project Overview
This is a Django-based chess game called "Kiro Chess Battle III" - a geopolitical chess game where players represent NATO Alliance vs Russian Alliance with special abilities.

## Architecture
- **Backend**: Django 5.1.4 framework
- **Database**: SQLite3 (development), PostgreSQL (production)
- **Frontend**: Django templates with JavaScript and HTML5 Canvas
- **Game Logic**: Custom chess engine with Minimax algorithm

## Code Standards

### Django Best Practices
- Follow Django's MVT (Model-View-Template) pattern
- Use Django's built-in authentication and session management
- Implement proper CSRF protection
- Use Django's ORM for database operations
- Follow Django naming conventions for apps, models, and views

### Game Logic Standards
- Keep chess logic modular and separated by concern:
  - `engine.py` - AI logic (Minimax algorithm)
  - `controller.py` - Game state management
  - `movements.py` - Piece movement rules
  - `checkCheck.py` - Check/checkmate detection
  - `getLegalMoves.py` - Legal move validation

### Frontend Standards
- Use Django templates for HTML rendering
- Implement AJAX for real-time game updates
- Use HTML5 Canvas for dynamic chess board rendering
- Maintain responsive design principles

### Security Considerations
- Never expose SECRET_KEY in production
- Use proper CSRF tokens for all forms
- Validate all user inputs
- Sanitize data before database operations

### Performance Guidelines
- Optimize AI depth based on performance requirements
- Use session storage efficiently for game state
- Implement proper caching where appropriate
- Monitor AI response times (currently logged to data.csv)

## File Structure
- `game/` - Main game application
- `chessGame/` - Django project settings
- `images/` - Chess piece assets
- `templates/` - HTML templates
- `static/` - CSS, JS, and static assets