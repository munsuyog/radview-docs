# Managing Dashboards

In WebLOAD Dashboard, you can manage any dashboard saved in the database, as well as create new dashboards, delete dashboards, import and export dashboards in JSON format, and save your customized dashboards.

## Loading a Dashboard

When you access WebLOAD Dashboard, the default Home dashboard is displayed. You can, however, select to display any other dashboard from the database, as described in this section.

Note that you can also import a dashboard that was saved as a JSON file, as described in *Importing a Dashboard* (on page 60).

### To load a dashboard:

1. In the menu bar, select **Dashboards** > **Main Dashboard**.
2. Click the dashboard drop-down in the dashboard header.

A list of all the dashboards in the database is displayed.

![Figure 67: Dashboards List](/images/dashboard/managing-dashboards/dashboards-list.png)

3. Optionally enter a text string in the Search box to filter the display by dashboards whose name contains that text string.
4. Optionally, click **starred** in the right side of the Search box to filter the display by your favorite dashboards (dashboards you had starred).
5. Select a dashboard from the list. WebLOAD Dashboard displays the selected dashboard.

## Exporting & Importing a Dashboard in JSON Format

You can export a dashboard as a JSON file and import dashboards that were saved in JSON file format.

For instructions on how to import a dashboard that was saved as a JSON file, refer to *Exporting a Dashboard as a JSON File*.

### Importing a Dashboard

**To import a dashboard that was saved in JSON file format:**

1. Do either of the following:
    - In the menu bar, select **Dashboards** > **Import**.

    ![Figure 68: Dashboard Menu](/images/dashboard/managing-dashboards/dashboard-menu.png)

    - In the Dashboard header, click the dashboard drop-down and select **Import**.

    ![Figure 69: Selecting to Import a Dashboard -- from the Header](/images/dashboard/managing-dashboards/select-to-import-a-dashboard.png)

2. In the Import Dashboard window that appears, select **Upload .json File**, and specify the desired JSON file.

Alternatively, paste JSON content into the Import Dashboard window and click **Load**.

![Figure 70: Import Dashboard window](/images/dashboard/managing-dashboards/import-dashboard-window.png)

WebLOAD Dashboard displays the selected dashboard.

## Creating a New Dashboard

You can create a new empty dashboard and define it as desired.

### To create a new dashboard:

1. Do either of the following:
    - In the menu bar, select **Dashboards** > **+ New**.

    ![Figure 71: Dashboard Menu](/images/dashboard/managing-dashboards/dashboard-menu.png)

    - In the Dashboard header, click the dashboard drop-down and click **+ Create New**.

    ![Figure 72: Selecting to Create a New Dashboard -- from the Header](/images/dashboard/managing-dashboards/select-to-create-a-new-dashboard.png)

A new empty dashboard appears.

2. Configure the dashboard as desired. Refer to *Customizing a Dashboard* (on page 46) for more information.

## Saving your Customized Dashboard

After changing a dashboard as desired, you can save the customized dashboard to keep all the changes. Note that two changes are not saved: the selected sessions and the selected time filter.

### To save a customized dashboard:

1. Click the Manage Dashboard Settings icon ![Manage Dashboard Settings icon](/images/dashboard/managing-dashboards/manage-dashboard-settings-icon.png) in the middle of the dashboard header, and select **Save As**.

![Figure 73: Saving a Customized Dashboard](/images/dashboard/managing-dashboards/import-dashboard-window.png)

2. Give your dashboard a unique name by editing the current name, which appears in the **New name** field.

## Setting the Default (Home) Dashboard

You can set any desired dashboard as your Home (default) dashboard, and you can also revert to the global WebLOAD Dashboard default any time.

### To set the Home dashboard:

1. In the right side of the menu bar, click the down arrow adjacent to your user name.

![Figure 74: Options of the Logged-in User](/images/dashboard/managing-dashboards/options-of-logged-in-user.png)

2. In the dropdown list that appears:
    - To set the default dashboard at the user level, select **Profile** and then in the Profile window, set the **Home Dashboard** in **Preferences**.
    - To set the default dashboard at the organization level, select **Preferences** and then in the Org Preferences window, set the **Home Dashboard** in **Preferences**.

Note that your personal default takes precedence over the Org default, which takes precedence over the global default.

3. To revert to the global default, select **Preferences** and then in the Org Preferences window, set the **Home Dashboard** to **Default**.

## Deleting a Dashboard from the Database

### To delete a dashboard from the database:

1. Click the Manage Dashboard Settings icon ![Manage Dashboard Settings icon](/images/dashboard/managing-dashboards/manage-dashboard-settings-icon.png) in the middle of the dashboard header, and select **Delete dashboard**.

![Figure 75: Selecting to Delete a Dashboard](/images/dashboard/managing-dashboards/select-to-delete-dashboard.png)

2. Confirm the operation.
