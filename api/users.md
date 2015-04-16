# The users API

### [ POST ] `/user/validate`

Validate a user's credentials. Returns the user information and the list of notebook, as well as a token that is valid for a certain period of time. Every subsequent request must be accompanied by this token ID.

### [ POST ] `/user/`

Used for registering a user.

### [ POST ] `/user/token/validate`

Takes a token, email, and checks if the token is valid. 

### [ POST ] `/user/password`

Accepts the email, and if present sends an email to the user with that email. This email contains a token which can be used to change the password.

### [ PUT ] `/user/password`

Takes the user's email or ID, and updates their password.

### [ GET ] `/user/:id/notebooks`

Get user's notebooks.

### [ GET ] `/user/:id`

Fetches the user's information such as the email address, username, id, timezone.

### [ PUT ] `/user/:id`

Used to update the user information such as the email, timezone etc.
