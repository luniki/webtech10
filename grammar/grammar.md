!SLIDE subsection

# Grammar #

!SLIDE

# insignificant Whitespace #
	@@@ javaScript
	var that = this;

!SLIDE
# comments

	@@@ javaScript
	// ...

	/*
		...
	*/

!SLIDE
# Identifier Names

	@@@ javaScript
	/[a-zA-Z_$][a-zA-Z0-9_$]*/

	/*
		really unicode letters:
		[A-Za-z\u00C0-\u1FFF\u2800-\uFFFD]
	*/

!SLIDE code

# Reserved Words

	break     else        new     var
	case      finally     return  void
	catch     for         switch  while
	continue  function    this    with
	default   if          throw
	delete    in          try
	do        instanceof  typeof

!SLIDE code

# Future Reserved Words

	abstract boolean byte char class
	const debugger double enum export
	extends final float goto implements
	import int interface long native
	package private protected public
	short static super synchronized
	throws transient volatile

!SLIDE subsection
# Types

!SLIDE
# Objects

call by sharing


!SLIDE bullets
# Number

* only 64 bit float (IEE 754 double)
* no integers

!SLIDE execute
# decimal fractions #

	@@@ javaScript
	result = 0.1 + 0.2;

!SLIDE execute
# big integers #

	@@@ javaScript
	result = 9007199254740992 + 1

!SLIDE code
# Math object #
	abs ceil floor round
	exp log sqrt pow
	acos asin atan atan2 cos sin tan
	max min	random
	E LN10 LN2 LOG10E LOG2E
	PI SQRT1_2 SQRT2

!SLIDE

	@@@ javaScript
	// convert string to number
	parseInt("17");
	> 17
	parseInt("010");
	> 8

	// always specify base
	parseInt("010", 10);
	> 10

!SLIDE
# Boolean
truthy + falsy

!SLIDE
# String

!SLIDE
# Array

!SLIDE
# RegExp

!SLIDE
# Functions

!SLIDE
# null

!SLIDE
# undefined

!SLIDE bullets
# Operators
*  +   -    *   /    %
* ==    !=   <    >    <= >=
* === !==
* && || !
* & | ^ >> >>> <<
* ?:

!SLIDE
# addition

!SLIDE
# division

!SLIDE
# type coercion

'' == '0'          // false
0 == ''            // true
0 == '0'           // true
false == 'false'   // false
false == '0'       // true
false == undefined // false
false == null      // false
null == undefined // true

!SLIDE
# &&

!SLIDE
# ||

!SLIDE smbullets
# Statements #
* if
* switch
* while
* do
* for
* break
* continue
* return
* try/throw

!SLIDE
# for in #

!SLIDE
# Inheritance

