# Managing Resources

The Resources tab enables loading any file type to the WebLOAD Dashboard's Resources folder. This functionality allows you to upload files of tests created in WebLOAD Console, such as templates, scripts, sessions, etc., and any file used to test your system. The Resources tab also offers the option of creating sub-folders. If you want the uploaded templates or scripts to continue working once they are uploaded to WebLOAD Dashboard, you will need to create the same hierarchy as the original hierarchy of the files you are uploading.

## Viewing Resources

**To view the resources uploaded to WebLOAD Dashboard:**

1. In the menu bar, select **Resources** > **Search**.

![Resources Page](/images/dashboard/managing-resources/resources-page.png)

The resources can be organized hierarchically in subfolders, or some or all of them can be located in the root of the Resources folder. To view the contents of a subfolder, click the subfolder name.

The Resources table provides the following information and available actions for each resource or resource subfolder:

| **Item** | **Description** |
|----------|-----------------|
| **Name** | The name of the resource or folder containing resources. |
| ![Delete](/images/dashboard/managing-tests/managing-tests-delete.png) | Instructs WebLOAD to delete the resource or folder. Refer to *Deleting a Resource or Resources folder* (on page 34). |
| ![Download](/images/dashboard/managing-resources/download-icon.png) | Instructs WebLOAD to download the resource to the local computer. |
| ![Create Load Test](/images/dashboard/managing-resources/create-load-test.png) | Enables creating a load test based on the resource. Refer to *Creating a Load Test Based on a Resource* (on page 34). |

## Uploading Resources

**To upload a resource into WebLOAD Dashboard:**

1. In the menu bar, select **Resources** > **Search**.

2. If you wish to add a resource into the root folder of the WebLOAD Console Resources folder, click **Upload Resources** on the Resources page.

3. If you wish to add a resource into a subfolder of the WebLOAD Console Resources folder:
    - a. Navigate to the subfolder in the folders tree displayed on the Resources page. If the subfolder does not yet exist, create it as described in *Creating a Resources subfolder* (on page 33).
    - b. Click **Upload Resource**.

   The Upload Resources page appears.

![Upload Resources Page](/images/dashboard/managing-resources/upload-resources-page.png)

4. On the Upload Resources page, click **Select resource files**.

5. In the file explorer window that appears, navigate to the files, select them, and then click **Open**.

6. The files are uploaded to the folder you were in when you clicked **Upload Resource**.

## Creating a Resources Subfolder

**To create a subfolder in the Resources folder:**

1. In the menu bar, select **Resources** > **Search**.
   
    The Resources page appears

2. If you wish to add a subfolder under the root folder of the WebLOAD Console Resources folder, click **Create Folder** on the Resources page.

3. If you wish to add a subfolder under a specific subfolder of the WebLOAD Console Resources folder, navigate to the specific subfolder in the folders tree displayed on the Resources page. Then click **Create Folder**.

    The New Resource Folder page appears.

    ![New Resource Folder Page](/images/dashboard/managing-resources/new-resource-folder.png)

4. Specify the subfolder's name, and click **Create**.

## Creating a Load Test Based on a Resource

You can create a load test based on either of the following types of resources:

- .wlp - a script as well as resources related to the script

- .tpl - a template file

**To create a load test based on a resource:**

1. In the menu bar, select **Resources** > **Search**.

2. In the Resources table, click ![Create Load Test](/images/dashboard/managing-resources/create-load-test.png) adjacent to a resource of type .wlp or .tpl.
   
3. If the resource was a .wlp file, the Create Load Test for a Script-type test appears, with the .wlp already appearing in the **Script** field. See *Creating a Script Load Test*. Set or edit any of the fields, and click **Create Test**.

4. If the resource was a .tpl file, the Create Load Test for a template-type test appears, with the .tpl already appearing in the **Template** field. See *Creating a Template Load Test*. Set or edit any of the fields, and click **Create Test**.

## Deleting a Resource or Resources Folder

1. In the menu bar, click **Resources** > **Search**.

2. Optionally navigate to a specific subfolder in the folders tree displayed on the Resources page.

3. Click ![Delete](/images/dashboard/icons/delete.png) adjacent to a resource or subfolder.

4. You are requested to confirm the delete operation.

    ![Delete Resource Confirmation](/images/dashboard/managing-resources/delete-resource-confirmation.png)

5. If the resource is a template, you can select between:
    - Deleting the template as well as its associated test and sessions
    - Deleting only the template, but keeping the associated test and sessions

    ![Delete Template Resource](/images/dashboard/managing-resources/delete-template-resource.png)

6. If you specified to delete a resources folder, keep in mind that although the templates located in this folder will be deleted, the tests and sessions from those folders will be kept for review and will be displayed in the Load Tests page and Load Sessions page (but without the ability to run them).

    ![Delete Resource Subfolder](/images/dashboard/managing-resources/delete-resource-subfolder.png)
