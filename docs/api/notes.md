# The notebook API

### [ GET ] `/user/:id/notebook/:notebookid/notes`

Fetches the notes for a given user and for the given notebook. This does not return the contents of the notes. By default fetches the current day notes.

### [ GET ] `/user/:id/notebook/:notebookid/notes?extended=true`

Same as above, but when the extended parameter is set in the URL, the server will also send the contents of each note.  By default fetches the current day notes.

### [ GET ] `/user/:id/notebook/:notebookid/notes?date=2015-04-16`

Fetches the notes for the given date. Note that the date has to encoded in the URL.

### [ GET ] `/user/:id/notebook/:notebookid/notes?date=2015-03`

Fetches the notes for an entire month. The above URL, fetches the notes for the month of March, 2015.

### [ GET ] `/user/:id/notebook/:notebookid/notes?summary=true`

Fetches a summary of the notes. This usually gives an indication of the number of notes present, and the number of completed notes.
If it's not a task based notebook, all notes will be marked as completed.

### [ GET ] `/user/:id/notebook/:notebookid/note/:id

Fetches the notes with the given ID. Can be passed the `extended` parameter to fetch the note's contents as well.

#### Notes

1. Some of the above query string parameters can be combined. Such as the `extended` and the `date` parameter can be combined to get the notes and their content for a certain date. Same can be done for `month`.
2. Since `extended` and `summary` are contradicting to each other, if the `summary` parameter is present, it'll take precedence over the `extended` parameter.

### [ POST ] `/user/:id/notebook/:notebookid/note`

Can be used to create a notebook.

### [ PUT ] `/user/:id/notebook/:notebookid/note/:id`

Can be used to update an existing note.

### [ DELETE ] `/user/:id/notebook/:notebookid/note/:id`

Can be used to delete an existing note.

### [ POST ] `/user/:id/notebook/:notebookid/note/:id/check`

Can be used to mark a note as checked. This can be only done for notes that are present inside a task based notebook.

### [ POST ] `/user/:id/notebook/:notebookid/note/:id/uncheck`

Can be used to mark a completed note as incomplete. This can be only done for notes that are present inside a task based notebook and belong to the current day.
