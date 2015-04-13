# Sign in 

The first page that the user sees will be the sign in form. It'll also have some promotional text/video/image on it's side.

![Sign in page](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/sign-in.png)

Clicking on the **Register** button will animate the sign in form out of view, and bring the registration form into view. No page refresh will occur.

A similar action will be carried out when the user clicks on **Forgot Password** or **I have a password token**.

# Registration

A new user can register into the application using the form below.

![Registration page](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/registration.png)

The image is self explanatory, but a few notes - 

- Placeholders are used for labels.
- Timezone is needed to determine the end of the day for the user and to show the time on the notes in their timezone.

# Forgot Password

The following screen will allow a user to retrieve a token that will allow them to reset their password.

![Retrieve forgot password link](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/forgot-password.png)

Once the user enters their email and password, the token will be sent to the user if they exist in the system.

The user can then visit this page, 

![TODO]

Here the user can enter the token and if the token is valid they'll be redirected to the following page -

![TODO]

Once here, the user can enter their new password.

> A link is considered to be expired if - 
> - It has not been used in 24 hours
> - It has already been used.
