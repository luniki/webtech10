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

