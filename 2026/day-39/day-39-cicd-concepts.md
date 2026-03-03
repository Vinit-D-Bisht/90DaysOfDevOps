Today I learned why CI/CD exists and what problems it solves.
No pipelines today — only concepts.

---

## Task 1: The Problem (Without CI/CD)

### Scenario
5 developers are working on the same project and deploying manually.

### What can go wrong?
- One developer overwrites another’s code
- Bugs go directly to production
- No proper testing before deployment
- Manual steps cause mistakes
- Fixing production issues becomes stressful

### What does “It works on my machine” mean?
It means:
- The code works on a developer’s laptop
- But fails on server or production

This happens because:
- Different OS
- Different software versions
- Missing environment variables

### How many times can a team deploy manually?
- Mostly **1 or 2 times per day**
- More than that = high risk and errors

---

## Task 2: CI vs CD (Simple Definitions)

### Continuous Integration (CI)
CI means:
- Code is automatically tested every time we push code
- It checks if the new code breaks anything

**Example:**  
When you push code → tests run automatically

---

### Continuous Delivery (CD)
CD means:
- Code is always ready to deploy
- Deployment needs manual approval

**Example:**  
Tests pass → click a button → deploy

---

### Continuous Deployment
Continuous Deployment means:
- Every change that passes tests goes to production automatically
- No manual approval

**Example:**  
Push code → tests pass → live to users

---

## Task 3: Pipeline Parts (Easy Explanation)

### Trigger
- What starts the pipeline  
- Example: code push

### Stage
- Big steps in pipeline  
- Example: test, build, deploy

### Job
- Work inside a stage  
- Example: run tests

### Step
- Single command  
- Example: `npm install`

### Runner
- Machine that runs the pipeline  
- Example: GitHub runner

### Artifact
- Output of a job  
- Example: build files or Docker image

---

## Task 4: Simple CI/CD Pipeline Diagram

Code -> Test -> Build -> Deploy

---

## Task 5: Open Source Example

### Repository Checked
FastAPI GitHub repo

### Workflow Trigger
- On code push
- On pull request

### Jobs
- Run tests
- Check code style

### What it does
- Makes sure new changes don’t break the app

---

## What I Learned Today

1. CI/CD makes software delivery safer
2. Automation reduces human mistakes
3. Pipeline failure means problem found early 