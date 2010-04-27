!SLIDE
# Array

!SLIDE bullets
# Arrays
* are objects
* indexes are converted to strings
* good for sparse arrays
* otherwise bad performance
* pro: no dimension necessary

!SLIDE
# Array literals #

	@@@ javaScript
	var cities = ["Adrilankha", "Northport", "Candletown"];

!SLIDE execute
# special length property #

	@@@ javaScript
	var anArray = ["foo"];
	anArray[100] = "bar;
	result = anArray.length;

!SLIDE
# Appending elements #

	@@@ javaScript
	cities[cities.length] = "Fenario";

!SLIDE
# Iterating #

	@@@ javaScript
	for (var i = 0; i < cities.length; i++) {
		doIt(a[i]);
	}

!SLIDE
# Delete #

	@@@ javaScript

	// w/ holes
	delete array[number]

	// w/o holes
	array.splice(number, 1)

!SLIDE smbullets
# Array methods #

* a.toString()
* a.concat(item, ..), a.join(sep)
* a.pop(), a.push(item, ..)
* a.reverse(), a.sort(cmpfn)
* a.shift(), a.unshift([item]..)
* a.slice(start, end)
* a.splice(start, delcount, [item]..)

!SLIDE execute
# sort #

	@@@ javaScript
	result = [4, 8, 10].sort();

