                                        Ex. No. 10: Use Ghidra to Disassemble and Analyze the Malware Code



---

## Project Objectives

* To provide a hands-on guide to disassembling and analyzing malware with **Ghidra**.  
* To enable readers to recognize common malware functionalities such as **persistence mechanisms**, **anti-analysis techniques**, and **network communications**.  
* To equip users with the skills to interpret **low-level assembly code** and understand **high-level behaviors** using Ghidra's decompiler.

---

## Prerequisites

* **Ghidra:** Installed and configured (requires Java Development Kit - JDK).  
* **Virtual Machine (VM):** A secure, isolated environment (e.g., VMWare, VirtualBox) to safely handle binaries.  
* **Sample Binary:** A benign or safe hex dump for analysis.  

---

##  Project Outline (GitHub Repository Components)

###  1. Repository Root

| File/Folder | Description |
| :--- | :--- |
| `README.md` | Overview of Ghidra, project requirements, and tutorial outline. |
| `templates/` | For documenting forensic analysis findings. |
| `docs/` | Contains step-by-step analysis tutorials. |
| `scripts/` | Stores automation scripts (Python/Java) for Ghidra. |
| `samples/` | Stores benign binaries or hex dumps for analysis. |

---

###  2. Tutorial Steps (`docs/Tutorial_StepX.md`)

####  A. Environment Setup
* Setting up a virtual machine and installing Ghidra.  
* Verifying JDK dependencies.  

![Ghidra Setup](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.18.png)

---

####  B. Initial Analysis
* **Loading the Binary:** Launch Ghidra, create a new project, and import the binary.  
* **Auto-Analysis:** Run Ghidra’s auto-analysis and choose analyzers.  
* **Entry Points:** Locate the `main()` or starting point of execution.  

![Binary Load](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.15.png)

![Entry Point](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.14.png)

---

#### C. Function Analysis
* **Decompiler:** Converts assembly into C-like code.  
* **Function Renaming:** Helps identify critical operations.  
* **Cross-Referencing (XREF):** Trace variable usage and function calls.  

![Decompiled View](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.11.png)

![Function XREF](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.10.png)

---

#### 🧵 D. String and Import Analysis
* **Strings:** Find static indicators like URLs, registry keys, or file paths.  
* **Imports:** Identify suspicious API calls like `CreateFileA`, `URLDownloadToFile`, etc.  

![Strings Window](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.9.png)

![Import Table](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.7.png)

---

####  E. Advanced Techniques (Optional)
* **Control Flow Graphs (CFGs):** Visualize execution flow.  
* **Custom Scripts:** Automate tasks with Ghidra’s scripting API (Python/Java).

---

### 3. Example Automation Scripts (`scripts/`)

| Script | Purpose |
| :--- | :--- |
| `extract_strings.py` | Extracts and lists all string references. |
| `network_analysis.py` | Detects functions with network-related API calls. |
| `label_functions.py` | Labels functions with known malicious patterns. |

---

###  4. Sample Data (`samples/`)

* Safe binaries for practice. Example:  
  `benign_sample1.bin` – A harmless C program mimicking system calls.  

![Sample Analysis](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.4.png)
![Code Analysis](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.3.png)
![Execution Flow](https://github.com/baddiputi/Digital-Forensic-Lab-Exercises/blob/97de06473d645e6627f8ffd9004efdb5c19742a8/images/10.2.png)

---

###  5. Report Template

1. **Summary of Analysis:** Overview of the malware sample and analysis scope.  
2. **Function Analysis:** Summary of key functions and findings.  
3. **Behavioral Indicators:** Observed behaviors (e.g., persistence, communication).  
4. **Recommendations:** Containment or further dynamic analysis.

---

##  **Result**

 The experiment on malware analysis using **Ghidra** was successfully performed.  
 The malware binary was **disassembled, decompiled, and analyzed** to identify its functions, strings, and behavioral patterns.  
 This analysis provided insights into its **internal logic, persistence mechanisms,** and **potential malicious activities**.

---
