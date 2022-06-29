# Acrobat PDF JavaScript

My learning of scripting the PDF Forms.

## Dropdown List

Instead of adding items manually using the properties dialogue box, use the following script to add the list items at one go.

```JS
  var l = [" ", "a", "b", "c", "d"];
  var lst = this.getField("Dropdown1");
  lst.setItems(l);
```

Multiple dropdown menu having the same content can be created repeating the definition and setItems.  

## Check Box

## Text Field Email Validation

Run the custom validation script.

```JS
var email = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,4})+$/; 
if (event.value!="")
  {
    if (!email.test(event.value))
      {
        event.rc = false;
        app.alert("\"" + event.value + "\" is not a valid email address.");
      };
  };
```

