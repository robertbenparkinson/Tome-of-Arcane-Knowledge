# How to Build a Responsive CSS Layout for Both Large and Small Devices 


``` html
<!DOCTYPE html>
<html>
<head>
/* Add this meta tag to head of your html file to allow use of "@media only sceeen and (min-width: 400px)" below  */
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
/* For width smaller than 400px: */
/* The intial background color is set to red

body {
    background-color: red; 
}

/* For width 400px and larger: */
/* When the screen is less than 400px it will change the background color to green */
@media only screen and (min-width: 400px) {
    body { 
       background-color: green; 
    }
}
</style>
</head>
<body>

<p style="margin-top:360px;">Resize the browser width and the background color will change at 400px.</p>

</body>
</html>

```
