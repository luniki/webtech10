!SLIDE subsection
# Operators #

!SLIDE
# Arithmetic #
	+ - * / %

!SLIDE
# Comparison #
	=== !===
	==  !=
	< <= > >=

!SLIDE
# Compound assignment #
	+= -= *= /= %=

!SLIDE
# Logical #
	&& || !

!SLIDE
# Bitwise #
	& | ^ >> >>> <<

!SLIDE
# Ternary Operator #
	true ? "hoge" : "fuga"

!SLIDE
# Increment and decrement #
	++fuga --fuga
	hoge++ hoge--

!SLIDE
# Concatenation #
	"foo" + "bar"

!SLIDE bullets
# + #
* addition and concatenation
* both numbers: add them
* else: convert to strings and concat

!SLIDE execute
	@@@ javaScript
	result = "¥" + 4 + 2

!SLIDE execute
# / #

	@@@ javaScript
	result = 23 / 13

!SLIDE bullets
# == != #
* equal/not equal use type coercion
* use === and !== instead

!SLIDE
	@@@ javaScript
	   '' == '0'       // false
	    0 == ''        // true
	    0 == '0'       // true

	false == 'false'   // false
	false == '0'       // true

	false == undefined // false
	false == null      // false
	null  == undefined // true

!SLIDE bullets
# && #
* guard operator
* first operand truthy: second operand
* else: first operand
* useful for checking for null objects before accessing their attributes
* var foo = o && o.getFoo();

!SLIDE bullets
# || #
* default operator
* first operand truthy: first operand
* else: second operand
* for setting default values:
* var hoge = otherHoge || "default";

!SLIDE
# typeof #

	@@@ javaScript
	typeof aNumber     === 'number'
	typeof aString     === 'string'
	typeof aBoolean    === 'boolean'
	typeof aFunction   === 'function'
	typeof anObject    === 'object'
	typeof anArray     === 'object'    // !
	typeof aNull       === 'object'    // !
	typeof anUndefined === 'undefined'

