# CI/CD – Continuous Integration and Continuous Delivery/Deployment

## What is CI/CD?

CI/CD is a DevOps practice used to automate the process of building, testing, and delivering software.

CI/CD helps development teams release software faster, more reliably, and with fewer manual errors.

CI/CD stands for:

- **CI** – Continuous Integration
- **CD** – Continuous Delivery
- **CD** – Continuous Deployment

---

## 1. Continuous Integration (CI)

Continuous Integration is the practice of frequently integrating code changes into a shared repository.

Whenever a developer pushes code, an automated pipeline can:

1. Checkout the source code
2. Install dependencies
3. Compile/build the application
4. Run automated tests
5. Perform code-quality checks
6. Generate build artifacts

### CI Flow

```text
Developer
    |
    | git push
    v
Git Repository
    |
    v
CI Pipeline
    |
    +----> Build
    |
    +----> Unit Tests
    |
    +----> Code Quality
    |
    +----> Security Checks
    |
    v
Build Artifact
