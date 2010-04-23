!SLIDE subsection

# Grammar #

!SLIDE

# insignificant Whitespace #
	@@@ javaScript
	var that = this;

!SLIDE
# comments

	@@@ javaScript
	// ...

	/*
		...
	*/

!SLIDE
# Identifier Names

	@@@ javaScript
	/[a-zA-Z_$][a-zA-Z0-9_$]*/

	/*
		really unicode letters:
		[A-Za-z\u00C0-\u1FFF\u2800-\uFFFD]
	*/

!SLIDE code

# Reserved Words

	break     else        new     var
	case      finally     return  void
	catch     for         switch  while
	continue  function    this    with
	default   if          throw
	delete    in          try
	do        instanceof  typeof

!SLIDE code

# Future Reserved Words

	abstract 	enum       	int       	short
	boolean  	export     	interface 	static
	byte     	extends    	long      	super
	char     	final      	native    	synchronized
	class    	float      	package   	throws
	const    	goto       	private   	transient
	debugger 	implements 	protected 	volatile
	double   	import     	public


!SLIDE
# Objects

passed by reference not value


!SLIDE
# Number

!SLIDE
# Boolean
truthy + falsy

!SLIDE
# String

!SLIDE
# Array

!SLIDE
# RegExp

!SLIDE
# Functions

!SLIDE
# null

!SLIDE
# undefined

!SLIDE bullets
# Operators
*  +   -    *   /    %
* ==    !=   <    >    <= >=
* === !==
* && || !
• & | ^ >> >>> <<
* ?:

!SLIDE
# addition

!SLIDE
# division

!SLIDE
# type coercion

'' == '0'          // false
0 == ''            // true
0 == '0'           // true
false == 'false'   // false
false == '0'       // true
false == undefined // false
false == null      // false
null == undefined // true

!SLIDE
# &&

!SLIDE
# ||

!SLIDE smbullets
# Statements #
* if
* switch
* while
* do
* for
* break
* continue
* return
* try/throw

!SLIDE
# for in #

!SLIDE
# Inheritance

