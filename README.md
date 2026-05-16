# luvbebnajubjub

# Smart Scheduler

Smart Scheduler is a C programming project that automatically creates a task schedule using Graph algorithms, Topological Sort, and Greedy Scheduling.

The system reads tasks from a file, checks dependencies, detects cycles, sorts tasks by priority, and generates a schedule and automatically update in text file.

---

# Features

- Add tasks to `tasks.txt`
- Display all tasks
- Create dependency graph
- Detect cycle in graph
- Topological Sort
- Priority-based scheduling
- Export schedule to `schedule.txt`
- Menu system
- Modular programming using `.c` and `.h`

---

# Algorithms Used

## Graph
Each task is represented as a node.

Dependency:
```
A → B
````

Means:

* Task A must be completed before Task B

---

## Topological Sort

Used to arrange tasks in a valid order based on dependencies.

Algorithm:

* DFS (Depth First Search)

---

## Cycle Detection

Checks whether the dependency graph contains a cycle.

Example:

```
A → B
B → A
```

This is invalid because tasks depend on each other infinitely.

---

## Greedy Scheduling

Tasks are scheduled based on priority.

Lower priority number = more important.

Example:

```
Priority 1 > Priority 5 > Priority 10
```

---

# File Structure

```
main.c
task_manager.c
graph.c
scheduler.c
scheduler.h
tasks.txt
schedule.txt
```

---

# Task Format

Inside `tasks.txt`:

```
name duration deadline priority dependency
```

Example:

```
Math 2 5 1 -1
HW 1 6 3 0
Project 3 10 5 1
```

---

# Field Description

| Field      | Description                    |
| ---------- | ------------------------------ |
| name       | Task name                      |
| duration   | Time required                  |
| deadline   | Finish before this time        |
| priority   | Lower number = higher priority |
| dependency | Required previous task         |

---

# Example Dependency

```
Math → HW → Project
```

---

# Compilation

```
gcc main.c task_manager.c graph.c scheduler.c -o scheduler
```

---

# Run Program

## Windows

```
./scheduler
```

---

# Menu

```
===== SMART SCHEDULER =====
1. Add Task
2. Generate Schedule
3. Display Tasks
4. Exit
```

---

# Example Output

```
=== SCHEDULE ===
Math : 0 -> 2
HW : 2 -> 3
Project : 3 -> 6
```

---

# Technologies Used

* C Programming
* File Handling
* Graph
* DFS
* Topological Sort
* Greedy Algorithm
* Modular Programming

---

# Team Responsibilities

## MS.Wilasinee Sornwilai (68070503454)

* File handling
* Task management
* Menu system

## MS.Ployvalanch Yensanit (68070503477)

* Graph
* DFS
* Cycle detection
* Topological Sort

## MR.Yanadet Somprasert (68070503487)

* Priority scheduling
* Schedule generation
* File handling
* Exporting and updating schedule files

---

