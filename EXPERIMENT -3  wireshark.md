                                                      //EXPERIMENT -3//

                                                        //Wireshark//

                                              //Network Packet Capture and Analysis Tool//

**Installation:**

**Windows:** <https://www.wireshark.org/download.html>

**Mac :** <https://www.wireshark.org/download.html>

**Linux:** preinstalled in kali else download source code from same
website

**Procedure:**

**Step 1: Start Capturing Packets**

-   First, open Wireshark. You will see a list of all available network
    interfaces.

-   Select the interface your computer is using to connect to the
    internet

-   Click the blue shark fin icon in the top-left corner to start the
    capture. Wireshark will immediately begin capturing all traffic
    passing through that interface.

    <img width="1365" height="720" alt="Image" src="https://github.com/user-attachments/assets/3b5ddc27-767c-4393-a8ed-764116a908e3" />

> **Step 2: Generate Login Traffic**

-   Open a web browser and navigate
    to <http://testphp.vulnweb.com/login.php>.

-   Enter any dummy credentials. For this example, we\'ll use:

Username: admin

Password: admin@123

-   Click the login button. The login will fail, but the data has
    already been sent across the network.

    <img width="1365" height="723" alt="Image" src="https://github.com/user-attachments/assets/3dab7ede-ce19-4fb6-a5a6-f503fec5254e" />

**step 3: Stop Capture and Filter Traffic**

-   Return to Wireshark and click the Stop button

-   In the display filter bar, you need to find the packet containing
    the login data. Since the form data was sent to the server, we will
    look for an HTTP POST request.

-   Apply the following filter(http.request.method) to find the exact packet and press Enter:

-   <img width="1365" height="644" alt="Image" src="https://github.com/user-attachments/assets/61c305ff-59ef-4d81-a61a-79fe9f30bdc3" />

**step 4: Inspect the Packet to Find Credentials**

-   In the filtered packet list, you should see a packet with
    information like \"POST /userinfo.php\". Select this packet.

-   In the Packet Details pane below the list, expand the following
    sections:

    <img width="1365" height="725" alt="Image" src="https://github.com/user-attachments/assets/9fd478c8-7218-4a9b-a644-6ac50b4f53a2" />

Hypertext Transfer Protocol HTML Form URL EncodedInside the \"HTML Form
URL Encoded\" section, you will see the credentials you entered in
plaintext.

**Result**

The experiment successfully intercepts the login credentials in a
human-readable format. The analysis of the captured POST packet reveals
the plaintext data that was transmitted over the network:

This result confirms the inherent security flaw of the HTTP protocol.
Any sensitive data sent over HTTP is transmitted openly, making it
trivial to intercept.
