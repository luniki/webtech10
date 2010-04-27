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

!SLIDE bullets
# Number

* single number type
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

!SLIDE bullets
# String

* UCS 2 (not UTF-16)
* immutable
* "foo" === "foo"
* 'bar' or "bar"

!SLIDE execute

	@@@ javaScript
	var num = 23;
	result = num.toString();

!SLIDE execute

# length Property #

	@@@ javaScript
	// wrong w/ surrogate pairs
	result = "23".length;

!SLIDE
# String methods

	@@@ javaScript
	charAt charCodeAt concat indexOf
	lastIndexOf localeCompare match
	replace search slice split substr
	substring toLowerCase toString
	toUpperCase valueOf

!SLIDE
# Boolean #
	@@@ javaScript
	true false

!SLIDE smbullets
# falsy #
* false
* null
* undefined
* "" (empty string)
* 0
* NaN

!SLIDE bullets
# truthy #
* everything else

!SLIDE bullets
# Variables #

!SLIDE
# new variables with var #

	@@@ javaScript
	var name = "hoge";

!SLIDE execute

	@@@ javaScript
	var a;
	result = a;

!SLIDE bullets
# undefined #
* primitive value used when a variable has not been assigned a value

!SLIDE bullets
# null #
* primitive value that represents the intentional absence of any object value.

!SLIDE
# Operators #

!SLIDE
# Arithmetic #
	+ - * / %

!SLIDE
# Comparison #
	=== !===
	== !=
	< > <= >=

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


!SLIDE
# Statements #

!SLIDE
	@@@ javaScript
	if (name == "foo") {
		//
	} else {
		//
	}

!SLIDE
	@@@ javaScript
	switch(1 + 3) {

		case 2 + 2:
			doIt();
			break;

		default:
			neverHappens();
	}

!SLIDE
	@@@ javaScript
	while (true) {
		neverEndingStory();
	}

!SLIDE
	@@@ javaScript
	do {
		matchHere(text);
	} while (text = text.substr(1));

!SLIDE
	@@@ javaScript
	for (i = 0; i < array.length; i += 1) {
		alert(array[i]);
	}

!SLIDE bullets
# Completion Specification Type #
* break
* continue
* return
* try/throw

!SLIDE
	@@@ javaScript
	for (name in object) {
		if (object.hasOwnProperty(name)) {
			doSomething(object[name]);
		}
	}




!SLIDE subsection
# Objects #

!SLIDE
# collection of dynamic properties #
# call by reference (sharing) #

!SLIDE
	@@@ javaScript
	// get
	object.name
	object[expression]

	// set
	object.name = value;
	object[expression] = value;

	// delete
	delete object.name
	delete object[expression]

!SLIDE
# Object literals #
	@@@ javaScript
	var foo = {bar: 23, baz: "hoge"};


!SLIDE
# Array

!SLIDE bullets
# Arrays
* are objects
* indexes are converted to strings
* good for sparse arrays
* otherwise bad performance
* pro: no dimension necessary

!SLIDE
# Array literals #

	@@@ javaScript
	var cities = ["Adrilankha", "Northport", "Candletown"];

!SLIDE execute
# special length property #

	@@@ javaScript
	var anArray = ["foo"];
	anArray[100] = "bar;
	result = anArray.length;

!SLIDE
# Appending elements #

	@@@ javaScript
	cities[cities.length] = "Fenario";

!SLIDE
# Iterating #

	@@@ javaScript
	for (var i = 0; i < cities.length; i++) {
		doIt(a[i]);
	}

!SLIDE
# Delete #

	@@@ javaScript

	// w/ holes
	delete array[number]

	// w/o holes
	array.splice(number, 1)

!SLIDE smbullets
# Array methods #

* a.toString()
* a.concat(item, ..), a.join(sep)
* a.pop(), a.push(item, ..)
* a.reverse(), a.sort(cmpfn)
* a.shift(), a.unshift([item]..)
* a.slice(start, end)
* a.splice(start, delcount, [item]..)

!SLIDE execute
# sort #

	@@@ javaScript
	result = [4, 8, 10].sort();


!SLIDE subsection
# Regular Expressions #

!SLIDE bullets
* straight from Perl
* regexp.exec, regexp.test
* string.match, string.replace
* string.search, string.split

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = /^(.*): (.*)$/.exec(header);

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = /^(.*): (.*)$/.test(header);

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = header.match(/^(.*): (.*)$/);

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = header.replace(/^(.*): (.*)$/, "$1=$2");

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = header.search(/: /);

!SLIDE execute
	@@@ javaScript
	var header = "Content-Type: text/html";
	result = header.split(/: /);


!SLIDE
# Functions

!SLIDE
# Inheritance

classes vs prototypes

working with prototypes
make an object you like
create new instances inheriting from that
customize new objects
classification not necessary

