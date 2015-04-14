# Managing a note

Once logged in this will be the page shown to the user. This is the main page from where the user can edit, add and delete his notes/tasks.

![Editing a notebook](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/editing-notebook.png)

## Notes on the image

The numbers in the prefix of the headings below represent the numbers in the image.

### 1. Icons in the textbox

A normal task/note will display two icons - **Delete** and **Edit**. If a task/note is inside a **Task** based notebook, it will also contain a **Checkbox** that denotes the state of the task. When a user checks a checkbox, it tells the system that the user has finished that task.

These icons will be only visible when the task has focus.

### 2. Note-level buttons

#### a. Add new note

Clicking on this button will add a note editor at the bottom of all existing tasks/notes and will put the focus in the editor, so the user can begin typing immediately.

#### b. Settings 

This will popup out the following dialog - ![Editing notebook properties](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/editing-notebook-props.png). 

The functionality of this dialog is similar to the [Add new notebook](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#adding-a-notebook) dialog.

Clicking on the **delete** button will delete the notebook alongwith all the notes contained in the task.

### 3. Note date

On an active notebook this shows the date from the current, clicking on it will open the calendar. The description for this screen can be found [here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#the-calendar).

### 4. The status bar

This status bar contains application related messages. If a user carried out an action such as - Marking a note as completed, this would contain a status message that shows whether that action was executed successfully by the system.

If there is an error though, the system will inform that to the user via a dialog box, and will try to offer them a resolution. So the status bar will generally only contain messages when actions have been completed successfully.

### 5. List of notebooks

This area of the UI shows the user the list of notebooks created by them in the system. The UI is a checkbox based system that shows the currently open notebooks as checked checkboxes.

- Clicking on an unchecked checkbox will open the corresponding notebook as a tab in the UI, and will transfer focus to the first note in the UI.
- Clicking on an checked checkbox will close the corresponding notebook.

The UI also provides the user a way to create new notes by click on the **+ New notebook** link. This will bring up a dialog box described [here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#adding-a-notebook).

### 6. Tabbed interface

The UI uses a tabbed based interface where each tab represents a notebook. This allows users to use an interface that they are familiar with (a browser). 

### 7. Application-level buttons

#### a. My Profile

This will open up the My Profile dialog described [here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/user-management.md#profile).

#### b. Logout

This will logout the user and bring them to the login page, described [here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/user-management.md#sign-in).

### 8. Date on in progress tasks

On an in-progress task, the last modified on date is shown.

### 9. Date on completed tasks

On a completed task, the completed on date is shown.

# The Calendar

The calendar maintains a track of the completed tasks on a monthly basis. It can be used to navigate between completed notes and to create/view future notes.

![The Calendar](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/notes-calendar.png)

## Notes on the image

### 1. The current day

The calendar highlights the current day in gray. The color in the final UI might be different, but there will be an indication of the current day.

### 2. Completed tasks

Day's in the past may have a task label if any tasks have been completed on that day. For example, the calendar above shows the label "5 Tasks" under 11th of March, 2015. This means that on this day, 5 tasks were completed by the user.

### 3. Upcoming tasks

Day's in the future may also have a task labels. It is possible for the user to create tasks in the future. These notes will appear automatically on that day for the user, alongwith any tasks that might have carried forward from previous days. This will allow the system to also function as a daily reminder.

### 4. Current calendar month

User can toggle between calendar months, using these dropdowns.

### 5. Calendar title

The title of the calendar depends on the notes' whose calendar the user is viewing. The notes' name is displayed as **Calendar for "xyz" notebook**, where "xyz" is the name of the notebook.

### 6. The "today" button

Clicking on this button will take the user directly to today's note.

# Viewing older notes

Older notes can be viewed via the calendar ([described here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#the-calendar) ). The older notes view is simply a modified version of the actual notes view. This view shows the users the tasks that were completed by them on the day selected on the calendar. It is not possible to make any sort of modifications to past notes.

> Since this gives an indication of tasks that were completed, the older notes view is only applicable for tasks based notebooks.

![The older notes view](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/older-notes.png)

## Notes on the image

### 1. Add new notes

As expected, the add new notes button will not be present when looking at an older note.

### 2. Travelling between notes

#### a. The "Go to Today's notes" button

This button will appear whenever we are viewing notes in the past or in the future. This allows you to quickly travel to today's notes.

#### b. The date

The date shown is the date for which the user is viewing the notes. The user can go back to the calendar view ([described here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#the-calendar)) by clicking on this button.

### 3. Icons/Dates on notes

The user will not be shown any dates on a past note, since the completed on date is the date on which the note is shown

Icons will also remain disabled since this note/task has already been completed.


# Adding a notebook

When the user clicks on the **new notebook** described [here](https://github.com/Abijeet/markdown-notes-doc/blob/master/ui/notes.md#5-list-of-notebooks), a dialog box pops-up that allows the user to add a new notebook.

![New notebook dialog](https://raw.githubusercontent.com/Abijeet/markdown-notes-doc/master/img/new-book.png)

### 1. Notebook name

The notebook name can contain any characters but needs to be unique for the user.

### 2. Shrinking notes

Notes when in focus automatically expand to the same height as their content, but when the user focuses out, this property will determine with the notes shrink to a single line, or stay at their current height.

### 3. Task based notebooks

Task based notebooks will have a checkbox in every note. Clicking on the checkbox will mark the note/task as completed. These notebooks track what notes are completed on daily basis, and uncompleted notes will be added automatically to the next day.
