---
inclusion: fileMatch
fileMatchPattern: "settings.py"
---

# Security Guidelines for Django Chess Game

## Critical Security Reminders

### Secret Key Management
- Never commit SECRET_KEY to version control
- Use environment variables for production: `os.environ.get('SECRET_KEY')`
- Generate new secret keys for different environments

### Debug Settings
- Always set `DEBUG = False` in production
- Remove or restrict `ALLOWED_HOSTS = ['*']` in production
- Use specific domain names in ALLOWED_HOSTS

### Database Security
- Use strong database passwords
- Never commit database credentials to code
- Use environment variables for database configuration
- Enable SSL for database connections in production

### CSRF Protection
- Ensure CSRF middleware is enabled
- Use `{% csrf_token %}` in all forms
- Configure CSRF_TRUSTED_ORIGINS properly

### Session Security
- Use secure session cookies in production
- Set appropriate session timeouts
- Consider using database-backed sessions for scalability

### Input Validation
- Validate all user inputs in views
- Sanitize data before database operations
- Use Django's built-in form validation
- Be cautious with eval() or exec() functions

### File Upload Security
- Validate file types and sizes
- Store uploads outside web root
- Scan uploaded files for malware
- Use proper file permissions