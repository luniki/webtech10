!SLIDE subsection
# Closures #

!SLIDE bullets
* You can define functions in functions.
* Inner functions can access params + variables of their outer functions.
* Even true for inner functions living longer than their outer functions.

!SLIDE execute
	@@@ javaScript
	var quo = function (status) {
		return {
			get_status: function () {
				return status;
			}
		};
	};

	var myQuo = quo("amazed");
	result = myQuo.get_status();

<br>
<br>
>	from "JS: The Good Parts"

