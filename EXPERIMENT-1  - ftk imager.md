                                                             Experiment.1

                                                 FTK Imager: A Forensic Imaging Tool Overview

                                                Acquiring Volatile Memory (RAM) Using FTK Imager

**Link for installation file :-**
https://www.exterro.com/digital-forensics-software/ftk-imager

Steps to Capture RAM Using FTK Imager

1\. Run as Administrator

-   Open FTK Imager with administrative privileges.

-   Right-click the FTK Imager icon and select Run as administrator
-   ![Image](https://github.com/user-attachments/assets/945303aa-d35d-4243-8a0a-5f5dc32d1866)

**2. Initiate Memory Capture**

-   In the top menu bar, click File → Capture Memory from the dropdown
    list.
    <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/c0074f95-3348-4176-9d76-0058b817082d" />

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

    <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/12bc34a2-167d-45fe-8093-4787ea253f6b" />

**4. Start Capture**

-   Click the **Capture Memory** button to begin acquisition.

-  <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/96e3a3cc-fa6e-47b7-88d3-1f088a70e250" />

**5. Wait for Completion**

-   A progress bar will indicate the capture status.

-   Capture time depends on the system's RAM size.

-   Once finished, the memory dump file will be available in the
    destination folder.

                             //Acquiring Non-Volatile Memory (Disk Image) Using FTK Imager//

1\. Start the Process

-   In FTK Imager, go to the top menu bar: File → Create Disk Image\....

-   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/c7cf1dce-c280-4a02-9013-764c72aa7e45" />

**2. Select Source Evidence Type**

A window will appear asking you to choose the source type:

-   **Physical Drive:** Images the entire disk, including all
    partitions, unallocated space, and the Master Boot Record (MBR).

-   **Logical Drive:** Images a specific partition (e.g., C: drive).

-   **Image File:** Converts or copies an existing image file.

-   **Contents of a Folder:** Creates an image of a specific folder
    only.

    <img width="1356" height="767" alt="Image" src="https://github.com/user-attachments/assets/8b853c61-74f6-4b20-954b-933f819a028d" />

**3. Select the Source Drive**

-   From the dropdown, choose the physical drive to image (connected
    via **write-blocker**).

-   Click **Finish**.

-   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/0048599b-7748-443f-b54e-c9c67a6429aa" />

**4. Configure the Image Destination**

-   Click **Add\...** in the \"Create Image\" window to define the
    image **format** and **destination**.

    <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/a22821a9-bec2-497f-af18-840e65078cb1" />

**Options:**

-   **Image Type:**

    -   **E01 (EnCase Format):** Recommended; includes compression,
        metadata, and error-checking.

    -   **Raw (DD):** Bit-for-bit copy with no extra features.
 
    -   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/01b21cca-9472-401a-a806-8387b229103c" />


-   **Fill in Evidence Item Information:**

    -   Enter case details, examiner name, and description.

    -   This information is stored in the image metadata (important for
        documentation).

        <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/af2a7c10-80c0-441b-a263-630536197210" />

-   **Choose Destination Folder:**

    -   Must be a different drive from the source.

    -   Name the image file (e.g., Case001_SuspectHDD).
 
    -   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/0fa33233-66f3-4acc-8427-fbb631b06152" />
    -   

-   **Image Fragment Size:**

    -   Set a value to split the image into multiple parts.

    -   Set to 0 for a single image file.

**5. Start the Imaging Process**

-   Click **Finish** to return to the \"Create Image\" screen.

-   **Check \"Verify images after they are created\"** to calculate hash
    values and ensure integrity.

-   Click **Start**.

-   <img width="1365" height="767" alt="Image" src="https://github.com/user-attachments/assets/729339dc-cdef-49e9-80fa-3d75a7cd632c" />

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
