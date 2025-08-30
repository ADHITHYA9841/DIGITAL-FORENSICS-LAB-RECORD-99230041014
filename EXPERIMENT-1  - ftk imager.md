                                                             Experiment.1

                                                 FTK Imager: A Forensic Imaging Tool Overview

                                                Acquiring Volatile Memory (RAM) Using FTK Imager

**Link for installation file :-**
https://www.exterro.com/digital-forensics-software/ftk-imager

Steps to Capture RAM Using FTK Imager

1\. Run as Administrator

-   Open FTK Imager with administrative privileges.

-   Right-click the FTK Imager icon and select Run as administrator
-  ![Image](https://github.com/user-attachments/assets/d45f9bbf-2df5-4b2c-82bf-62471d4e78ce)

**2. Initiate Memory Capture**

-   In the top menu bar, click File → Capture Memory from the dropdown
    list.
    <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/f462b449-6b1e-4c47-ba2f-1f50cf7b97af" />

**3. Configure Destination**

A dialog box will appear where you configure where and how the memory
will be saved.

-   **Destination Path:**\
    Click **Browse** to select a folder on an **external drive**

-   **Destination Filename:**\
    You can keep the default memdump.mem or assign a more descriptive
    name.

-   **Optional:**
-   **Include pagefile.sys**\
    Check this box to capture pagefile.sys, which is virtual memory
    stored on the disk.

-   **create AD1 file**\
    Saves the memory dump in an AccessData-specific container file.

    <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/484dee02-b3aa-43a9-b76a-41b890729922" />

**4. Start Capture**

-   Click the **Capture Memory** button to begin acquisition.

- <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/30e357c4-0fac-47ce-8896-98105eecb8c1" />


**5. Wait for Completion**

-   A progress bar will indicate the capture status.

-   Capture time depends on the system's RAM size.

-   Once finished, the memory dump file will be available in the
    destination folder.

                             //Acquiring Non-Volatile Memory (Disk Image) Using FTK Imager//

1\. Start the Process

-   In FTK Imager, go to the top menu bar: File → Create Disk Image\....

-  <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/e2a72525-43e7-45e4-ae78-63b067413617" />

**2. Select Source Evidence Type**

A window will appear asking you to choose the source type:

-   **Physical Drive:** Images the entire disk, including all
    partitions, unallocated space, and the Master Boot Record (MBR).

-   **Logical Drive:** Images a specific partition (e.g., C: drive).

-   **Image File:** Converts or copies an existing image file.

-   **Contents of a Folder:** Creates an image of a specific folder
    only.

   <img width="1356" height="767" alt="Image" src="https://github.com/user-attachments/assets/875e6028-ea41-4402-b73c-af5cc080fda8" />

**3. Select the Source Drive**

-   From the dropdown, choose the physical drive to image (connected
    via **write-blocker**).

-   Click **Finish**.

-   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/2efe2c5d-c93d-4afa-a2a5-4937eab469ff" />

**4. Configure the Image Destination**

-   Click **Add\...** in the \"Create Image\" window to define the
    image **format** and **destination**.

  <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/25b48ff5-572a-462b-b41e-c063aa3fcca4" />

-   **Image Type:**

    -   **E01 (EnCase Format):** Recommended; includes compression,
        metadata, and error-checking.

    -   **Raw (DD):** Bit-for-bit copy with no extra features.
 
    -<img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/91175f3c-0868-488b-bf0a-14b339cb5457" />


-   **Fill in Evidence Item Information:**

    -   Enter case details, examiner name, and description.

    -   This information is stored in the image metadata (important for
        documentation).

       <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/b676246a-71b8-489f-abff-12a36cdfbcfa" />

-   **Choose Destination Folder:**

    -   Must be a different drive from the source.

    -   Name the image file (e.g., Case001_SuspectHDD).

-   **Image Fragment Size:**

    -   Set a value to split the image into multiple parts.

    -   Set to 0 for a single image file.
 
    -   

**5. Start the Imaging Process**

-   Click **Finish** to return to the \"Create Image\" screen.

-   **Check \"Verify images after they are created\"** to calculate hash
    values and ensure integrity.

-   Click **Start**.

-  <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/a23f3fd9-fd2f-48ea-ad09-5ea6ce7684ff" />

**6. Completion and Hash Verification**

-   The imaging process may take time depending on the drive size.

-   After completion, FTK Imager verifies the hashes automatically.

-   A final window shows **MD5** and **SHA1** hashes for both the source
    drive and image.

-   Matching hashes confirm the forensic image's integrity.

**References**

-   [FTK Imager Official
    Website](https://accessdata.com/product-download/ftk-imager-version-4-5)

-   FTK Imager Documentation

