# 🚀 FOSSEE Internship 2026 — My Open Source Journey

<p align="center">
  <img src="https://img.shields.io/badge/Internship-FOSSEE%202026-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Organization-IIT%20Bombay-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-eSim%20%7C%20Automation-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Ongoing-brightgreen?style=for-the-badge" />
</p>

<p align="center">
  <b>Learning by Building. Growing by Contributing. Improving Through Open Source.</b>
</p>

---

## 👨‍💻 About This Journey

Welcome to my **FOSSEE Semester Long Internship – Autumn 2026** repository!

I'm **Sumit Kumar Jha**, a Computer Science and Engineering student, and this repository documents my technical journey, contributions, research, experiments, challenges, and progress throughout the internship.

This is more than a collection of daily updates. It is a record of how I approach real-world software engineering problems, investigate existing systems, understand unfamiliar codebases, test solutions, and continuously improve my development skills.

My internship work revolves around **eSim**, an open-source Electronic Design Automation (EDA) tool developed under the FOSSEE project at IIT Bombay.

---

## 🎯 Internship Focus

### Major Task: Automation Circuit/Tasks Verification Strategy

My major task focuses on exploring and improving the verification strategy for automation-related circuits and tasks in eSim.

Key areas of exploration include:

- Understanding eSim's existing architecture and workflow.
- Investigating automated verification processes.
- Exploring circuit and simulation validation.
- Testing software modules and identifying compatibility issues.
- Improving test reliability across operating systems.
- Documenting technical findings and proposed improvements.

### Current Technical Focus

**Windows Compatibility and Test Reliability**

An important part of my ongoing work involves investigating Windows-specific compatibility issues in eSim's testing infrastructure.

Areas explored include:

- Toolchain detection and validation.
- Windows executable resolution.
- MSYS2 and MinGW integration.
- GHDL backend validation.
- Icarus Verilog and VVP validation.
- Co-simulation dependency checks.
- Cross-platform automated testing.

---

## 🛠️ Technology & Tools

| Category | Technologies |
|---|---|
| Programming | Python |
| Testing | Pytest |
| Version Control | Git & GitHub |
| Development Environment | Visual Studio Code |
| Operating System | Windows 11 |
| Simulation Tools | Ngspice, GHDL, Icarus Verilog |
| Build Tools | MinGW, GCC, Verilator, Make |
| Environment | Python Virtual Environment |

---

## 📂 Repository Structure

```text
fossee-esim-internship-2026/
│
├── daily-updates/
│   ├── Day 01 - ...
│   ├── Day 02 - ...
│   ├── ...
│   ├── Day 36 - Windows Compatibility Investigation
│   ├── Day 37 - Actual Windows Toolchain Diagnostic
│   ├── Day 38 - Windows Toolchain Test Investigation
│   ├── Day 39 - GHDL Backend Test Fixes
│   ├── Day 40 - Icarus Verilog and libvvp Test Fixes
│   └── Day 41 - Toolchain Test Suite Validation
│
├── eSim/
│   └── eSim source code and development workspace
│
├── Meeting_notes/
│   └── Internship meeting notes and discussions
│
├── research/
│   └── README.md
│
└── README.md
```

*The daily-updates folder contains individual progress reports. The eSim folder contains the working source-code checkout.*

---

## 📈 Technical Progress & Milestones

### Milestone 1 — Understanding the eSim Codebase
- Explored the project structure and important modules.
- Studied the existing testing infrastructure.
- Identified relevant components for the major task.

### Milestone 2 — Testing and Environment Investigation
- Set up the local development environment.
- Executed different module-level test suites.
- Investigated Windows-specific testing behaviour.
- Checked the availability and configuration of simulation tools.

### Milestone 3 — Windows Toolchain Investigation
- Investigated `ToolchainCheck.py` and `CosimConfig.py`.
- Examined Windows executable resolution.
- Verified MSYS2 and MinGW tool detection.
- Compared actual Windows toolchain behaviour with automated test fixtures.

### Milestone 4 — Improving Test Reliability
- Updated GHDL backend tests using mocks.
- Improved Icarus Verilog and libvvp validation tests.
- Updated toolchain test fixtures for Windows compatibility.
- Validated toolchain requirement checks.

### Milestone 5 — Toolchain Test Validation

**Latest verified result:**

```text
Test File: src/maker/tests/test_toolchain_check.py

Total Tests: 15
Passed:      15
Failed:       0

Status: SUCCESS
```

Command used:

```powershell
python -m pytest src/maker/tests/test_toolchain_check.py -v
```

All 15 tests passed successfully in the Windows environment.

*This result applies to the specified test file, not the entire eSim test suite.*

---

## Windows Compatibility Investigation – Progress Through Day 47

**Period:** 2–7 November 2026  
**Major Task:** Automation Circuit/Tasks Verification Strategy

Continued investigating Windows compatibility issues in the eSim test suite, focusing on Maker modules, HDL parsing, simulation toolchain validation and process lifecycle management.

### Key Contributions

#### 1. Maker Test-Suite Investigation
- Investigated Windows-specific test failures and dependency-related collection issues.
- Examined platform-specific assumptions in test fixtures and external-tool execution.

#### 2. HDL Parser Dependency Compatibility
- Investigated the legacy hdlparse package compatibility issue with Python 3.13.
- Applied a local workaround inside the Python virtual environment.
- Verified Verilog and VHDL parser imports.

#### 3. HDL Structure and Port Parsing
- Improved port extraction fallback handling.
- Used regex-derived information to recover missing port widths.
- Validated parameter-dependent port widths and testbench generation.

#### 4. ToolchainCheck Windows Compatibility
- Updated platform-specific fake toolchain fixtures.
- Added Windows executable naming and MSYS2/MinGW directory layouts.
- Improved unit-test coverage for GHDL backend detection and libvvp validation.

#### 5. Process Lifecycle Testing
- Replaced Unix-specific process commands with Python interpreter subprocesses.
- Added cleanup safeguards to prevent child processes from remaining active after test failures.
- Validated Popen and QProcess lifecycle behaviour.

### Verified Test Results

| Validation | Result |
|---|---:|
| Complete Maker test suite | 570 passed, 10 skipped |
| HDL structure tests | 39 passed |
| Port parsing tests | 5 passed |
| ToolchainCheck tests | 15 passed |
| Process lifecycle tests | 8 passed |

### Current Status

The reported Maker test-suite execution completed without failures on Windows.

The 570 passed and 10 skipped result applies specifically to the Maker test suite, not the complete eSim repository.

The hdlparse compatibility workaround was applied only to the local virtual environment and was not committed as an eSim source-code or dependency-file change.

### Follow-up Work
- Complete the review of all modified files.
- Perform any remaining regression checks.
- Document unresolved compatibility limitations.
- Continue coordination with the internship mentor.
- Maintain daily GitHub progress documentation.

**Day 47 documentation and final-review status should be updated after the day's actual work is completed.**

## 📅 Daily Development Log

Every working day is documented separately to maintain a transparent record of progress.

Each daily update may include:

- Tasks and objectives.
- Technical investigation.
- Implementation and testing.
- Errors encountered and debugging.
- Results and observations.
- Next steps.

📁 Explore the [`daily-updates`](./daily-updates) folder for the development history.

---

## 🔬 Research & Documentation

The `research/` directory contains supporting research material, technical observations, and investigation notes related to the internship.

The `Meeting_notes/` directory maintains important discussions, guidance, decisions, and follow-up tasks from internship meetings.

These records help connect technical implementation with the overall project objectives.

---

## 🧠 What I'm Learning

This internship is helping me develop practical experience in:

- Working with an existing open-source codebase.
- Understanding software architecture and module dependencies.
- Writing and debugging Python code.
- Designing and executing automated tests.
- Investigating operating-system-specific issues.
- Working with simulation and development tools.
- Using Git branches and maintaining development history.
- Documenting technical work professionally.
- Understanding collaborative software development practices.

---

## 🔄 Development Workflow

My general workflow throughout this internship:

```text
Understand the Requirement
          ↓
Explore the Existing Codebase
          ↓
Identify the Problem
          ↓
Investigate Possible Causes
          ↓
Implement or Improve the Solution
          ↓
Run Automated Tests
          ↓
Analyse Test Results
          ↓
Document Daily Progress
          ↓
Plan the Next Milestone
```

---

## 🌱 Beyond the Code

I believe meaningful open-source contributions are not only about writing code.

They also involve:

- Asking the right technical questions.
- Understanding why something fails.
- Reading and analysing existing implementations.
- Testing assumptions instead of making guesses.
- Learning from feedback.
- Making improvements that are reliable and maintainable.

This repository represents that learning process.

---

## 🙏 Acknowledgement

I'm grateful to **FOSSEE, IIT Bombay**, for this opportunity to learn, explore, and contribute to an open-source engineering project.

Special thanks to my internship mentor and the FOSSEE team for their guidance, feedback, and support throughout this journey.

---

## 📌 Current Status

**Internship:** FOSSEE Semester Long Internship – Autumn 2026  
**Project:** eSim  
**Major Task:** Automation Circuit/Tasks Verification Strategy  
**Current Focus:** Windows Compatibility & Automated Test Reliability  
**Latest Verified Milestone:** 15/15 Toolchain Tests Passed  
**Development Status:** Ongoing

---

<p align="center">
  <b>One Commit at a Time. One Problem at a Time. One Step Closer to Better Engineering.</b>
  <br/>
  <i>Documenting the journey, not just the destination.</i>
</p>