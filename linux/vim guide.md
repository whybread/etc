# VIM Guide

## 1. Split Screen
### 1-1. Vertical split
\<filename\> is optional.

	:split <filename>
	:sp <filename>
	:10sp <filename>
	:new <filename>
### 1-2. Horizontal split
Similarly

	:vsplit <filename>
	:vs <filename>
	:10vs <filename>

### 1-3. Cursor movement
We can change cursor among multiple split screens.

	Ctrl + w, w // move to next 
	Ctrl + w, W // move to prev
	Ctrl + w, [H | J | K | L] // move the cursor to a certain direction

### 1-4. Screen modify
We can modify each screen's size.
These are some relative ones.

	Ctrl + w, = // same same
	Ctrl + w, _ // maximize this screen's height.
	Ctrl + w, | // maximize this screen's width.
We can also choose the amount to increase/decrease.

	Ctrl + w, [n] + // height +n
	Ctrl + w, [n] - // height -n
	Ctrl + w, [n] > // width +n
	Ctrl + w, [n] < // width -n
	
We can also exchange the locations of two screens.

	Ctrl + w, r // exchange this screen location with the next one.

### 1-5. Quit split
We can quit one split only, or all together whether you want.

	:q // quit this screen
	:qa // quit all screens
	Ctrl + w, o // quit all screens except for current one.
