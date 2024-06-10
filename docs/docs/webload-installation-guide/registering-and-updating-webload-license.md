# Registering and Updating the WebLOAD License

Your WebLOAD license must be registered before you can start working with WebLOAD. WebLOAD licenses that have expired must also be renewed or updated before you can continue working with WebLOAD. When installing a new major or minor version of WebLOAD, make sure that you have an adequate license for that specific version. All license registration and updating is accomplished through the Update License dialog box.

You can register and update your WebLOAD license either through an Update License application or through the Command Line Interface.

## License Administration through the UI

### Standard License Registration

**To open the Update License dialog box:**

- At the time of WebLOAD installation, when the WebLOAD Installation Wizard is finished, the License dialog box opens automatically.

> **Note:** After a WebLOAD installation, you may be prompted to restart your computer before the Update License dialog box appears. In this case, the License dialog box will appear automatically after the computer restarts.

- Or -

- At any other time, from the Windows desktop, select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** > **Update License**.

The License dialog box includes the following sections:

- License Details
- Update License

These sections are used to register and update your WebLOAD authorization license information.

### To Complete or Update Your License Registration

1. If you are registering a new license after an initial WebLOAD installation, access the Update License dialog box. The Update License dialog box is opened automatically after a successful WebLOAD installation is completed.

   - Or -

   If you are updating your license registration after your current license has expired, from the Windows desktop, select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** > **Update License**.

   The Update License dialog box appears.

   ![Update License Dialog Box](/images/webload-installation-guide/update-license-dialog-box.png)

2. Create an email message with the following information:

   a. Copy the Host ID displayed in the text box into the email.

   b. Add your name, company, address, and phone number to the email message.

3. Send the email to [license@radview.com](mailto:license@radview.com).

   A WebLOAD license file (*.lic) will be sent to you.

4. Select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** > **Update License** to open the Update License dialog box and install the license key.

5. By default, the **Use a license file** radio button is selected. This assumes that your license file is located on your local computer system.

   For information on installing a floating license or connecting to a license server, see *WebRM Server*.

   For information on installing a license for an evaluation of WebLOAD, see *Trial License*.

6. Click the browse button next to the **Use a license file** text box to browse to the location of the license (*.lic) file sent to you by a RadView representative.

7. Select the correct license file and click **Open** to return to the Update License dialog box.

8. Click **OK** to load the new license.

   If the license registration was successful, a message box appears indicating a successful license update.

   You can now begin working with WebLOAD.

   > **Note:** After loading the license, you can optionally click **License Information** to view the license's full details.

   If the license registration was not successful, an error message appears.

   If you are not able to successfully register a valid license file, contact RadView Support for assistance.

### Trial License

You can install a trial version of WebLOAD, which provides 50 virtual clients and is available for 30 days.

**To use the WebLOAD evaluation:**

1. After installing WebLOAD, the Update License dialog box opens,

   - Or -

   To open the Update License dialog box manually, select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** > **Update License**.

   The Update License dialog box appears.

   ![Update License Dialog Box](/images/webload-installation-guide/update-license-dialog-box-trial.png)

2. Select **30-day trial**.

3. Click **OK** or **Apply** to install the license for the trial.

   You can now begin working with the trial version of WebLOAD.

### WebRM Server

The WebRM Server is a stand-alone tool that manages all resource distribution to WebLOAD Console, which is the machine used to run loads in a WebRM environment.

It is the method that controls the number of users allowed to access the product concurrently.

WebRM for virtual clients is available and defined as a pool of virtual (probing) clients that can concurrently be used by members of a testing team and monitored by the WebRM Server.

During installation of the WebRM server, you are prompted for the WebRM file that defines:

- The number of concurrent applications for the WebLOAD Console.
- The number of concurrent Virtual and Probing Clients.

Installation also creates a FlexLM Service that controls the operation.

The WebRM Server displays a list of the number of resources (Virtual and Probing Clients) that the Console is using. The WebRM Server enables a testing team to share resources.

This section describes how to connect to the WebRM Server and how to view the license details.

#### Connecting to the WebRM Server

**To connect to the WebRM Server:**

1. After installing WebLOAD, the Update License dialog box opens,

   - Or -

   To open the Update License dialog box manually, select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** > **Update License**.

   The Update License dialog box appears.

   ![Update License Dialog Box -- WebRM Server Installation](/images/webload-installation-guide/update-license-dialog-box-webrm-server.png)

2. Select **Connect to the WebRM License Server**.

3. Click the **Browse** button and select the machine where WebRM is installed.

4. Click **OK**.

   A connection to the selected license server is attempted.

   - If the connection is successful, a success message appears.
   - If the connection is not successful, a failure message appears.

#### Viewing License Details

After selecting the license server, you can view the current license details in the License Details section of the Update License dialog box.

## License Administration through the Command Line Interface

You can register or upload a WebLOAD license through a command line interface. You can enter the `wlUpdateLicenseApplicationCmd` command into a batch file or into an external script to automatically launch a WebLOAD License action, without user intervention, using the parameters you specify.

For a full description of the command, refer to the *WebLOAD™ Automation Guide*.
