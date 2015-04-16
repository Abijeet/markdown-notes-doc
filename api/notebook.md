# The notebook API

### [ GET ] `/user/:id/notebook/:notebookid/notes`

Fetches the notes for a given user and for the given notebook. This does not return the contents of the notes. By default fetches the current day notes.

### [ GET ] `/user/:id/notebook/:notebookid/notes?extended=true`

Same as above, but when the extended parameter is set in the URL, the server will also send the contents of each note.  By default fetches the current day notes.

### [ GET ] `/user/:id/notebook/:notebookid/notes?date=2015-04-16`

Fetches the notes for the given date. Note that the date has to encoded in the URL.

### [ GET ] `/user/:id/notebook/:notebookid/notes?month=3`

Fetches the notes for an entire month. Month index starts with 1. So January is 1, Feburary is 2 and so on.

### [ GET ] `/user/:id/notebook/:notebookid/notes?summary=true`

Fetches a summary of the notes. This usually gives an indication of the number of notes present, and the number of completed notes.
If it's not a task based notebook, all notes will be marked as completed.

#### Notes

1. Some of the above query string parameters can be combined. Such as the `extended` and the `date` parameter can be combined to get the notes and their content for a certain date. Same can be done for `month`.
2. Since `extended` and `summary` are contradicting to each other, if the `summary` parameter is present, it'll take precedence over the `extended` parameter.
3. Similarly `month` will take precendence over the `date` parameter. 

