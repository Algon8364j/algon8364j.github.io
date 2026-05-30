# IT Project: Refinement, Ethical Integration, and Peer Review
*Documentation detailing extensive technical and ethical code enhancements executed on a previous project archive.*

---

## 📦 Project Overview & Narratives
* **Selected Project Base:** Inventory Management System Script (Python / SQLite Backend)
* **Core Technical Purpose:** To track asset movements, manage warehouse stock thresholds, and produce automated relational query logs.
* **Comprehensive Narrative:** This project tracks my growth as an engineer. While the initial build focused entirely on basic functionality, this refined version blends technical optimizations with explicit ethical constraints regarding accessibility and security.

---

## 🔧 Extensive Refinements & Decision-Making Process

### 1. Security Optimization (Technical Refinement)
* **The Challenge:** The initial codebase utilized raw string formatting to construct SQL statements, exposing the entire database structure to destructive SQL Injection vulnerabilities.
* **The Refinement:** I completely refactored the database query tier to use **parameterized queries** and prepared statements natively.
* **Spiritual/Ethical Justification:** Keeping user data secure is an immediate extension of the principle of *Digital Stewardship*. Protecting data keeps it safe from bad actors.

### 2. Accessibility Remediation (Ethical Refinement)
* **The Challenge:** The user logs and system outputs were rendered in tightly packed, poorly structured plain text blocks, which completely broken screen readers and violated accessibility guidelines.
* **The Refinement:** I refactored the presentation structure to output clean semantic HTML landmarks, integrated explicit **ARIA labels**, and verified that all color contrast ratios met WCAG 2.2 Level AA guidelines.
* **Spiritual/Ethical Justification:** Aligns directly with *Universal Inclusivity*. No user should be excluded from using a system due to physical barriers.

### 3. Data Minimization Controls (Ethical Refinement)
* **The Challenge:** The database indefinitely stored historical employee tracking telemetry long after it lost its business utility.
* **The Refinement:** I programmed an automated retention cycle script that securely overwrites and purges identifying log records after 90 days.
* **Spiritual/Ethical Justification:** Adheres to the principle of *Fairness and Respect for Privacy*, ensuring we do not hoard user tracking histories needlessly.

---

## 🤝 Peer Review Evaluation & Integration Report

### **Feedback Collected**
During the Week 4 peer review session, my classmate evaluated my code and noted that while the query parameterization was excellent, the application's internal script exceptions were being printed directly to the standard output screen. If an unhandled exception occurred, it leaked raw directory paths and server structures to the end-user window.

### **Actioned Refinement**
Taking this constructive peer feedback, I immediately went back to the code and implemented a robust, multi-tier **Try-Catch Exception Handling block**. 

Instead of printing raw stack traces to the user interface, the system now catches exceptions internally, writes the diagnostic details to a local, heavily encrypted file (`error_log.db`), and passes a polite, generic warning message to the end-user. This change fixed the security leak while keeping the app professional and clean.
