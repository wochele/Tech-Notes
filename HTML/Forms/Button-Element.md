# Button Element

- [Button Element - MDN]()

```html
<form action="/my-handling-form-page" method="post">
    <div>
        <label for="name">Name:</label>
        <input type="text" id="name" name="user_name" />
    </div>
    <div>
        <label for="mail">E-mail:</label>
        <input type="email" id="mail" name="user_mail" />
    </div>
    <div>
        <label for="msg">Message:</label>
        <textarea id="msg" name="user_message"></textarea>
    </div>
    
    <div class="button">
        <button type="submit">Send your message</button>
    </div>
</form>
```

- A button can be of three types: submit, reset, or button.
  - A click on a submit button sends the form's data to the web page defined by the action attribute of the <form> element.
  - A click on a reset button resets all the form widgets to their default value immediately. From a UX point of view, this is considered bad practice.
  - A click on a button button does... nothing! That sounds silly, but it's amazingly useful to build custom buttons with JavaScript.
