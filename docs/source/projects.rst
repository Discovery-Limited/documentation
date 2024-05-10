Projects File Documentation
===========================

Overview
--------
The `projects.js` file serves as a crucial component in managing projects within a web application. It facilitates the organization of projects, enabling users to efficiently view project details, track progress, and perform essential project management actions.

Description
-----------
The Projects file is responsible for rendering project items dynamically, displaying detailed project information, and providing functionality for project management tasks such as project deletion and user departure. Through its intuitive interface and interactive features, the file enhances the user experience by offering seamless navigation and efficient project handling.

Functionality
--------------
1. **Rendering Projects**:
   - Utilizes data fetched from the server through `fetch_projects.php` to dynamically render project items.
   - Renders project items with essential details like project name, contributor count, and completion progress.

2. **Project Details**:
   - Presents detailed project information in a popup upon clicking on a project item.
   - Displays comprehensive project data including project name, admin details, task status, and contributor list.

3. **Project Management**:
   - Empowers admins to delete projects directly from the interface.
   - Enables contributors to leave projects, updating project data accordingly.

How It Works
------------
- Upon the DOMContentLoaded event, the script initializes by selecting required HTML elements and defining event listeners.
- Instances of the Projects class are created to manage project-related functionalities and interactions.
- Project data is retrieved from the server using `fetch_projects.php` to populate project items dynamically.
- Detailed project information is displayed in a popup when users interact with project items.
- Admins and contributors can perform project management actions such as deletion and departure, with the interface updating in real-time to reflect these changes.

Functions
---------
1. **Projects Class**:
   - **Constructor**: Initializes Projects object with project data obtained from the server.
   - **render()**: Dynamically renders project items with essential details extracted from the fetched data.
   - **detailsEvent()**: Manages the display of detailed project information in a popup upon user interaction.

2. **omitData(data)**:
   - Sends project-related data to the parent window using postMessage.

3. **togglePopup()**:
   - Controls the visibility of popups within the application interface.

File Structure
--------------
- `projects.js`: Main JavaScript file containing project management logic.
- `fetch_projects.php`: PHP file for fetching project data from the server.
- `project_delete.php`: PHP file for deleting projects.
- `project_leave.php`: PHP file for allowing users to leave projects.

Note
----
Ensure proper server-side configuration and error handling for fetching and updating project data.
