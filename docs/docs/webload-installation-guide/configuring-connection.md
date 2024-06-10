# Configuring Connection to the Oracle Database using WebLOAD

Connecting to the Oracle Database using WebLOAD requires that you install the Oracle Data Access Components (ODAC) on your computer. For information on ODAC, refer to the appropriate Oracle documentation.

**Note:** You need to be assigned a valid username and user privileges for Oracle so that you can connect to the Oracle database.

The following procedure is confirmed to work with Oracle Database version 11g, and is also expected to work with Oracle Database version 10g.

## To Configure Your Computer to Enable Connection to the Oracle Database Using WebLOAD:

1. Navigate to `$ORACLE_HOME\NETWORK\ADMIN`.

2. Open `tnsnames.ora` for editing.

    **Note:** If `tnsnames.ora` does not exist, create it. The default content is as follows:

    ```
    <tns_name> =
        (DESCRIPTION =
        (ADDRESS = (PROTOCOL = TCP)(HOST = <host or ip>)(PORT = 1521))
        (CONNECT_DATA =
            (SERVER = DEDICATED)
            (SERVER_NAME = <instance_name>)
        )
        )
    ```

3. Make the following definitions in the file:

    ```
    tns_name = <tns name configured in the listener on the server (default orcl)>
    host = <hostname or IP address of the server>
    instance name = <instance configured on the server (default orcl)>
    ```

4. Log out and log in, or restart, to activate the environmental variables.
