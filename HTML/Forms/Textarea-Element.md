# Textarea Element

- [Textarea Element - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea)

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

If you want to define the default value of a `<textarea>`, you just have to put that default value between the starting 
and ending tag of the `<textarea>` element, like this:

```html
<textarea>by default this element is filled with this text</textarea>
```

