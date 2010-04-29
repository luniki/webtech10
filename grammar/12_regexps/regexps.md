!SLIDE subsection
# Regular Expressions #

!SLIDE
# RegExp literals #

	var number = /^-?\d+$/i;

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

