Log In and Register Page
=====

An explanation of the functions used in the log in and the sign up pages. 

.. code-block:: javascript

    function validateLogin() {
        if (email.value.length == 0 && password.value.length == 0 ) {
            button.style.cursor = 'not-allowed';
            button.style.opacity = (0.4);
        } else if(email.value == '' && password.value == ''){
            button.style.cursor = 'not-allowed';
            button.style.opacity = (0.4);
        } else if (password.value.length >= 8 && email.value != '' ) {
            button.style.opacity = (1);
            button.style.cursor = 'pointer';
        } else {
            button.style.cursor = 'not-allowed';
            button.style.opacity = (0.4);
        }
    }

The validateLogin() function is called on key down for the email and password input fields.
This function prevents the user from clicking on the 'log in' button if the inputs do not meet the requirements, which is if any of the fields are left empty.

.. code-block:: javascript

    function checkUsername() {
        const rules = {
            length: username.value.length > 4,
            specialChar: /[!@#$%^&*(),.?";':{}|<>]/.test(username.value)
        };
        
        const messages = [];
        if (!rules.length) messages.push("Username must be longer than 4 characters.");
        if (rules.specialChar) messages.push("Username must not contain special character.");
        if (messages.length === 0) {
            usernameFeedback.style.display = 'none';
            usernameChecked = true;
        } else {
            usernameFeedback.style.display = 'block';
            usernameFeedback.innerHTML = messages.join('<br>');
            usernameChecked = false;
        }
        handleForm();
    }

The checkUsername() function is called on key up on the username input field.
If the username meets the requirements, which is to have more than 4 characters and not contain any special characters, then usernameChecked will be set to true.
If the username does not meet the requirements, then usernameChecked is set to false. Also, a message stating that the username entered is not valid and the reason why will be displayed below the username input field.


.. code-block:: javascript

    function checkEmail() {
        const emailVal = email.value;
        if (!emailVal.includes('@')) {
            emailFeedback.style.display = 'block';
            emailChecked = false;

        } else {
            emailFeedback.style.display = 'none';
            emailChecked = true;
        }
        handleForm();
    }
The checkEmail() function is called on key up on the email input field.
The function checks if the input contains the '@' symbol, and sets the 'emailChecked' variable to true if it does.


.. code-block:: javascript

    function checkPassword(event) {
        const placeholder = event.target.placeholder;

        if (placeholder === "Password") {
            const rules = {
                length: password.value.length > 8,
                uppercase: /[A-Z]/.test(password.value),
                lowercase: /[a-z]/.test(password.value),
                number: /\d/.test(password.value),
                specialChar: /[£~`!@#$%^&*(),.?";':{}|<>]/.test(password.value)
            };
            
            const messages = [];
            if (!rules.length) messages.push("Password must be longer than 8 characters.");
            if (!rules.uppercase) messages.push("Password must contain at least one uppercase letter.");
            if (!rules.lowercase) messages.push("Password must contain at least one lowercase letter.");
            if (!rules.number) messages.push("Password must contain at least one number.");
            if (!rules.specialChar) messages.push("Password must contain at least one special character.");
            if (messages.length === 0) {
                passwordFeedback.style.display = 'none';
                if (confirmPassword.value.length > 0) {
                    if (password.value !== confirmPassword.value) {
                        confirmFeedback.style.display = 'block'
                        passwordChecked = false;
        
                    } else {
                        confirmFeedback.style.display = 'none';
                        passwordChecked = true;
                    }
                }
            } else {
                passwordFeedback.style.display = 'block';
                passwordFeedback.innerHTML = messages.join('<br>');
                passwordChecked = false;
            }
            return;     
        }
        if (password.value !== confirmPassword.value) {
            confirmFeedback.style.display = 'block'
            passwordChecked = false;

        } else {
            confirmFeedback.style.display = 'none';
            passwordChecked = true;

        }
        handleForm();
    }

The checkPassword() function is called on key up on the password and confirm password input fields.
The password must contain an uppercase letter, a lowercase letter, a number, a special character, and be longer than 8 characters.
If the password entered does not meet any of these requirements, a message below the password input will notify the user on which requirement(s) the password does not meet.

.. code-block:: javascript

    function handleForm() {
        if (usernameChecked && emailChecked && passwordChecked) {
            submitForm.classList.add("active");
            return submitForm.disabled = false;
        }
        submitForm.classList.remove("active");
        submitForm.disabled = true;
    }

The handleForm() function is called at the end of each of the input check functions for signing up.
When all the inputs meet the requirements, the user will be able to click on the 'sign up' button to successfully create their account.