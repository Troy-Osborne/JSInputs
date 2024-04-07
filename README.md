To install JSInputs into your file simply place
<script src='InputsJS.js'> </script>
at the top of your file.

Use the function UIJSInitialiseCSS() to return the required CSS.
usually by placing document.write(UIJSInitialiseCSS()) near the beginning of your file.

The somewhere in your body include a div with the ID UserInputJS, this div will automatically be made invisible
if you've correctly imported the stylesheets from UIJSInitialiseCSS().


Examples:
TextInput("Test Title","This is an example input","Default Value");

This is equivalent to 
CustomInput("Test Title",["text"],["Default Value"],["This is an example input"]);
and is just shorthand for a single text input, like prompt();

User Registration:
CustomInput("User Registration",["text","text","text","password","password"],["","","","",""],["Name:","Username:","Email:","Password:","Verify:"]);

File Upload
CustomInput("Upload File",["text","file","color"],["","","#FF0000"],["Name:","File:","Colour Code:"]);

Contact Info
CustomInput("Contact Info",["text","tel","tel","text","text","file"],["First Last","0456123123","38921111","user@domain.com","<unit #>/<st #> <Street Name>, <Suburb or Town> <Postcode or Zipcode>, <State>, <Country>"],["Name:","Personal Phone:","Business Phone:","Email:","Postal Address:","Photo:"],caption="Test");
The 4th input contains the row's labels/captions but
The optional caption="Test" included at the end of the function call is an example of a form caption.
Displayed above the form they're used to include text that isn't specific to a particular input


It should work for most types of html5 inputs, but as currently it only uses the value attribute, things checkboxes might not behave as expected.


"""Note: Unlike other input controls,
a checkbox's value is only included in the submitted data if the checkbox is currently checked. 
If it is, then the value of the checkbox's value attribute is reported as the input's value, or on if no value is set. 
Unlike other browsers, Firefox by default persists the dynamic checked state of an <input> across page loads. 
Use the autocomplete attribute to control this feature. """- https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox

Support for custom objects will be added soon.
