                        Ex.No.9: Analyzing Suspicious Processes with Process Explorer 

**Overview**  
**Process Explorer** is a powerful Windows tool that provides detailed insights into running processes. It helps monitor system activity, troubleshoot issues, and detect potentially malicious or unusual processes. 🔍

---

### Step 1: Download and Launch Process Explorer 

* **Get Process Explorer:**  
  Visit the Microsoft Sysinternals website and download the tool.
  link:-https://learn.microsoft.com/en-us/sysinternals/downloads/process-explorer
* **Extract Files:**  
  Unzip the downloaded package into a dedicated folder. 
* **Run as Administrator:**  
  Open the folder and launch `procexp64.exe` or `procexp.exe` by right-clicking and selecting **Run as Administrator**. 🛡️
  
<img width="1365" height="767" alt="Screenshot 2025-10-27 213149" src="https://github.com/user-attachments/assets/beb4f208-7054-4e4c-8cff-cec02e86344a" />

---

### Step 2: Explore the Interface 

Process Explorer displays processes in a hierarchical tree structure. Each process is **color-coded** based on its status:

| Color | Description |
| :--- | :--- |
| **Pink** | Suspended processes |
| **Light Blue** | Processes running under your account  |
| **Dark Blue** | System services or processes  |
| **Green** | Newly started processes  |
| **Red** | Recently terminated processes  |

---

### Step 3: Spotting Suspicious Processes 

To investigate potentially harmful processes:

1. **Check Unknown Processes:**  
   Look for unfamiliar names. Trusted processes usually come from known vendors like Microsoft, Adobe, or Intel. 
2. **Verify Digital Signatures:**  
   Right-click → **Properties** → **Image** tab. Check for a valid **Digital Signature**. Unsigned processes may be risky. 
3. **Examine File Paths:**  
   Check the **Path** under the Image tab. Legitimate system processes are usually in `C:\Windows\System32`. Running from temp or user folders is suspicious. 
4. **Monitor Resource Usage:**  
   Watch for processes consuming excessive CPU, memory, or disk resources without explanation. 
5. **Review Process Details:**  
   Lack of description or unclear company names can indicate a suspicious process. 
6. **Inspect Network Activity:**  
   Right-click → **Properties** → **TCP/IP** tab. Unexpected external connections require attention. 

---
<img width="787" height="591" alt="Screenshot 2025-10-27 213216" src="https://github.com/user-attachments/assets/c3817bb0-b496-4c92-9e17-d1ce1bd2b2a6" />



### Step 4: Research Suspicious Processes 

* Search the process name online (e.g., `cmd.exe`) to learn more about it. 
* Use databases like **VirusTotal** or **ProcessLibrary** to check for known malware. 


<img width="782" height="598" alt="Screenshot 2025-10-27 213346" src="https://github.com/user-attachments/assets/78182b1a-c7a4-4bc3-a5bf-2d08fcd4ce28" />

---

### Step 5: Handle Malicious or Unwanted Processes 

* **Terminate:** Right-click → **Kill Process** to stop it immediately.   
* **Suspend:** Right-click → **Suspend** to pause execution temporarily.  
* **Delete Source:** Locate the executable via its Path and remove it if confirmed malicious. 

---

<img width="776" height="584" alt="Screenshot 2025-10-27 213359" src="https://github.com/user-attachments/assets/7b652e63-1403-41ac-8b37-806d0f6bf431" />



<img width="773" height="590" alt="Screenshot 2025-10-27 213432" src="https://github.com/user-attachments/assets/ecab9c3e-3d93-4adc-9e6c-ba218db8ae63" />



---

### Step 6: Conduct a Full System Scan 

* Run a comprehensive antivirus scan. 
* Use malware removal tools (e.g., Malwarebytes or Windows Defender) for a thorough cleanup. 
