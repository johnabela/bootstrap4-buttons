# bootstrap4-buttons
A collection of additional buttons for bootstrap 4.

# A few notes
These buttons utilize css "_:root_", for example:

```css
--btn-btn-danger-bgcolor: #dc3545;
--btn-btn-danger-bgcolor-hover: #424242;
--btn-btn-danger-text-color: #fff;
--btn-btn-danger-text-hover-color: #fff;
```

These buttons are best used with a div that has all padding removed, via [bootstrap spacing notation](https://getbootstrap.com/docs/4.0/utilities/spacing/#notation) `p-0`, for example:

```css
<div class="card-footer p-0">
    <button type="submit" class="btn btn-btn"><i class="fa fa-arrow-circle-right"></i> Press to sign in&hellip;</button>
</div>
```
There are a number of things happening to these buttons that the default bootstrap 4 buttons do not do. Let us take a look at the css for one:

```css
.btn-btn-danger {
	color: var(--btn-btn-danger-text-color);
	background-color: var(--btn-btn-danger-bgcolor);
	border-color: var(--btn-btn-danger-bgcolor);
	font-weight: bold;
	letter-spacing:1px;
	text-align: left !important;
	display: block;
	width: 100%;
	border-top-right-radius: 0px !important;
	border-top-left-radius: 0px !important;
}
```
You will see that we are applying a **bold** font weight, we are using a 1px letter spacing, we are applying a `text-left !important` _(which saves us having to apply: `text-left` to every button)_, we are using '_display:block_' _(which saves us having to apply: `btn-block` to every button)_ and using '_width:100%_' just to make sure the button is full width, and we are doing an _!important_ on removing the _top radius_ of both the top left and top right, so it looks properly inside of the _card-footer_ div. These could be applied to the default bootstrap '_btn_' if you wanted to save some file size and remove them from the source code and instead apply them to just a '_btn_', but in the scope of not wanting to affect the default bootstrap 4 code, within this particular css file, the decision was made to do it this way.

# btn-btn

The '_btn-btn_' is very close to the standard '_btn-primary_', however the blue is a darker blue, which is just a personal preference of mine over the '_btn-primary_' color.

# btn-danger

The '_btn-danger_' is the same color as the standard bootstrap 4 '_btn-danger_' but in order to get all of the above mentioned css attributes applied to the button, it was just easier to go this route.

# all the other buttons...

Pretty much all of the other buttons within this css file are custom selected colors to match what has been needed over time as more button colors have been found to be necessary to add.
