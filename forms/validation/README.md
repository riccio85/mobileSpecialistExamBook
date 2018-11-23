## Patterns
#### between 3 and 15 characters
`<input … maxlength="15" minlength="3">`
#### Https url only
```html
<input type=”url” pattern="^((https):\/\/(www.)[a-z0-9]+\.[a-z]+(\/[a-zA-Z0-9#]+\/?)*$)"/>
```
#### Obbligatorio http o https
```html
 pattern="^((https?):\/\/(www.)[a-z0-9]+\.[a-z]+(\/[a-zA-Z0-9#]+\/?)*$)"
 ```
#### tel format xxxx-xxx-xxxx
```html
<input type="tel" pattern="^\d{4}-\d{3}-\d{4}$" >
```
#### email pattern
```html
“^[a-zA-Z0-9.!#$%&'*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$”
```
#### format #3b5998 or #000
```html
<input type="text" pattern="^#+([a-fA-F0-9]{6}|[a-fA-F0-9]{3})$" >
```
#### Custom validation message
```javascript
var email = document.getElementById("mail");
email.addEventListener("input", function (event) {
  if (email.validity.typeMismatch) {
    email.setCustomValidity("I expect an e-mail!");
  } else {
    email.setCustomValidity("");
  }
});
```
#### Form check validity validation message
```javascript
var form= document.getElementById('myForm');
form.addEventListener("submit", function(evt) {
  if (form.checkValidity() === false) {
    evt.preventDefault();
    alert("Form is invalid - submission prevented!");
    return false;
  } else {
    evt.preventDefault();
    alert("Form is valid - submission prevented to protect privacy.");
    return false;
  }
});
```
