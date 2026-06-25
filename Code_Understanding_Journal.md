# Code Understanding Journal

## Exercise Part 1: Understanding a Specific Feature

### Feature: Task Creation and Status Updates

#### Files Involved
- cli.py
- task_manager.py
- models.py
- storage.py

#### Main Components
- cli.py handles user commands.
- task_manager.py contains business logic.
- models.py defines Task, TaskPriority, and TaskStatus.
- storage.py handles data persistence.

#### Task Creation Flow
1. User enters a command.
2. cli.py processes the command.
3. task_manager.py creates a task.
4. storage.py saves the task.
5. User receives confirmation.

#### Task Status Update Flow
1. User selects a task.
2. cli.py receives the request.
3. task_manager.py updates the task status.
4. storage.py saves the changes.
5. User receives confirmation.

#### Data Storage
Task data is stored and retrieved through storage.py.

---

## Exercise Part 2: Deepening Understanding

### Initial Understanding
I initially believed task priorities were simple labels assigned to tasks.

### What I Discovered
Task priorities are implemented using the TaskPriority enumeration:

- LOW
- MEDIUM
- HIGH
- URGENT

### Key Insights
- Priorities are standardized through enums.
- Priorities can be used for filtering and organizing tasks.
- Business logic relies on these values.

### Misconceptions
I originally thought priorities were stored as plain text values.

---

## Exercise Part 3: Mapping Data Flow

### Marking a Task as Complete

User
→ cli.py
→ task_manager.py
→ models.py
→ storage.py
→ saved data

### State Changes

Before:
- TODO

After:
- DONE

### Potential Failure Points

- Invalid task ID
- Storage failure
- Invalid state transition

### Persistence

Changes are saved through storage.py after task status is updated.

---

## Exercise Part 4: Reflection

### Application Architecture

- User Interface Layer (CLI)
- Business Logic Layer
- Domain Model Layer
- Storage Layer

### Interesting Design Pattern

The use of enums for TaskPriority and TaskStatus ensures consistency and prevents invalid values.

### Most Challenging Part

Understanding how data moves through multiple files.

### How AI Helped

AI helped explain:
- Project structure
- Data flow
- Domain models
- Relationships between components

### Conclusion

This exercise improved my understanding of unfamiliar codebases and demonstrated how AI can assist with software comprehension and learning.
