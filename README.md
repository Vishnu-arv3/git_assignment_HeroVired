Git Assignment - HeroVired

Repository Name

git_assignment_HeroVired

---

Author

Vishnu Kumar

---

Project Overview

This repository contains solutions for the HeroVired Git assignment.
It demonstrates practical usage of Git workflows including branching, merging, pull requests, Git LFS, and Git stash through Python-based projects.

---

Q1: CalculatorPlus Application

Objective

Enhance an existing Python calculator application by:

* Adding a square root feature
* Fixing a critical bug in division
* Following proper Git workflow (branches, PRs, merging)

---

Steps Performed

1. Repository Setup

* Created a private GitHub repository
* Cloned it locally

2. Branch Creation

* Created `dev` branch for development

```bash
git checkout -b dev
```

3. Implemented Calculator

* Added basic operations:

  * Addition
  * Subtraction
  * Multiplication
  * Division

4. Added Square Root Feature

```python
def square_root(self, x):
    return math.sqrt(x)
```

5. Initial Merge & Release

* Merged `dev` → `main`
* Created version:

```bash
git tag v1.0
```

---

Bug Fix

Issue:

Division by zero was not handled.

Fix:

```python
def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b
```

---

Feature Development Workflow

Created Feature Branch

```bash
git checkout -b feature/sqrt
```

Updated Feature Branch

* Synced with `dev`

```bash
git merge dev
```

Pull Request

* Created PR → `main`
* Code review performed
* Changes merged into `dev`

---

Final Merge & Release

* Merged `dev` → `main`
* Created version:

```bash
git tag v2.0
```

---

Q2: Git LFS (Large File Storage)

Objective

Manage large files efficiently using Git LFS.

---

Steps Performed

1. Installed Git LFS

```bash
git lfs install
```

2. Created Branch

```bash
git checkout -b lfs
```

3. Tracked Large Files

```bash
git lfs track "*.zip"
```

4. Added Large File (>200MB)

```bash
git add .gitattributes
git add largefile.zip
git commit -m "Added large file using Git LFS"
git push origin lfs
```

---

Verification

* Cloned repository on another system
* Verified file downloaded correctly via LFS

---

Q3: Geometry Calculator with Git Stash

Objective

Implement:

* Area of Circle
* Area of Rectangle
  Using Git Stash for managing incomplete work.

---

Workflow

1. Created Branch

```bash
git checkout -b geometry-calculator
```

---

Circle Area Feature

Branch:

```bash
git checkout -b feature/circle-area
```

Stashed Work

```bash
git stash
```

Completed Implementation

```python
radius = 5
print(f"Area of circle = {calculator.calculate_circle_area(radius)}")
```

Commit & Push

```bash
git add .
git commit -m "Completed circle area feature"
git push origin feature/circle-area
```

---

Rectangle Area Feature

Branch:

```bash
git checkout -b feature/rectangle-area
```

Stashed Work

```bash
git stash
```

Completed Implementation

```python
length = 10
width = 6
print(f"Area of rectangle = {calculator.calculate_rectangle_area(length, width)}")
```

Commit & Push

```bash
git add .
git commit -m "Completed rectangle area feature"
git push origin feature/rectangle-area
```

---

Pull Requests & Merge

* Created PRs → `dev`
* Code reviewed
* Merged into `dev`
* Finally merged into `main`

---

Key Concepts Demonstrated

* Git Branching Strategy
* Feature Branch Workflow
* Pull Requests & Code Reviews
* Merge Conflict Resolution
* Git Tags (Versioning)
* Git LFS (Large File Handling)
* Git Stash (Work in Progress Management)

---

Project Structure

```
git_assignment_HeroVired/
│── calculator.py
│── geometry_calculator.py
│── README.md
│── .gitattributes
```

---

Submission Notes

* Repository initially kept private
* Will be made public after submission deadline
* Collaborator added for code review

---

Conclusion

This assignment demonstrates real-world Git workflows used in collaborative software development, including handling features, bugs, large files, and multiple development tasks efficiently.

---
