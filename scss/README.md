# How to use

## _variables.css

`_variables.scss` contains the default variables.

```scss
// Fonts

$font_primary: "Raleway";
$font_secondary: $font_primary;
$font-size: 12px;
$weight-thin: 300;
$weight-normal: 400;
$weight-bold: 700;

// Colors

$primary-color-dark:    #D32F2F;  // Darkened Base color
$primary-color:         #F44336;  // Base color
$primary-color-light:   #FFCDD2;  // Lightened Base color

$primary-text-color:    #212121;  // Headings color
$secondary-text-color:  #757575;  // Contents color
$divider-color:         #BDBDBD;  // Divider color (also for, not so important content)

$accent-color:          #7C4DFF;  // Emphasis color
$text-icon-color:       #FFFFFF;  // Text/Icon color(i.e. text inside buttons, icons)

// Custom Colors

$color-green: #39AEA9;
$color-green-light: lighten($color-green, 5);
$color-green-dark: darken($color-green, 10);

$color-blue: #1E88E5;
$color-blue-light: lighten($color-blue, 5);
$color-blue-dark: darken($color-blue, 10);
$color-blue-green: #185a9d;

$color-grey: #8F8F8F;
$color-grey-light: lighten($color-grey, 5);
$color-grey-dark: darken($color-grey, 20);

```

## style.css

This is where all the default stylings are contained.

```scss
@import '_variables';

// Resets ========================================

* {
  transition: all 0.3s;
}

*, html, body, div {
  font-family: $font_primary;
  box-sizing: border-box;
  color: $primary-text-color;
}

p {
  font-family: $font_secondary;
  font-size: $font-size;
  font-weight: $weight-thin;
  line-height: 22px;
}

ul, ol {
  padding: 0;
  margin: 0;
  li {
    font-size: $font-size;
    font-weight: $weight-thin;
  }
}

label {
  font-weight: $weight-bold;
}

a, a:hover, a:focus, a:visited {
  color: inherit;
  text-decoration: none;
  font-size: $font-size;
  font-weight: $weight-thin;
}

// Utilities =====================================

.divider {
  border-bottom: 1px solid lighten($divider-color, 20);
  margin: 20px 0px;
}

.hidden {
  display: none;
}

.float-right {
  float: right;
}

.float-left {
  float: left;
}

.text-center {
  text-align: center;
}

.center {
  margin-left: auto;
  margin-right: auto;
}

.red { color: $primary-color; }
.blue { color: $color-blue; }
.green { color: $color-green; }
.grey { color: $color-grey; }

// Headers =======================================

h1, h2, h3, h4, h5, h6 {
  font-family: $font_primary;
  font-weight: $weight-thin;
  margin: 0.95em 0;
}

// Buttons =======================================

.button {
  // Variables
  $padding-top-bottom: 10px;
  $padding-left-right: 30px;
  $border-bottom-size: 1px;

  // Defaults
  font-size: $font-size;
  color: $text-icon-color;

  padding: $padding-top-bottom $padding-left-right;
  padding-bottom: $padding-top-bottom - $border-bottom-size;
  margin-bottom: 4px;

  border: none;
  border-radius: 2px;
  box-shadow: none;
  // box-shadow: 0px 0px 1px $divider-color;

  transition: all 0.3s;

  &.btn__red {
    background-color: $primary-color;
    // border-bottom: $border-bottom-size solid $primary-color-dark;
  }
  &.btn__red:hover {
    background-color: $primary-color-dark;
  }

  &.btn__green {
    background-color: $color-green;
    // border-bottom: $border-bottom-size solid $color-green-dark;
  }
  &.btn__green:hover {
    background-color: $color-green-dark;
  }

  &.btn__blue {
    background-color: $color-blue;
    // border-bottom: $border-bottom-size solid $color-blue-dark;
  }
  &.btn__blue:hover {
    background-color: $color-blue-dark;
  }

  &.btn__grey {
    color: $text-icon-color;
    background-color: $color-grey;
    // border-bottom: $border-bottom-size solid $color-grey-dark;
  }
  &.btn__grey:hover {
    background-color: $color-grey-dark;
  }
}

// Bordereds =====================================

.bordered {
  // Variables
  $padding-top-bottom: 10px;
  $padding-left-right: 30px;
  $border-bottom-size: 1px;

  // Defaults
  font-size: $font-size;
  background-color: transparent;
  color: $secondary-text-color;

  padding: $padding-top-bottom $padding-left-right;
  padding-bottom: $padding-top-bottom;
  margin-bottom: 4px;

  border: none;
  border-radius: 2px;
  box-shadow: none;
  // box-shadow: 0px 0px 2px $divider-color;
  border: 1px solid $divider-color;
  transition: all 0.3s;

  &.bordered__red:hover {
    background-color: $primary-color;
    border-color: $primary-color;
    color: $text-icon-color;
  }

  &.bordered__green:hover {
    background-color: $color-green;
    border-color: $color-green;
    color: $text-icon-color;
  }

  &.bordered__blue:hover {
    background-color: $color-blue;
    border-color: $color-blue;
    color: $text-icon-color;
  }

  &.bordered__grey:hover {
    background-color: $color-grey;
    border-color: $color-grey;
    color: $text-icon-color;
  }
}

// Groups / Button / Bordered groups =============

.group__horizontal,
.group__vertical {
  display: block;
  margin: 0.5em 0;
}

.group__horizontal > .button,
.group__horizontal > .bordered {
  display: inline-block;
}

.group__vertical > .button,
.group__vertical > .bordered {
  display: list-item;
}

// Form Inputs ===================================

input,
textarea {
  font-size: 0.9em;
  width: 100%;
  padding: 10px 15px;
  border-radius: 2px;
  border: 1px solid $divider-color;
}

input:focus,
textarea:focus {
  outline: none;
}

textarea {
  border: 1px solid $divider-color;
  padding: 10px;
  resize: vertical;
}

.form-group {
  margin: 2px 0px;
}

// Lists =========================================

ul,
ol {
  list-style: none;
}

li {
  padding: 5px 0;
}

.list > li,
.list > a {
  display: block;
}

.list__inline > li,
.list__inline > a {
  display: inline-block;
}
```

## NOTE:
If you want to modify the predefined stylesheets, I suggest that you should create a custom css file.
