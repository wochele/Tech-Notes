# Input Element

- [Input Element - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input)

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

On the `<input>` element, the most important attribute is the *type* attribute. This attribute is extremely important 
because it defines the way the `<input>` element behaves. It can radically change the element so pay attention to it. 
In our example we use the value text—the 
default value for this attribute. It represents a basic single-line text field that accepts any kind of text without control 
or validation. We also use the value email that defines a single-line text field that only accepts a well-formed e-mail address. 
This last value turns a basic text field into a kind of "intelligent" field that will perform some checks on the data typed by the user.

The `<input>` tag is an auto-closing element, which means that if you want to formally close the element, you have to add a "/" 
at the end of the element itself and not a closing tag.

