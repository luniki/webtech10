!SLIDE subsection
# Functions #

!SLIDE
# Function expression #
## produces a function object ##

	@@@ javaScript
	var add = function (x, y) {
		var sum = x + y;
		return sum;
	};

!SLIDE smbullets
# First class objects #
* may be passed as argument to a function
* may be returned from a function
* may be assigned to a variable or property
* may have methods
* can be invoked

!SLIDE bullets
# var statement#
* declares local variables in functions
* variables declared in a function are visible everywhere in this function
* If you forget the var, you get a global variable.
* Global variables are evil.

!SLIDE
# Function statement #

	@@@ javaScript
	function add(x, y) {...}

	// (almost) the same as
	var add = function (x, y) {...};

!SLIDE bullets
# Scope #
* function scope (no block scope)
* variables defined in a function are not visible outside of it

!SLIDE
	@@@ javaScript
	function foo() {
		var bar = 23;
	}

	foo();

	result = window.bar === undefined;

!SLIDE
# return statement #

	@@@ javaScript
	// returns expression
	return expression;

	// returns undefined
	return;

	// w/o return statement: undefined

!SLIDE bullets execute
# arguments #
## more like... guidelines ##
## missing parameters are undefined ##
## more arguments are ignored: ##
	@@@ javaScript
	var add = function (x, y) { return x + y; }

	result = add(2, 3, 4)

!SLIDE bullets execute
# Pseudo parameter: arguments #

	@@@ javaScript
	var add = function () {
		var sum = 0, i;
		for (i = 0; i < arguments.length; i += 1) {
			sum += arguments[i];
		}
		return sum;
	}

	result = add(2, 3, 4, 5);

!SLIDE bullets
# Pseudo parameter: this #
* *this* contains reference to object of invocation
* value determined by invocation pattern

!SLIDE bullets
# Invocation Patterns #
* Function form: func(arg)
* Method form: rascal.func(arg)
* Constructor form: new Func(arg)
* Apply form: func.apply(arg)

!SLIDE execute
# Function form #
## *this* is bound to the global object ##

	@@@ javaScript
	var func = function () { return this; };
	result = func();

!SLIDE execute
# Method form #
## *this* is bound to the object to which the message was sent ##

	@@@ javaScript
	rascal.func = function () { return this; };
	result = rascal.func();

!SLIDE bullets
# Constructor form #
* JS is a prototypal oo language
* syntax from a classical oo language
* → confusion

!SLIDE bullets
* invoking a function with *new* will create a new object
* *func.prototype* linked as the new object's prototype
* *this* is bound to the new object

!SLIDE execute
	@@@ javaScript
	var Rascal = function (given_name, surname) {
		this["given-name"] = given_name;
		this.surname = surname;
	};
	Rascal.prototype.fullName = function () {
		return this["given-name"] + " " + this.surname;
	};

	var rascal = new Rascal("Borrah", "Minnevitch");

	result = rascal.fullName();

!SLIDE execute
# Apply form #
## this is bound to first argument ##

	@@@ javaScript
	var func = function () { return this; };

	result = func.apply(rascal, ["more", "arguments"])

