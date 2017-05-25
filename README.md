# axl-flat-ui
My own minimalistic flat UI framework. Based from [Bootstrap 3](http://getbootstrap.com/) with [Raleway](https://fonts.google.com/specimen/Raleway) google font.

## Initial Components

- Headers
- Dividers
- Paragraphs
- Buttons (Primary)
- Buttons (Bordered)
- Button and Bordered Groups (Horizontal and Vertical)
- Form Inputs
  a. Textbox
  b. Textarea
- List (Block and Inline)

## How to use

### Basic index.html file

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Axl UI</title>

    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css?family=Raleway:300,400,700" rel="stylesheet">
    
    <!-- Refer the axl-flat-ui stylesheet -->
    <link rel="stylesheet" href="css/style.css">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <!-- Your codes here... -->

    <!-- Scripts -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
  </body>
</html>
```

### Headers

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

### Dividers

```html
<div class="container"><div class="divider"></div></div>
```
The `.container` is optional. It's purpose is for the `.divider` to conform to the page's container width or else it will take the whole browser's width.

### Paragraphs

A simple, clean paragraph that compliments the thickness of the headers.

```html
<p>Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor.</p>
```

### Buttons 

These are the predefined buttons and bordered links.
**Primary** buttons has a default fill color rather the **bordered** ones that only has borders and will have a fill color upon hover.

```html
<!-- Primary -->
<button class="button btn__red">Submit</button>
<button class="button btn__green">Reset</button>
<button class="button btn__blue">Cancel</button>
<button class="button btn__grey">OK</button>
```

```html
<!-- Bordered -->
<button class="bordered bordered__red">Read More</button>
<button class="bordered bordered__green">View Post</button>
<button class="bordered bordered__blue">Comment</button>
<button class="bordered bordered__grey">Share</button>
```

### Group - Horizontal and Vertical

Group aligns the buttons and bordereds horizontally and vertically. As of now, it was intended only for the **Primary** and **Bordered** buttons.

```html
<!-- Groups using the `ul` tag -->
<ul class="group__horizontal">
  <li class="bordered bordered__red">Create</li>
  <li class="bordered bordered__green">Edit</li>
  <li class="bordered bordered__blue">Delete</li>
</ul>
<ul class="group__horizontal">
  <li class="button btn__red">Cancel</li>
  <li class="button btn__green">Save</li>
  <li class="button btn__blue">Publish</li>
</ul>
```

```html
<!-- Groups using `div` tag -->
<div class="group__vertical">
  <button class="bordered bordered__red">Read More</button>
  <button class="bordered bordered__green">View Post</button>
  <button class="bordered bordered__blue">Comment</button>
</div>
<div class="group__vertical">
  <button class="button btn__red">Delete Post</button>
  <button class="button btn__green">Submit Post</button>
  <button class="button btn__blue">Publish</button>
  <button class="button btn__grey">Make as draft</button>
</div>
```
### List - Block and Inline

Unlike **Group**, **List** is primarily intended for `li` and `a` for them to display as block(horizontally) and inline(vertically).

```html
<!-- Each `li` Will display as block element -->
<ul class="list">
  <li>Home</li>
  <li>About Us</li>
  <li>Projects</li>
  <li>Contact Us</li>
</ul>
```

```html
<!-- Each `li` Will display as inline-block element -->
<ul class="list__inline">
  <li>Home</li>
  <li>About Us</li>
  <li>Projects</li>
  <li>Contact Us</li>
</ul>
```

### Form Inputs

```html
<form action="">
  <div class="form-group">
    <label for="name" class="hidden">Name</label>
    <input type="text" name="name" placeholder="Name">
    <a href="" class="close"></a>
  </div>

  <div class="group__horizontal">
    <button type="button" class="button btn__grey">Reset</button>
    <button type="button" class="button btn__blue">Submit</button>
  </div>
</form>
```

`.for-group` is just a fancy container for related form inputs. For example, `<label></label>` and its corresponding `<input type="text" />`.
