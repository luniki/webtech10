!SLIDE
# Functions #

!SLIDE
# Function expression #
## produces a function object ##

	@@@ javaScript
	var add = function (x, y) {
		var sum = x + y;
		return sum;
	};

!SLIDE bullets
# First class objects #
* may be passed as argument to a function
* may be returned from a function
* may be assigned to a variable
* may be stored in objects or arrays

!SLIDE bullets
# var #
* declares local variables in functions
* variables declared in a function are visible everywhere in this function
* If you forget the var, you get a global variable.
* Global variables are evil.

!SLIDE
# Function statement #

	@@@ javaScript
	function add(x, y) {...}

	// (almost) the same as
	var add = function (x, y) {...}

!SLIDE bullets
# Scope #
* function scope (not block scope)
* variables defined in a function are not visible outside of it

!SLIDE

	@@@ javaScript
	function foo() {
		var bar = 23;
	}

	foo();

	result = window.bar === undefined;

!SLIDE
# return #

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
	function add(x, y) { return x + y; }

	result = add(2, 3, 4)

!SLIDE bullets execute
# Pseudo parameter: arguments #

	@@@ javaScript
	function add() {
		var sum = 0;
		for (var i = 0; i < arguments.length; i++) {
			sum += arguments[i];
		}
		return sum;
	}

	result = add(2, 3, 4, 5);

!SLIDE
Constructor




!SLIDE
# Pseudo parameter: this #
• The this parameter contains a reference
  to the object of invocation.
• this allows a method to know what object
  it is concerned with.
• this allows a single function object to
  service many functions.
• this is key to prototypal inheritance.

                   Invocation
• There are four ways to call a function:
  • Function form
     • functionObject(arguments)
  • Method form
     • thisObject.methodName(arguments)
     • thisObject["methodName"](arguments)
  • Constructor form
     • new FunctionObject(arguments)
  • Apply form
     • functionObject.apply(thisObject,[arguments])

               Method form
       thisObject.methodName(arguments)
      thisObject[methodName](arguments)
• When a function is called in the method
  form, this is set to thisObject, the object
  containing the function.
• This allows methods to have a reference to
  the object of interest.
               Function form
          functionObject(arguments)
• When a function is called in the function
  form, this is set to the global object.
   • That is not very useful. (Fixed in ES5/Strict)
   • An inner function does not get access to the
     outer this.
              var that = this;
            Constructor form
       new FunctionValue(arguments)
• When a function is called with the new
  operator, a new object is created and
  assigned to this.
• If there is not an explicit return value, then
  this will be returned.
• Used in the Pseudoclassical style.
                   Apply form
  functionObject.apply(thisObject, arguments)
  functionObject.call(thisObject, argument)
• A function’s apply or call method allows for
  calling the function, explicitly specifying
  thisObject.
• It can also take an array of parameters or a
  sequence of parameters.
   Function.prototype.call = function (thisObject) {
       return this.apply(thisObject, Array
            .prototype.slice.apply(arguments, [1]));
   };

CLOSURE

