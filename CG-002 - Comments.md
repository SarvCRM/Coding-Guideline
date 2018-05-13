# Comments

All JS comments **MUST** be encapsulated in `/**/`.

~~~js
// previous code

/* Added By FirstName LastName - Jan 5, 2000 */
/* REASON FOR CHANGE */
// developers code
/* END */

// previous code
~~~

All one-line comments in PHP **MUST** use `// ` only. Mind the space after `//`.

All comments except one-line comments in PHP **MUST** use `/**/` only.

`/*` and `*/` **MUST** be on their own lines except for one-line comments in JS.

All lines between `/*` and `*/` **MUST** start with ` * `. Mind the space before and after `*`.

Each developer **MUST** indicate start and end of his/her code insertion with the exact following pattern which **MUST NOT** be indented.

~~~php
<?php
	// previous code

//******************************************//
//	Added By FirstName LastName
//	Jan 5, 2000
//******************************************//
// REASON FOR CHANGE
	// developers code
//******************************************//

	// previous code
?>
~~~

There **MUST NOT** be any comment on the following directories:
- /cache/*
- /modules/[MODULE_NAME]/language/
- /modules/[MODULE_NAME]/metadata/



		





