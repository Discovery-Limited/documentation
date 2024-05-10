Deadlines File Documentation
==============================

Overview
--------
The Deadlines JavaScript file manages deadlines within a web application. It handles rendering, displaying details, and providing functionality for managing deadlines.

Purpose
-------
The Deadlines file serves the following purposes:

1. **Rendering Deadlines**: Dynamically renders deadline items based on fetched data.
2. **Deadline Details**: Displays detailed information about each deadline.
3. **Deadline Management**: Provides options to leave or mark deadlines as complete.

Functionality
--------------
1. **Rendering Deadlines**:
   - Fetches deadline data from the server using `fetch_deadline.php`.
   - Renders deadline items based on fetched data.

2. **Deadline Details**:
   - Opens a popup with detailed information when a deadline is clicked.
   - Displays task name, deadline date, description, and assignees.

3. **Deadline Management**:
   - Allows users to leave or mark deadlines as complete.
   - Sends requests to the server to update deadline status.

Usage
-----
1. **Rendering Deadlines**:
   - Ensure the `fetch_deadline.php` file is correctly configured to fetch deadline data from the server.

2. **Deadline Details**:
   - Click on a deadline item to view detailed information in a popup.

3. **Deadline Management**:
   - Use the "Leave" button to remove yourself from a deadline.
   - Use the "Complete" button to mark a deadline as complete.

Functions
---------
1. **openPopup()**:
   - Opens the deadline details popup and displays detailed information about the selected deadline.

2. **Deadline Class**:
   - **Constructor**: Initializes a Deadline object with data.
   - **render()**: Renders the deadline item with task name, deadline date, and days left.
   - **detailsEvent()**: Handles the click event on the deadline details button to display detailed information.

3. **omitData(data)**:
   - Sends data to the parent window using postMessage.

4. **leaveDeadline()**:
   - Sends a request to the server to remove the user from the selected deadline.

5. **completeDeadline()**:
   - Sends a request to the server to mark the selected deadline as complete.

Note
----
Ensure proper server-side configuration and error handling for fetching and updating deadline data.

