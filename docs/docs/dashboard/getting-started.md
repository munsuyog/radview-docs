# Getting Started


## Launching WebLOAD Dashboard
To launch WebLOAD Dashboard:

1. Select **Start** > **Programs** > **RadView** > **WebLOAD** > **Utilities** - > **Start WebLOAD**
    **Dashboard**.
This launches the WebLOAD Dashboard server.
2. Navigate to **[http://localhost:3000/](http://localhost:3000/)**
    The WebLOAD Dashboard login window appears. The default user is ‘ **admin’**
    with password ‘ **admin’**.

Note that the default user is a Super Admin, as explained in Super Administrators
(on page 81 ).

<!-- Figure 3 : WebLOAD Dashboard Login page -->

After login, the homepage appears, showing the latest sessions and tests with links to 
those sessions and tests, as well as links to creating new load tests in WebLOAD 
Dashboard. 

<!-- Figure 4: WebLOAD Dashboard Homepage -->

## Using the menu bar

The menu bar provides access to the various WebLOAD Dashboard functions. Note
that the Admin menu is available only for Super Administrators.

<!-- Figure 5 : WebLOAD Dashboard menu bar -->
| Item           | Description            | For more information, see  |
|----------------|------------------------|-----------------------------|
| Tests          |                        |                             |
| Search         | View the list of Load Tests and their definitions, and perform operations on a selected Load Test: <br> • Run test <br> • Pause test <br> • Edit test <br> • View this test's sessions <br> • Show this test's last session <br> • Delete test | Viewing Tests (on page 12) |
| New            | Create a new Load Test | Creating a new load test (on page 13) |
| Sessions       |                        |                             |
| Search         | Select a session for viewing and analysis | Viewing Load Sessions (on page 28) |
| Upload         | Import a session into the database | Uploading a session (on page 30) |
| Dashboards     |                        |                             |
| Home           | The Home dashboard, as configured in the user's Profile | Setting the Default (Home) Dashboard (on page 64) |
| Playlists      | Create and play a dashboard that rotates through a list of dashboards | Creating and Playing a Playlist (on page 72) |
| + New          | Create a new dashboard | Creating a New Dashboard (on page 62) |
| + Import       | Import a dashboard that was saved in JSON file format | Importing a Dashboard (on page 60) |
| Resources      |                        |                             |
| Search         | View the list of resources | Viewing Resources (on page 31) |
| Upload         | Upload resources into the database | Uploading Resources (on page 33) |
| Admin (Super Admin only) |            |                             |
| Global Users   | Manage users | User Management by a Super Admin (on page 82) |
| Global Orgs    | Manage organizations | Adding an Organization (on page 88) |
| Load Generators | Define the available load generators | Managing Load Generators (on page 76) |
| Data Sources | A data source is a statistics data source. <br> There are two types: <br> • WebLOAD Data source - get information from a WebLOAD session. By default, this is the local installation, but it can be changed to point to a different one. Note - only one WebLOAD data source can be used at a time per organization (the default one) - to use more than one, create another organization and switch to it. <br> • Other -WebLOAD Dashboard can access other time-based data sources and show them alongside the WebLOAD data. | Changing the Back-End Server's Listening Port (on page 95) |
| Plugins        | List the installed plugins |                             |
| Server Settings | Show the current configuration |                             |
| Server Stats   | Show the usage stats |                             |
| Logged in user |                        |                             |
| You            |                        |                             |
| Profile        | Change your user name, password, and UI preferences |                             |
| See EULA       | View the End User License Agreement |                             |
| Sign out       | Sign out               |                             |
| Logged in user's Org |                  |                             |
| Preferences    | Change preferences at the Organizational level | Managing Organizations (on page 88) |
| Users          | Manage the organization's users, including their roles (permissions) | Managing Users (on page 82) |
| API Keys       | Manage API access     |                             |
| Switch to      | Switch between organizations in which you are a member. Note that when you switch to an organization, your permissions are the ones dictated by your role in that particular organization. | User Editing by a Super Admin -- Editing User's Permissions, Organizations, Roles and Details |
| + New Organization | Add an organization | Adding an Organization (on page 88) |
