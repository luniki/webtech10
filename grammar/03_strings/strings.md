!SLIDE bullets
# String

* UCS 2 (not UTF-16)
* immutable
* "foo" === 'foo'

!SLIDE execute

	@@@ javaScript
	var num = 23;
	result = num.toString();

!SLIDE execute

# length Property #

	@@@ javaScript
	// but: wrong w/ surrogate pairs
	result = "23".length;

!SLIDE
# String methods

	@@@ javaScript
	charAt charCodeAt concat indexOf
	lastIndexOf localeCompare match
	replace search slice split substr
	substring toLowerCase toString
	toUpperCase valueOf

