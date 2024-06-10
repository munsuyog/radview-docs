# Installing WebLOAD for Linux

This chapter contains the instructions for installing the WebLOAD Load Engine on a machine running a Linux operating system.

## Installing the WebLOAD Load Engine for Linux

**To install the WebLOAD Load Engine on your system:**

1. Select or create a directory for installing the WebLOAD Load Engine. This directory will be referred to as the working directory.
2. Download the `WebLOAD-linux.version.tar.gz` compressed file from a server to the working directory.
3. Uncompress and extract the tar file in the working directory using the following command:
   ```sh
   tar --zvxf WebLOAD-linux-version.tar.gz
   ```
4. Change directories by typing the following:
   ```sh
   cd radview/webload<version number>/linux/bin
   ```
5. Run setup by typing the following:
   ```sh
   ./setup
   ```
   During the setup process, the `webload.ini` configuration file is created.
6. When prompted, enter the path to the Java runtime libraries. The default path to the libraries is displayed. If you are working with a different version of Java, enter the path of the libraries using the following:
   ```sh
   /usr/java/jre/lib/i386/server:/usr/java/jre/lib/i386/native-threads
   ```
   The path information is stored in the `LD_LIBRARY_PATH` variable.

**Important:** The WebLOAD Load Generator will not function properly without the correct paths for the Java libraries.

## Running the Load Engine on Linux

When running the Load Engine on Linux, Load Engine runs with TestTalk.

TestTalk enables communication between the different components of the WebLOAD module. When running the Load Generator through Linux you generally need to connect with other WebLOAD modules running on a remote Windows machine (for example WebLOAD Console). To connect with these remote modules, you must run TestTalk. Once TestTalk is running, you can access the remote WebLOAD modules. The remote module then initiates the communication with TestTalk and then TestTalk loads the Load Generator.

**Note:** If the Load Generator is running and TestTalk is not running, the remote WebLOAD application will not be able to access the Load Generator.

**To run TestTalk on your system:**

1. Open the `linux/bin` directory within your working directory by typing the following:
   ```sh
   cd <working-directory>/linux/bin
   ```
2. Run TestTalk by typing the following:
   ```sh
   ./starttestalk
   ```
   TestTalk starts running.

**To stop running TestTalk:**

From the `linux/bin` directory, run:
```sh
./stoptesttalk
```

## Installing Third Party Software for Server-side Monitoring

WebLOAD Console provides a Performance Measurements Manager (PMM) for monitoring the performance of various data sources such as server-side applications, databases, stream technology, system, and Web server measurements in real-time while your test is running.

Some data sources require initial configuration to enable monitoring by the PMM. For more information, see the *Enabling Data Sources Monitoring* section in the *WebLOAD Console User's Guide*.