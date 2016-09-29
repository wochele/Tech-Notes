# Form

[Form tutorial](http://www.tutorialspoint.com/html/html_forms.htm)

```html
<form action="Script URL" method="GET|POST">
    form elements like input, textarea etc.
</form>
```

#### Form Attributes

Attribute | Description
---|---
action | Backend script ready to process your passed data
method | Method to upload, typically POST or GET

#### Text input

- **Single-line text input controls** - This control is used for items that require only one line of user input, such as search boxes or names. They are created using HTML `<input>` tag.
    - Attributes
        - **type** - Indicates the type of input control and for text input control it will be set to *text*.
        - **name** - Used to give a name to the control which is sent to the server to be recognized and get the value.
        - **value** - This can be used to provide an initial value inside the control.
        - **size** - Allows to specify the width of the text-input control in terms of characters.
        - **maxlength** - Allows to specify the maximum number of characters a user can enter into the text box.
- **Password input controls** - This is also a single-line text input but it masks the character as soon as a user enters it. They are also created using HTMl `<input>` tag.
- **Multi-line text input controls** - This is used when the user is required to give details that may be longer than a single sentence. Multi-line input controls are created using HTML `<textarea>` tag.
    - Attributes
        - **name** - Used to give a name to the control which is sent to the server to be recognized and get the value.
        - **rows** - Indicates the number of rows of text area box.
        - **cols** - Indicates the number of columns of text area box
