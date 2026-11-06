# 🚀 FOSSEE Internship 2026 — My Open Source Journey

<p align="center">
  <img src="https://img.shields.io/badge/Internship-FOSSEE%202026-blue?style=for-the-badge" alt="FOSSEE Internship 2026" />
  <img src="https://img.shields.io/badge/Organization-IIT%20Bombay-orange?style=for-the-badge" alt="IIT Bombay" />
  <img src="https://img.shields.io/badge/Project-eSim-success?style=for-the-badge" alt="eSim Project" />
  <img src="https://img.shields.io/badge/Status-Ongoing-brightgreen?style=for-the-badge" alt="Ongoing Internship" />
</p>

<p align="center">
  <b>Learning by Building. Growing by Contributing. Improving Through Open Source.</b>
</p>

---

## 👨‍💻 About This Journey

Welcome to my **FOSSEE Semester Long Internship – Autumn 2026** repository!

I'm **Sumit Kumar Jha**, a Computer Science and Engineering student. This repository documents my technical journey, research, experiments, implementation work, testing activities, challenges, and progress throughout the internship.

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
- HDL parsing and port extraction.
- Process lifecycle management.
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
│   ├── day-01-...
│   ├── day-02-...
│   ├── ...
│   ├── day-36-windows-compatibility-toolchain-investigation.md
│   ├── day-37-actual-windows-toolchain-diagnostic.md
│   ├── day-38-windows-toolchain-test-investigation.md
│   ├── day-39-ghdl-backend-test-fixes.md
│   ├── day-40-icarus-libvvp-test-fixes.md
│   ├── day-41-toolchain-test-suite-validation.md
│   ├── day-42-windows-maker-suite-investigation.md
│   ├── day-43-hdlparse-python313-compatibility.md
│   ├── day-44-hdl-structure-and-port-parsing.md
│   ├── day-45-toolchaincheck-windows-test-fixtures.md
│   ├── day-46-maker-suite-and-process-lifecycle-validation.md
│   └── day-47-final-review-and-documentation-plan.md
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

*The `daily-updates/` folder contains individual internship progress reports. The `eSim/` folder contains the working source-code checkout.*

---

## 📈 Technical Progress & Milestones

### Milestone 1 — Understanding the eSim Codebase

- Explored the project structure and important modules.
- Studied the existing testing infrastructure.
- Identified relevant components for the major task.
- Studied the eSim circuit simulation workflow.

### Milestone 2 — Testing and Environment Investigation

- Set up the local Python development environment.
- Installed and configured testing dependencies.
- Executed existing project validation tests.
- Investigated simulation utilities and data extraction tests.
- Examined frontend and backend testing infrastructure.

### Milestone 3 — Existing Module Validation

- Executed project path regression tests.
- Executed model cache regression tests.
- Investigated process lifecycle functionality.
- Executed simulation utility and mathematical utility tests.
- Documented test results and identified compatibility issues.

### Milestone 4 — Windows Toolchain Investigation

- Investigated `ToolchainCheck.py` and `CosimConfig.py`.
- Examined Windows executable resolution.
- Verified the actual Windows simulation toolchain.
- Investigated MSYS2 and MinGW tool detection.
- Examined GHDL backend requirements.
- Investigated Icarus Verilog, VVP and libvvp validation.
- Compared actual toolchain behaviour with automated test fixtures.

### Milestone 5 — Improving Test Reliability

- Updated GHDL backend tests using mocks.
- Improved Icarus Verilog and libvvp validation tests.
- Updated toolchain test fixtures for Windows compatibility.
- Improved HDL port extraction fallback handling.
- Investigated legacy HDL parser compatibility with Python 3.13.
- Improved process lifecycle tests using cross-platform Python subprocesses.
- Added cleanup safeguards for process-based tests.

### Milestone 6 — Maker Test-Suite Validation

**Latest major verified testing milestone:**

```text
Test Suite: src/maker/tests/

Total Passed: 570
Skipped:       10
Failed:         0

Status: SUCCESS
```

Command used:

```powershell
python -m pytest src/maker/tests/ -v --tb=short
```

The Maker test suite completed successfully in the Windows environment.

**Important:** This result applies specifically to `src/maker/tests/`, not the complete eSim repository.

---

## 🪟 Windows Compatibility Investigation — Progress Through Day 46

**Period:** 26 October – 6 November 2026

Continued investigating Windows compatibility issues in the eSim test suite, focusing on Maker modules, HDL parsing, simulation toolchain validation, and process lifecycle management.

### 1. Maker Test-Suite Investigation

- Investigated Windows-specific test failures and dependency-related collection issues.
- Examined platform-specific assumptions in test fixtures.
- Identified problems involving external-tool execution on Windows.

### 2. HDL Parser Dependency Compatibility

- Investigated the legacy `hdlparse` package compatibility issue with Python 3.13.
- Applied a temporary compatibility workaround inside the local Python virtual environment.
- Verified successful imports of Verilog and VHDL parser modules.

### 3. HDL Structure and Port Parsing

- Improved port extraction fallback handling.
- Used regex-derived information to recover missing port widths.
- Validated parameter-dependent port widths and testbench generation.

### 4. ToolchainCheck Windows Compatibility

- Updated platform-specific fake toolchain fixtures.
- Added Windows executable naming and MSYS2/MinGW directory layouts.
- Improved unit-test coverage for GHDL backend detection and libvvp validation.

### 5. Process Lifecycle Testing

- Replaced Unix-specific process commands with Python interpreter subprocesses.
- Added cleanup safeguards to prevent child processes from remaining active after test failures.
- Validated `subprocess.Popen` and `QProcess` lifecycle behaviour.

### Verified Test Results

| Validation | Result |
|---|---:|
| Complete Maker test suite | 570 passed, 10 skipped |
| HDL structure tests | 39 passed |
| Port parsing tests | 5 passed |
| ToolchainCheck tests | 15 passed |
| Process lifecycle tests | 8 passed |

*These are results from separate test executions. They should not be added together to calculate a total test count.*

### Implementation Note

The `hdlparse` compatibility workaround was applied only to the local virtual environment. It was not committed as an eSim source-code or dependency-file change.

---

## 📅 Daily Development Log

Every working day is documented separately to maintain a transparent record of progress.

Each daily update may include:

- Tasks and objectives.
- Technical investigation.
- Implementation and testing.
- Errors encountered and debugging.
- Test results and observations.
- Next steps.

📁 Explore the [`daily-updates`](./daily-updates) folder for the complete development history.

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

| Detail | Information |
|---|---|
| Internship | FOSSEE Semester Long Internship – Autumn 2026 |
| Organization | FOSSEE, IIT Bombay |
| Project | eSim |
| Major Task | Automation Circuit/Tasks Verification Strategy |
| Current Focus | Windows Compatibility & Automated Test Reliability |
| Latest Verified Milestone | Maker test suite: 570 passed, 10 skipped |
| Development Status | Ongoing |

**Next Focus:** Continue module-wise integrity testing, review Windows compatibility changes, and document remaining findings based on mentor guidance.

---

<p align="center">
  <b>One Commit at a Time. One Problem at a Time. One Step Closer to Better Engineering.</b>
  <br/>
  <i>Documenting the journey, not just the destination.</i>
</p>