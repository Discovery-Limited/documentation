User View Page
==============

Introduction
------------

This page provides an overview of the user view in your project. The user view is a crucial part of our application, providing a personalized experience for each user.

Code Explanation
----------------

The JavaScript code provided is responsible for handling various user interactions on the page. Here is a detailed explanation of the main functions:

.. code-block:: javascript

    // Fetches the list of projects from the server and populates the sidebar with them.
    // It also sets up click event listeners for each project, which set the project ID in the session, update the project button, and load the project content.
    fetch("fetch_projects.php")
    ...

    // Sets the given project ID in the user's session on the server.
    // It sends a POST request to the server with the project ID in the body.
    function setProjectIdInSession(projectId) {
    ...
    }

    // Toggles the visibility of the profile dropdown list when the profile dropdown button is clicked.
    // It adds or removes the "active" class from the profile dropdown list.
    profileDropdownButton.addEventListener("click", function () {
    ...
    }

    // Toggles the visibility of the sidebar dropdown list when the sidebar toggle button is clicked.
    // It also toggles the icon of the sidebar toggle button.
    sidebarToggle.addEventListener("click", function () {
    ...
    }

    // Loads the content from the given file into the content frame.
    // It also adds a unique parameter to the URL to prevent caching.
    window.loadContent = function (fileName) {
    ...
    }

    // Toggles the visibility of the project form when the create project button is clicked.
    // It adds or removes the "active" class from the project form.
    createProject.addEventListener("click", function () {
    ...
    }

    // Adds the given email to the email list.
    // It creates a new span element with the email as its text content and appends it to the email list div.
    function addEmailToList(email) {
    ...
    }

    // Validates the given email.
    // It uses a regular expression to check if the email is in the correct format.
    function validateEmail(email) {
    ...
    }

    // Loads the welcome page into the content frame when the window loads.
    // It sets the src attribute of the content frame to "projects.html".
    window.onload = loadWelcomePage;
    ...

    // Adds an event listener to each sidebar toggle button that makes it active when clicked and makes all others inactive.
    // It removes the "active" class from all sidebar toggle buttons and adds it to the clicked one.
    const sidebarToggles = document.querySelectorAll(".sidebar-toggle");
    ...

    // Listens for messages from the specified origin and handles them.
    // If the message contains a project ID, it removes the corresponding project from the sidebar and checks the projects.
    window.addEventListener("message", (event) => {
    ...
    }

    // Checks the list of projects and updates the project button accordingly.
    // If there is at least one project, it sets the text content and data-id attribute of the project button to the first project's name and ID, respectively, and sets the project ID in the session.
    // If there are no projects, it sets the text content of the project button to "Projects" and removes its data-id attribute.
    function checkProjects() {
    ...
    }

Conclusion
----------

In this section, we have explained the JavaScript code that handles various user interactions on the user view page. This code is crucial for providing a personalized and interactive experience for each user.