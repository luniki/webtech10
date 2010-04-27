!SLIDE subsection
# Closures #

!SLIDE bullets
* You can define functions in functions.
* context of inner functions includes the scope of their outer functions
* even for inner functions living longer than their outer functions

!SLIDE execute
# Global #
	@@@ javaScript
	var rot13 = {a: "m", b: "n", c: "o" /*, … */ };

	var encode = function (char) {
		return rot13[char];
	};

	result = encode("b");

!SLIDE execute
# Local #
	@@@ javaScript
	var encode = function (char) {
		var rot13 = {a: "m", b: "n", c: "o" /*, … */};

		return rot13[char];
	};

	result = encode("b");

!SLIDE execute
# Closure #
	@@@ javaScript
	var encode = (function () {

		var rot13 = {a: "m", b: "n", c: "o" /*, … */};

		return function (char) {
			return rot13[char];
		};

	}());

	result = encode("b");

