# Appendix A: Recording Binary AMF

WebLOAD supports recording AMF transactions with binary encoded data and simultaneously recording AMF and other binary content.

## Recording Binary-format AMF Representations

After installing the Adobe Flex Add-on, all AMF content is displayed in an easy-to-read JavaScript representation in the JavaScript Editor. Alternatively, the binary format of the AMF traffic can be displayed. In this case, the AMF content is extracted from the HTTP traffic and the native binary data is encoded in your script.

![AMF Transactions with Binary Encoded Data](/images/adobe-flex/appendix-a/amf-transactions.png)

*Figure 12: AMF Transactions with Binary Encoded Data*

**To enable recording AMF transactions with binary encoded data:**

1. In the WebLOAD Recorder, select **Tools** ➡️ **Recording and Script Generation Options**.
    - The Recording and Script Generation Options dialog box appears.
2. Select the **Content Types** tab and verify that the `application/x-amf` content type appears in the Recorded Types field.
3. Select the **Post Data** tab and verify that the `application/x-amf` content type appears in the DATA Block field.
4. Select the **Script Generation** tab and verify that **Encode Binary Data** is selected.
5. Click **OK**.
    - The recording options are configured.

**Note:** For additional information about configuring the recording options, refer to *Configuring the WebLOAD Recorder Options* in the *WebLOAD Recorder Users Guide*.

## Recording AMF with Additional Binary Content

WebLOAD enables you to simultaneously record AMF with additional binary content by defining the relevant content types in the WebLOAD Recorder. This is particularly useful when recording a Web page that contains both AMF and RTMPT content. For additional information about configuring the recording options, refer to *Configuring the WebLOAD Recorder Options* in the *WebLOAD Recorder Users Guide*.