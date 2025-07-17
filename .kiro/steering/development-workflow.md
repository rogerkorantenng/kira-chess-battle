---
inclusion: always
---

# Development Workflow & Commands

## Common Development Tasks

### Running the Application
```bash
# Activate virtual environment (if using)
# Windows: venv\Scripts\activate
# Linux/Mac: source venv/bin/activate

# Run development server
python manage.py runserver

# Run with specific port
python manage.py runserver 8080
```

### Database Operations
```bash
# Create migrations after model changes
python manage.py makemigrations

# Apply migrations
python manage.py migrate

# Create superuser for admin access
python manage.py createsuperuser

# Reset database (SQLite)
# Delete db.sqlite3 and run migrate
```

### Testing & Debugging
```bash
# Run tests
python manage.py test

# Run specific app tests
python manage.py test game

# Clear cache (using django-clearcache)
python manage.py clearcache

# Collect static files (for production)
python manage.py collectstatic
```

### Game Development Workflow
1. **Game Logic Changes**: Modify files in `game/` directory
2. **AI Improvements**: Update `engine.py` with new algorithms
3. **Frontend Updates**: Modify templates and static files
4. **Testing**: Test both local and AI game modes
5. **Performance**: Monitor AI response times in `data.csv`

### Deployment Considerations
- Switch from SQLite to PostgreSQL for production
- Update `ALLOWED_HOSTS` in settings
- Set `DEBUG = False` for production
- Configure proper static file serving
- Use environment variables for sensitive settings