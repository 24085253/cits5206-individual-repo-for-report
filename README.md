# CITS5206 Individual Coverage Reports and Documentation

**Student**: Chenglin Hou (24085253)
**Project**: SmallGoods Competition App
**Team**: Team 32

## Coverage Reports

### Test Coverage Report
- **Live Coverage Report**: [View Coverage Report](https://24085253.github.io/cits5206-individual-repo-for-report/docs/coverage/)
- **Total Coverage**: 26% (Project files focus on real-time features and testing framework)
- **Key Modules Tested**:
  - `app/models.py`: 97% coverage
  - `app/config.py`: 86% coverage
  - `app/real_time/timer_manager.py`: 85% coverage
  - `testing/realtime_test.py`: 81% coverage
  - `testing/timer_test.py`: 70% coverage

### Coverage Highlights

#### Highly Tested Components (>80% coverage):
- **Database Models** (`app/models.py`): 97% - Comprehensive model testing
- **Configuration Management** (`app/config.py`): 86% - Environment and config validation
- **Timer Management System** (`app/real_time/timer_manager.py`): 85% - Real-time timer functionality
- **Real-time Testing Suite** (`testing/realtime_test.py`): 81% - WebSocket and real-time features

#### Test Categories:
- **Timer Tests**: Competition timer functionality and threading
- **Real-time Tests**: WebSocket communication and event handling
- **Integration Tests**: End-to-end system testing
- **Unit Tests**: Individual component validation

## Documentation

This repository contains coverage reports and documentation for individual contributions to the CITS5206 SmallGoods Competition App project.

### Features Implemented:
- Real-time competition timer system
- WebSocket-based athlete dashboard
- Timer management and synchronization
- Comprehensive testing framework

### Test Results Summary:
- **15 tests passed** (timer_test.py, realtime_test.py, simple_test.py)
- **Test coverage focus**: Real-time features, database models, configuration
- **Performance**: Real-time response ≈ 50ms for WebSocket events

---
*Generated on: September 30, 2025*
*Repository: https://github.com/cits5206Group9/SmallGoods-Competition-app*