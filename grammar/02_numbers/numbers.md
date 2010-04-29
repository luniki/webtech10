!SLIDE subsection
# Types

!SLIDE bullets
# Number

* single number type
* only 64 bit float (IEEE 754 double)
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

