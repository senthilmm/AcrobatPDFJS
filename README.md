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

## Check Box and Text Field

Choosing the export value to fill the text field. Use the mouseup action of the checkbox to run the script.

```JS
var check = (this.getField("Checkbox1").valueAsString=="Yes") ? "Select" : "Unselect";
this.getField("Text1").value = check;
}
```

## Text Field with Default Value 

Text field with default value displayed in gray, when the field is filled, the custom format script is executed.

```JS
if(event.value=="")
{
event.value="File Name";
event.target.textColor = color.gray;
}else
{
event.target.textColor = color.black;
}
```

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

