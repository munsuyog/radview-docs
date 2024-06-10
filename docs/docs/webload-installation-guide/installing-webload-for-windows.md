# Installing WebLOAD for Windows

This chapter provides step-by-step instructions for installing WebLOAD on a PC running Windows systems.

## Installing WebLOAD for Windows

You can choose either of the following installation methods:
- **Command Line Installation**
- **Using the Installation Wizard**

### Command Line Installation

To perform a command line installation, run the following command:
```
<WebLOAD executable installation file> [flags]
```

Where the flags (case sensitive) are:

- `/SILENT` Silent mode
- `/DIR="<destination directory>"` Destination directory
- `/TYPE=Agent` Install a Load Generator only
- `/TYPE=Dashboard` Install the Web Dashboard only
- `/SERVICE` Install TestTalk as a service
- `/DOMAIN="<domain name>"` The domain in which to install for service installation
- `/USERNAME="<user name>"` The user name for service installation
- `/PASS="<user password>"` The password of the service installation
- `/MANUAL` How to start the service. If not set, the service will start automatically
- `/NOCHECK` Do not check for a previous installation

For example:
```
WebLOAD Professional-10.1.0.013.en.exe /SILENT /DIR="c:\radviewtemp" /TYPE=Agent /SERVICE /MANUAL /DOMAIN="dom" /USERNAME="us" /PASS="pas" /NOCHECK
```

### Using the Installation Wizard

When you install WebLOAD on your computer, the installation program asks you for the components to install. As part of the installation process, WebLOAD installs a database management system (PostgreSQL 8.3) for use with WebLOAD Analytics.

Install the WebLOAD components as follows:

- Install the full WebLOAD product on computers that will be used to run the WebLOAD Console.
- Install only the Load Generator or the Probing Client software on a computer that will be a dedicated Load Machine. There is no need to install the full product on computers that will be used as Load Machines.

**To install WebLOAD on your system:**

1. Browse to the location of the WebLOAD executable (*.exe) installation file.
2. Double-click the file. The WebLOAD Installation Wizard appears.
3. Follow the instructions in the Installation Wizard.
4. In the Select Components screen:
    - Select the type of installation. For Load Machines and Probing Clients, select **Load Generator only**.
    - Specify whether to install the **Load Generator As Service**.
        - If you select this option, TestTalk is installed as a service. Since a service can be started automatically, this is especially useful for machines that serve only as Load Generators.
        - If you do not select this option, TestTalk is installed as an executable file.
    - Specify whether to also install the WebLOAD Cloud. The WebLOAD Cloud enables viewing, analyzing, and comparing load sessions in a web browser, with full control and customization of the display.

> **Note:** The installation process is the same for Load Machines and Probing Clients.

When the WebLOAD installation is complete, the WebLOAD License dialog box automatically opens to complete the registration process. License registration is discussed in *Registering and Updating the WebLOAD License*.

## Installing WebRM

**To install WebRM:**

1. Browse to the location of the WebRM-10.0.xxx.en.exe installation file.
2. Double-click the file. The WebRM Installation Wizard appears.
3. The WebRM Installation Wizard displays the Select Destination Location dialog box. On the Select Destination Location dialog box, browse to the location where you would like WebRM installed. By default, this location is `C:\Program Files\RadView\WebRM`.
4. Click **Next**.
5. The WebRM Installation Wizard displays the Select License Location dialog box. This dialog box displays your HostID and enables you to browse to the License location.

> **Note:** If you have already received your WebRM License file, skip to step 9.

6. If you have not received your License file, copy the HostID displayed in the text box into an email, together with your name, company, address, and phone number. Send the email to

   A WebRM license file (*.lic) will be sent to you.

7. After receiving the file, save it on the hard drive of your WebRM machine.
8. Double-click the WebRM executable installation file to restart the installation process.
9. On the Select License dialog box, browse to the location where you saved your WebRM license, select the file and click **Next**.

![WebRM Installation Wizard -- Select Start Menu Folder](/images/webload-installation-guide/webrm-installation-wizard.png)

10. WebRM begins the installation. When the WebRM installation process is complete, a dialog box appears stating that the WebRM installation has completed successfully. Click **Finish**.

## Upgrading WebLOAD

**To upgrade WebLOAD:**

1. Close TestTalk.
2. Close all browser windows that are open.
3. Uninstall the existing WebLOAD version.

   For instructions on the uninstall procedure, see *Uninstalling WebLOAD*.

4. Install the new version of WebLOAD.

   For installation instructions, see *Installing WebLOAD for Windows*.

## Installing and Configuring the WebLOAD Analytics Database

WebLOAD stores information from Load Sessions in a PostgreSQL database for use with WebLOAD Analytics. You can install PostgreSQL and the WebLOAD Analytics database during the WebLOAD installation or manually after WebLOAD has already been installed. You might want to perform manual installation in the following situations:

- If PostgreSQL is already installed on your machine and you only need to create the WebLOAD Analytics database. For instructions, refer to *Creating the Database when PostgreSQL is Already Installed*.
- If you want to use a different machine as the database server and have several WebLOAD Analytics applications connect to the database. For instructions, refer to *Installing and Configuring the Database on a Dedicated Machine*.

### Creating the Database when PostgreSQL is Already Installed

If PostgreSQL is already installed on your machine, you do not have to reinstall it during the WebLOAD installation. However, you must complete the following steps in order to create the WebLOAD Analytics database in PostgreSQL so that it can be used by WebLOAD Analytics.

**To create the WebLOAD Analytics database after WebLOAD was installed:**

- Run `deploy-database.bat` from the `C:\Program Files\RadView\WebLOAD\bin\database` folder.

### Installing and Configuring the Database on a Dedicated Machine

You can run the PostgreSQL database using a dedicated machine with several WebLOAD Analytics client applications.

**To install and configure the database on a dedicated machine:**

1. Install PostgreSQL.

   > **Note:** It is recommended to install PostgreSQL Version 8.3. You can download the application from and install it using its default installation settings.

2. Copy all the files from the `C:\Program Files\RadView\WebLOAD\bin\database` directory to a temporary folder on the dedicated server.
3. Run `deploy-database.bat` from the temporary folder to which you copied the files in the previous step. The WebLOAD Analytics database is created.
4. Configure PostgreSQL to allow remote connections. For more information, see *Configuring PostgreSQL to Allow Remote Database Connections*.
5. Configure the relevant WebLOAD Analytics clients to work with the remote database. For more information, see *Configuring Clients to Work with the Remote Database*.

### Configuring PostgreSQL to Allow Remote Database Connections

For WebLOAD Analytics clients to work with the remote database, you must perform the following configuration steps on the host machine.

**To configure a remote database connection through PostgreSQL:**

1. Run **Start** → **PostgreSQL 8.3** → **PgAdmin III**. The PgAdmin III application opens.
2. Edit the `postgresql.conf` file, as follows:
    - Select **File** → **Open**.
    - Browse to `C:\program files\Postgres\Data\`, select `postgresql.conf`, and click **Open**. The `postgresql.conf` configuration file opens.
    - Change the value of `listen_address` to `*`. This configures the server to listen to all addresses.
    - Enable the value and save the file.
3. Edit the `pg_hba.conf` file, as follows:
    - Select **File** → **Open**.
    - Browse to `C:\program files\Postgres\Data\`, select `pg_hba.conf`, and click **Open**. The `pg_hba.conf` configuration file opens.
    - Add a new entry with the following parameters:
        - **Type** = host
        - **Database** = all
        - **User** = all
        - **IP address** = `<IP subnet mask>.0.1.1/24`, where `<IP subnet mask>` is your organization's IP subnet mask.
        - **Method** = md5
    - Enable the entry and save the file.

### Configuring Clients to Work with the Remote Database

**To configure a remote database connection through PostgreSQL:**

1. Open WebLOAD Analytics on the client machine.
2. Select **Window** → **Preferences** → **Database**.
3. Enter the server's IP address and name in the Database host name field.
4. Click **OK**.

## Installing Third Party Software for Server-side Monitoring

WebLOAD Console provides a Performance Measurements Manager (PMM) for monitoring the performance of various data sources such as server-side applications, databases, stream technology, system, and Web server measurements in real-time while your test is running.

Some data sources require initial configuration to enable monitoring by the PMM. For more information, see

 the *Enabling Data Sources Monitoring* section in the *WebLOAD Console User's Guide*.