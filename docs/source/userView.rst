UserView File Documentation
============================

Introduction
------------
The UserView JavaScript file facilitates user interactions and interface functionalities within web applications. It primarily focuses on managing user profiles, project creation, project selection, and email input validation. This documentation outlines the purpose, functionality, and usage of the UserView file.

Purpose
~~~~~~~
The UserView JavaScript file serves the following purposes:

1. **Profile Dropdown**: Enables the display of a dropdown menu for user profile options such as settings and logout.
2. **Sidebar Toggle**: Facilitates the toggling of the sidebar menu for navigating between different sections of the application.
3. **Project Management**: Allows users to create, select, and manage projects within the application.
4. **Email Input Validation**: Validates email inputs entered by users for project invitations or notifications.

Functionality
~~~~~~~~~~~~~
1. **Profile Dropdown**:
   - Toggles the visibility of the profile dropdown menu when the profile dropdown button is clicked.

2. **Sidebar Toggle**:
   - Toggles the visibility of the sidebar menu when the sidebar toggle button is clicked, allowing users to navigate between different sections of the application.

3. **Project Management**:
   - Fetches existing projects from the server and dynamically populates the sidebar menu with project options.
   - Allows users to select a project from the sidebar menu, updating the active project displayed in the interface.
   - Enables project creation by displaying a form for users to input project details and submit project creation requests to the server.
   - Handles project selection events, updating the active project displayed in the interface and storing the selected project ID in the session.

4. **Email Input Validation**:
   - Validates email inputs entered by users in the email input field.
   - Ensures that valid email addresses are added to the list of project collaborators or recipients.

Usage
~~~~~
Integrating the UserView JavaScript file into a web application enables users to:
- Interact with user profile options through the profile dropdown menu.
- Navigate between different sections of the application using the sidebar toggle button.
- Manage projects by creating, selecting, and viewing project details within the application.
- Input valid email addresses for project invitations or notifications.

Conclusion
~~~~~~~~~~
The UserView file enhances user experience and functionality within web applications by providing intuitive user interface elements and streamlined project management features.
