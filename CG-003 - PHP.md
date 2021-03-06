# 1. Keywords and True/False/Null

PHP [keywords] **MUST** be in lower case.

The PHP constants `true`, `false`, and `null` **MUST** be in lower case.

[keywords]: http://php.net/manual/en/reserved.keywords.php


# 2. Classes

Class names **MUST** be declared in `StudlyCaps`.

The opening brace for the class **MUST** go on its own line; the closing brace for the class **MUST** go on
the next line after the body.


## 2.1. Extends and Implements

The `extends` and `implements` keywords **MUST** be declared on the same line as the class name.


## 7.2. Properties, Constants and Variables

Class constants **MUST** be declared in all upper case with underscore separators.

Class properties **MUST** be declared in `camelCaps()`.

There **MUST NOT** be more than one property declared per statement.

All global variables **MUST** be declared at first row and all globals **MUST** be at one line.

~~~php
<?php
namespace Vendor\Model;
class ClassName extends ParentClass implements \ArrayAccess, \Countable
{
	global $fistVar, $secondVar;
	const VERSION = '1.0';
	const DATE_APPROVED = '2012-06-01';
	var $thirdVar;
}
?>
~~~


## 2.3. Methods and Functions

Method names **MUST** be declared in `StudlyCaps()`.

Visibility **MUST** be declared on all methods.

Method names SHOULD NOT be prefixed with a single underscore to indicate protected or private visibility.

There **MUST** be two empty lines before any method.

Method names **MUST NOT** be declared with a space after the method name. The opening brace **MUST** go on
its own line, and the closing brace **MUST** go on the next line following the body.

There **MUST NOT** be a space after the opening parenthesis, and there **MUST NOT** be a space before the closing parenthesis.

In the argument list, there **MUST NOT** be a space before each comma, and there **MUST** be one space after each comma.

Method arguments with default values **MUST** go at the end of the argument list.

A method declaration looks like the following. Note the placement of parentheses, commas, spaces, and braces:

~~~php
<?php
namespace Vendor\Package;
class ClassName
{
	var $fistVar;


	public function FirstMethod($arg1, &$arg2, $arg3=[])
	{
		// method body
	}


	public function SecondMethos($arg1, $arg2=null)
	{
		// method body
	}
}
?>
~~~


## 2.4. `abstract`, `final`, and `static`

When present, the `abstract` and `final` declarations **MUST** precede the visibility declaration.

When present, the `static` declaration **MUST** come after the visibility declaration.

~~~php
<?php
namespace Vendor\Package;
abstract class ClassName
{
	protected static $fistVar;


	abstract protected function FirstFunc();


	final public static function SecondFunc()
	{
		// body
	}
}
?>
~~~

## 2.5. Method and Function Calls

When making a method or function call, there **MUST NOT** be a space between the method or function name
and the opening parenthesis, there **MUST NOT** be a space after the opening parenthesis.

There **MUST NOT** be a space before the closing parenthesis.

In the argument list, there **MUST NOT** be a space before each comma, and there **MUST** be one space after each comma.

~~~php
<?php
FirstFunc();
$fistVar->FirstFunc($arg1);
ClassName::FirstFunc($arg2, $arg3);
?>
~~~

Argument lists MAY be split across multiple lines, where each subsequent line is indented once. When doing so,
the first item in the list **MUST** be on the next line, and there **MUST** be only one argument per line.

~~~php
<?php
$fistVar->FirstFunc(
	$longArgument,
	$longerArgument,
	$muchLongerArgument);
?>
~~~


# 3. Control Structures

There **MUST** be one space after the control structure keyword.

There **MUST NOT** be a space after the opening parenthesis.

There **MUST NOT** be a space before the closing parenthesis.

The opening brace **MUST** go on its own line; the closing brace.

The structure body **MUST** be indented once.

The closing brace **MUST** be on the next line after the body.

The body of each structure **MUST** be enclosed by braces. This standardizes how the structures look, and reduces
the likelihood of introducing errors as new lines get added to the body.


## 3.1. `if`, `elseif`, `else`

An `if` structure looks like the following. Note the placement of parentheses, spaces, and braces.

The keyword `elseif` SHOULD be used instead of `else if` so that all control keywords look like single words.

~~~php
<?php
if ($firstVar == true && $secondVar > 10)
{
	// if body
}
elseif ($firstVar == true || $thirdVar == false)
{
	// elseif body
}
else
{
	// else body;
}
?>
~~~


## 3.2. `switch`, `case`

A `switch` structure looks like the following. Note the placement of parentheses, spaces, and braces.

The `case` statement **MUST** be indented once from `switch`, and the `break` keyword (or other terminating keyword)
MUST be indented at the same level as the `case` body.

There **MUST** be a comment such as `// no break` when fall-through is intentional in a non-empty `case` body.

~~~php
<?php
switch ($expr)
{
	case 0:
		echo 'First case, with a break';
		break;
	case 1:
		echo 'Second case, which falls through';
		// no break
	case 2:
	case 3:
	case 4:
		echo 'Third case, return instead of break';
		return;
	default:
		echo 'Default case';
		break;
}
?>
~~~


## 3.3. `while`, `do while`

A `while` statement looks like the following. Note the placement of parentheses, spaces, and braces.

~~~php
<?php
while ($expr)
{
	// structure body
}
?>
~~~

Similarly, a `do while` statement looks like the following. Note the placement of parentheses, spaces, and braces.

~~~php
<?php
do
{
	// structure body;
}
while ($expr);
?>
~~~


## 3.4. `for`

A `for` statement looks like the following. Note the placement of parentheses, spaces, and braces.

~~~php
<?php
for ($i=0; $i<10; $i++)
{
	// for body
}
?>
~~~


## 3.5. `foreach`

A `foreach` statement looks like the following. Note the placement of parentheses, spaces, and braces.

~~~php
<?php
foreach ($iterable as $key=>$value)
{
	// foreach body
}
?>
~~~


## 3.6. `try`, `catch`

A `try catch` block looks like the following. Note the placement of parentheses, spaces, and braces.

~~~php
<?php
try
{
	// try body
}
catch (FirstExceptionType $e)
{
	// catch body
}
catch (OtherExceptionType $e)
{
	// catch body
}
?>
~~~


# 4. Operators and Assignment

All Operatoors and Assignments **MUST** have a single space befor and after them.

Check `Control Structures` for their style.

PHP array **MUST** be declared such as `array()`. Pay attention to casing and spaces.

Each element of a PHP array **MUST** be on a new line.

~~~php
<?php
$firstVar = 1;
$firstVar += 1;
$firstVar .= '1';
$firstVar++;
$firstVar = $firstVar.$secondVar;
$firstVar = array();
$firstVar = array(
	'first',
	'second',
	0 => 'third');
?>
~~~
