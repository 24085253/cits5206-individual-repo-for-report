# CLI Tools Usage Documentation - Chenglin Hou (24085253)

## Project Overview
**Project**: SmallGoods Competition App - CITS5206
**Student**: Chenglin Hou (24085253)
**Focus**: Command-line tools for development workflow and project management

---

## Git Command Line Workflow

### Core Development Workflow
```bash
# Branch creation and management
git checkout -b feature-athlete
git checkout -b realtime-competition-sync
git checkout -b login-page-dev

# Development cycle
git add .
git commit -m "Implement athlete dashboard functionality"
git push -u origin feature-athlete

# Branch merging workflow
git checkout main
git pull origin main
git merge feature-athlete
git push origin main
```

### Advanced Git Operations
```bash
# Interactive rebase for clean history
git rebase -i HEAD~3

# Stash management during development
git stash push -m "WIP: athlete form validation"
git stash pop

# Remote branch management
git branch -r
git branch --merged
git branch -d feature-completed

# Conflict resolution
git status
git diff
git mergetool
```

---

## GitHub CLI (gh) Usage

### Repository Management
```bash
# Repository operations
gh repo view cits5206Group9/SmallGoods-Competition-app
gh repo clone cits5206Group9/SmallGoods-Competition-app
gh repo fork cits5206Group9/SmallGoods-Competition-app

# Issue management
gh issue list --assignee 24085253
gh issue create --title "Real-time data synchronization" --body "Implementation details..."
gh issue close 46
```

### Pull Request Workflow
```bash
# PR creation and management
gh pr create --title "Feature: Athlete Dashboard Implementation" --body "Comprehensive athlete interface with real-time updates"
gh pr list --author 24085253
gh pr status
gh pr merge 60 --squash

# PR review process
gh pr review 39 --approve --body "Clean architecture and comprehensive coverage"
gh pr review 34 --request-changes --body "Consider data integrity improvements"
```

### Advanced GitHub CLI Operations
```bash
# Milestone management
gh api repos/cits5206Group9/SmallGoods-Competition-app/milestones
gh issue edit 46 --milestone "24085253 Milestone"

# Repository insights
gh api repos/cits5206Group9/SmallGoods-Competition-app/stats/contributors
gh workflow list
gh workflow run
```

---

## Python Development CLI

### Virtual Environment Management
```bash
# Environment setup
python -m venv venv
source venv/bin/activate  # macOS/Linux
pip install -r requirements.txt

# Dependency management
pip freeze > requirements.txt
pip install coverage pytest flask-socketio
```

### Testing and Coverage
```bash
# Test execution
python -m pytest tests/ -v
python -m pytest testing/timer_test.py testing/realtime_test.py -v

# Coverage analysis
coverage run --source=app,testing -m pytest testing/
coverage report --include="app/*,testing/*"
coverage html --include="app/*,testing/*"

# Test result: 15 passed, 26% overall coverage, 85%+ core modules
```

### Flask Development Server
```bash
# Development server management
export FLASK_APP=app
export FLASK_ENV=development
flask run --host=0.0.0.0 --port=5000
flask db migrate -m "Add athlete models"
flask db upgrade
```

---

## Database Management CLI

### SQLite Operations
```bash
# Database inspection
sqlite3 instance/competition.db
.tables
.schema athletes
.schema competitions

# Data queries for testing
SELECT * FROM athletes WHERE competition_id = 1;
SELECT * FROM attempts ORDER BY timestamp DESC LIMIT 10;
```

### Migration Management
```bash
# Alembic migrations
alembic revision --autogenerate -m "Add real-time sync tables"
alembic upgrade head
alembic downgrade -1
alembic history
```

---

## Development Productivity CLI

### File Operations
```bash
# Project structure navigation
find . -name "*.py" -type f | grep -E "(models|routes)" | head -10
grep -r "WebSocket" app/ --include="*.py"
find . -name "requirements*.txt" -exec cat {} \;

# Log analysis
tail -f logs/application.log
grep -i error logs/application.log
```

### Build and Deployment
```bash
# Docker operations (if applicable)
docker build -t smallgoods-app .
docker run -p 5000:5000 smallgoods-app
docker-compose up -d

# Package management
pip list --outdated
pip install --upgrade package_name
```

---

## Documentation and Reporting CLI

### Coverage Report Generation
```bash
# HTML coverage report creation
coverage run -m pytest testing/timer_test.py testing/realtime_test.py testing/simple_test.py
coverage html
open htmlcov/index.html  # View in browser
```

### Git Statistics and Reports
```bash
# Contribution analysis
git log --author="24085253" --oneline --since="2025-07-01" --until="2025-09-30"
git shortlog -sn --since="2025-07-01"
git log --stat --author="24085253" | head -50

# Branch analysis
git branch -vv
git log --graph --oneline --all --since="1 month ago"
```

---

## CLI Usage Statistics

### Development Metrics
- **Git commits**: 50+ commits across feature branches
- **GitHub CLI operations**: Issue management, PR workflow, repository insights
- **Testing commands**: 15 tests executed with coverage analysis
- **Database operations**: Schema migrations, data queries for validation

### Workflow Efficiency
- **Branch management**: 3 feature branches (login-page-dev, realtime-competition-sync, feature-athlete)
- **Automated testing**: Coverage reports with 26% overall, 85%+ core modules
- **Code review**: CLI-based PR management and review workflow
- **Issue tracking**: Milestone management via GitHub CLI

### Technical Proficiency Demonstrated
- **Git mastery**: Advanced branching, merging, conflict resolution
- **GitHub integration**: CLI-based project management and collaboration
- **Python development**: Virtual environments, testing, coverage analysis
- **Database management**: SQLite queries, migration workflows
- **Build tools**: Flask development server, package management

---

## Command Examples Used in Project

### Real-time Feature Development
```bash
# Feature branch creation for WebSocket implementation
git checkout -b realtime-competition-sync
git add app/real_time/
git commit -m "Implement real-time competition data synchronization"
git push -u origin realtime-competition-sync

# Testing WebSocket functionality
python -m pytest testing/realtime_test.py -v
coverage run testing/realtime_test.py
```

### Athlete Dashboard Implementation
```bash
# Feature development workflow
git checkout -b feature-athlete
git add app/routes/athlete.py app/templates/athlete/
git commit -m "Add comprehensive athlete dashboard with live timer"
gh pr create --title "Feature: Athlete Dashboard Implementation"
```

### Database Schema Updates
```bash
# Model changes and migration
git add app/models.py
git commit -m "Update athlete and competition models for real-time sync"
flask db migrate -m "Add athlete entry and attempt models"
flask db upgrade
```

---

**Documentation Date**: September 30, 2025
**Student**: Chenglin Hou (24085253)
**Project**: CITS5206 SmallGoods Competition App