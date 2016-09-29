# Label Element

- [Label - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label)

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

The `<div>` elements are there to conveniently structure our code and make styling easier (see below). Note 
the use of the for attribute on all `<label>` elements; it's a formal way to link a label to a form widget. 
This attribute references the id of the corresponding widget. There is some benefit to doing this. The most 
obvious one is to allow the user to click on the label to activate the corresponding widget
