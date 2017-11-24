# javaScript Notes

### A simple little javaScript button and function that changes the text in the <p> tag with the 'id="demo"'.  

```html
<html>
<head>
<body>

<p id="demo"></p>

<button type="button" onclick="myFunction()">Click Me!</button>

<script>
function myFunction() {
    document.getElementById("demo").innerHTML = "Wow, it works!";
}
</script>

</body>
</head>
</html>

```



