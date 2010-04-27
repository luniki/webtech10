!SLIDE subsection
# Objects #

!SLIDE bullets
# Objects... #
* are collection of dynamic properties
* are class-free
* inherit from objects

!SLIDE
# Object literals #
	@@@ javaScript
	var empty = {};

	var rascal = {
		"given-name": "Borrah",
		surname:      "Minnevitch"
	};

!SLIDE
	@@@ javaScript
	// get
	rascal.surname
	rascal["given-name"]

	// set
	rascal.surname = "Fields";
	rascal["given-name"] = "George";

	// delete
	delete rascal.surname;
	delete rascal["given-name"];

!SLIDE bullets
# Prototype #
* Every object is linked to a prototype object from which it inherits properties.
* Object literals inherit from Object.prototype
* You can make new objects inheriting from other prototypes.

!SLIDE
# Object.create #

	@@@ javaScript
	Object.create = function (o) {
		var F = function () {};
		F.prototype = o;
		return new F();
	};

!SLIDE execute

	@@@ javaScript
	var rascal = {
		"given-name": "Borrah",
		surname: "Minnevitch"
	};

	var anotherRascal = Object.create(rascal);
	result = anotherRascal.surname;

!SLIDE execute
	@@@ javaScript
	// updates do not touch prototypes
	// prototypes only used for retrieval
	var anotherRascal = Object.create(rascal);

	anotherRascal["given-name"] = "George";

	result = rascal["given-name"]
	         + " and " +
	         anotherRascal["given-name"];

!SLIDE smbullets
* retrieving a property starts with the object
* \<repeat> not found? → search in the prototype object \</repeat>
* finally ends in Object.prototype
* still not found: undefined
* → *delegating inheritance based on prototypes*

!SLIDE bullets
# Reflection #
* typeof operator
* anotherRascal.hasOwnProperty("surname")

