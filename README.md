# flaw.less
16 column Grid System Designed by Windfall Studios

## Installation

Download files and place them in site directory.

Link to files in header

```shell
<link rel="stylesheet" href="/assets/css/app.css">
<script src="assets/js/jquery-2.0.2.min.js"></script>
```

Link to files in Footer

```shell
<script src="/assets/js/flawless.js"></script>
```

Boom! Good to go!


## Features

### Customize

Options.less file allows you to set custom variables. You should be sure to change the following:

1. Font Size
2. Main/secondary theme colors
3. Font families


### Tutorial

Create a row and specify how the columns should be broken up:

```html
<div class="row two">
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
</div>
<div class="row three">
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
      	<div class="column">
		<p>Lorem ipsum</p>
	</div>
</div>
<!-- four, five, six, seven, eight, nine, ten, eleven, twelve, thirteen, fourteen, fifteen, sixteen-->
<!-- fourths, sixths, sevenths, eighths, ninths, tenths, elevenths,twelfths, etc can also be used -->
```

Columns will automatically have space between them. To eliminate space, declare the row to have "no-gutter"

```html
<div class="row no-gutter two">
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
</div>
```

You can use Modal boxes and expanding content sections to make content clean

```html
<div class="row no-gutter thirds">
	<div class="column">
		<h1>This is heading 1</h1>
		<h2>This is heading 2</h2>
		<h3>This is heading 3</h3>
		<h4>This is heading 4</h4>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
		<h5>This is heading 5</h5>
		<h6>This is heading 6</h6>
	</div>
	<div class="column">
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
		<h2 class="expander" data-expand="#expand-me">Link Title</h2>
		<div id="expand-me" class="expandable">
			<p>Content</p>
			<li class="modalbtn" data-modal="#modalname"><a>Link Title</a></li>
		</div>
	</div>
	<div class="column">
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
	</div>
</div>
```

Notice that columns stretch to match the column with the most content in it. 
```diff 
+ Fancy!
```

Columns are positioned relative so that adding absolute items inside is a breeze!

Space out columns by pushing them. This example will give you a 50% margin on the left side, and two even columns on the right:

```html
<div class="row no-gutter fourths">
	<div class="column push-two">
		<p>Lorem ipsum</p>
	</div>
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
</div>
<!-- push-one, push-two, push-three, push-four, push-five, push-six, etc -->
```

Note that a push will push by its column length. So if you have a row with a class of "three" the push-one will react accordingly.
You cannot push a column past the number of columns in a row. For instance, push-ten will not function in a "row two"

You can declare a row to wrap it's columns as well. 

```html
<div class="row wrap two">
	<div class="column push-two">
		<p>Lorem ipsum</p>
	</div>
	<div class="column">
		<p>Lorem ipsum</p>
	</div>
</div>
<!-- row wrap three, row wrap four-->
```
