!SLIDE subsection
# Closures #

!SLIDE bullets
* You can define functions in functions.
* Inner functions can access params + variables of their outer functions.
* Even true for inner functions living longer than their outer functions.

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

