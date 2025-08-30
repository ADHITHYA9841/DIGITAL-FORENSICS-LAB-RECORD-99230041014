                                                               //EXPERIMENT - 4//

                                                                    //MHA//

                                                             //Mail Header Analyzer//

**Link:-** <https://mxtoolbox.com/EmailHeaders.aspx>

**Procedure**

**Step 1: Get the Email Header**

-   First, you need to copy the full, raw header from the email.

-   Gmail: Open the email, click the three dots (⋮), and select Show
    original.

-   Select all the text in the header and copy it.

-   <img width="1365" height="724" alt="Image" src="https://github.com/user-attachments/assets/28226ccd-af66-4b40-8a6d-b3d7db0fbadc" />
    <img width="1365" height="717" alt="Image" src="https://github.com/user-attachments/assets/267536af-1fcb-47ad-a889-f6caae085ee6" />
    <img width="1365" height="630" alt="Image" src="https://github.com/user-attachments/assets/636fdc0d-e402-4ebb-8144-1b64918556e0" />
-   
  

**Step 2: Use a Mail Header Analyzer**

-   The easiest way to analyze the header is with an online tool.

-   Navigate to a site which analyze Email Header

-   Paste the entire header you copied into the analysis box.

-   Click the \"Analyze\" button to get a parsed, easy-to-read report.

-  <img width="1358" height="632" alt="Image" src="https://github.com/user-attachments/assets/ebb0ab60-2b91-47d3-8b16-bfe76297e337" />

> **Step 3: Analyze The Report**

-   This is the most critical step. In the analyzer\'s report, look for
    the SPF, DKIM, and DMARC results.

    <img width="1361" height="639" alt="Image" src="https://github.com/user-attachments/assets/e5c4d644-6722-4dd9-89cb-76f0d3ebc220" />

    

**Review the Overall Delivery Summary**

-   First, look at the high-level summary to get an immediate sense of
    the email\'s status.

-   Check DMARC Compliance: The report shows the email is DMARC
    Compliant. This is the most important overall result.

-   Check SPF Status: Both SPF Authenticated and SPF Alignment passed.
    This means the sending server was authorized.

-   Check DKIM Status: DKIM Alignment passed, but DKIM Authenticated
    failed . This is a critical finding and indicates a problem with
    the email\'s digital signature.

    <img width="1361" height="639" alt="Image" src="https://github.com/user-attachments/assets/e5c4d644-6722-4dd9-89cb-76f0d3ebc220" />

  

**Investigate the SPF Record and Email Path**

-   Next, verify why the SPF check passed.

-   Examine the SPF Record: The SPF record for the domain is v=spf1
    include:mailgun.org \~all. This record explicitly authorizes servers
    from Mailgun to send emails on its behalf.

-   Trace the Relay Information: The delivery path shows the email was
    sent from m241-136.mailgun.net.

-   Conclusion: Since the email came from a Mailgun server, which is
    authorized in the SPF record, the SPF check passed.

    <img width="1346" height="641" alt="Image" src="https://github.com/user-attachments/assets/fb68ee3f-1a54-4026-a9d2-2bd076e54de8" />

    

    

**Analyze the DKIM Failure**



<img width="1365" height="632" alt="Image" src="https://github.com/user-attachments/assets/3b5c0f30-f6fa-4e43-b1b5-b48d2631bac6" />


**References**
