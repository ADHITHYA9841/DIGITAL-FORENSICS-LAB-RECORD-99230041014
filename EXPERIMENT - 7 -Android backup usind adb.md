                                                           Experiment 7 
                                       Android Device Forensic Acquisition using ADB Logical Backup

---
## Aim
To perform logical acquisition of data from an Android device using Android Debug Bridge (ADB) backup functionality.

---

## Description
This experiment demonstrates the forensic acquisition of data from an Android device using ADB's built-in backup functionality. The process includes creating a logical backup, verifying its integrity through hashing, and analyzing the extracted contents while maintaining forensic principles.

---
## Tools Used
1. Android Debug Bridge (ADB)
2. Android Device
3. USB Cable
4. Android Backup Extractor (abe.jar)
      .Download Android Backup Extractor from GitHub:
   ```bash
   git clone https://github.com/nelenkov/android-backup-extractor/releases/tag/latest
   ```
5. SHA256 hashing tool

---
## Prerequisites
1. Android device with:
   - USB debugging enabled
   - At least 50% battery life
   - Device unlocked and screen active
2. Computer with:
   - ADB installed and configured
   - Java Runtime Environment (JRE)
   - Required USB drivers installed

---
## Procedure

### 1. Device Connection and Verification
1. Connect Android device via USB
2. Verify connection using ADB:
```powershell
   adb devices
```
<img width="1107" height="498" alt="Screenshot 2025-10-27 215651" src="https://github.com/user-attachments/assets/36a80c42-abd3-4114-962d-e6cd8b088757" />

<!-- [Insert Screenshot: ADB devices list output] -->

3. Check device details:
```powershell
   adb shell getprop ro.product.model
   adb shell getprop ro.build.version.release
```
<img width="1113" height="460" alt="Screenshot 2025-10-27 215750" src="https://github.com/user-attachments/assets/d0ab7cc8-396a-48c5-b1be-e9ad44bbaba4" />

<!-- [Insert Screenshot: Device properties output] -->

### 2. Creating Full ADB Logical Backup
1. Create full backup including shared storage:
```powershell
   adb backup -f device_backup.ab -all -system -shared -apk
```
<img width="1110" height="435" alt="Screenshot 2025-10-27 215924" src="https://github.com/user-attachments/assets/c24bcfa2-a5de-4a37-aafd-b6254e978a59" />

<!-- [Insert Screenshot: Backup creation dialog on device] -->

2. Monitor backup progress:
```powershell
   dir device_backup.ab
```
<img width="1110" height="435" alt="Screenshot 2025-10-27 215924" src="https://github.com/user-attachments/assets/bcc314f6-8fbc-4bc4-8e6b-c84397b5c08b" />

<!-- [Insert Screenshot: File size and creation time] -->

### 3. Backup Integrity Verification
1. Generate SHA256 hash of backup file:
```powershell
   certutil -hashfile device_backup.ab SHA256
```
<img width="1094" height="482" alt="Screenshot 2025-10-27 220118" src="https://github.com/user-attachments/assets/7d5f7e3c-2c5b-45b5-a3be-f5bc5effbf7b" />

<!-- [Insert Screenshot: Hash output] -->


<img width="1363" height="648" alt="Screenshot 2025-10-27 220533" src="https://github.com/user-attachments/assets/e3d5df9e-f276-4b16-b774-603740a2aa71" />


### 4. Converting Backup to TAR Format
1. Download Android Backup Extractor (abe.jar)
2. Convert .ab file to .tar:
```powershell
```


### 6. Extracting Backup Contents
1. Extract TAR archive:
```powershell
   tar -xvf sd_backup.tar -C D:\extracted_backup\
```

2. List extracted contents:
```powershell
   dir extracted_backup /s
```


### 7. Data Analysis

1. Common locations to examine:
   - apps/com.android.providers.contacts/d_*/databases/contacts2.db
   - apps/com.android.providers.telephony/d_*/databases/mmssms.db
   - apps/com.android.providers.media/d_*/databases/external.db

2. Analyze database contents using SQLite Browser

---
## Results
Document the following findings:
1. Backup File Details:
   - Size: [Size in MB]
   - Creation Time: [Timestamp]
   - SHA256 Hash: [Hash value]

2. Extracted Content Statistics:
   - Number of applications: [Count]
   - Total files extracted: [Count]
   - Key databases found: [List]

---

## Conclusion
The experiment successfully demonstrated the process of performing logical acquisition from an Android device using ADB backup. This method proves effective for basic forensic acquisition while maintaining evidence integrity through proper documentation and hash verification.

---
