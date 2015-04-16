# The users API

### [ POST ] `/user/validate`

Validate a user's credentials. Returns the user information and the list of notebook, as well as a token that is valid for a certain period of time. Every subsequent request must be accompanied by this token ID.

### [ POST ] `/user/`

Used for registering a user.

### [ GET ] `/user/:id/notebooks`

Get user's notebooks.

### [ GET ] `/user/:id`

Fetches the user's information such as the email address, username, id, timezone.

### [ PUT ] `/user/:id`

Used to update the user information such as the email, timezone etc.
