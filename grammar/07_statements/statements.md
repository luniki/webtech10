!SLIDE subsection
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

