!SLIDE bullets
# Selectors Level 3#
* <http://www.w3.org/TR/css3-selectors/#selectors>

!SLIDE
# Type Selector CSS 1 #

    @@@ CSS
    body {…}

!SLIDE
# Attribute Selectors CSS 2 #

    @@@ CSS
    h1[title]

    span[class="example"]

    a[rel~="copyright"]

    a[hreflang|="en"]

!SLIDE
# Attribute Selectors CSS 3 #

    @@@ CSS
    E[foo^="bar"]

    E[foo$="bar"]

    E[foo*="bar"]

!SLIDE
# Structural pseudo-classes #

    @@@ CSS
    E:root
    E:empty

!SLIDE
# Structural pseudo-classes #

    @@@ CSS
    E:first-child
    E:last-child
    E:only-child
    E:nth-child(n)
    E:nth-last-child(n)

!SLIDE

    @@@ CSS
    tr:nth-child(2n+1)
    tr:nth-child(odd)

    tr:nth-child(2n+0)
    tr:nth-child(even)

!SLIDE

    @@@ CSS
    p:nth-child(4n+1) { color: navy; }
    p:nth-child(4n+2) { color: green; }
    p:nth-child(4n+3) { color: maroon; }
    p:nth-child(4n+4) { color: purple; }

!SLIDE
# Structural pseudo-classes #

    @@@ CSS
    E:first-of-type
    E:last-of-type
    E:only-of-type
    E:nth-of-type(n)
    E:nth-last-of-type(n)

!SLIDE
# Link pseudo-classes CSS 1#

    @@@ CSS
    E:link
    E:visited

!SLIDE
# User action pseudo-classes
## CSS 1+2

    @@@ CSS
    E:active
    E:hover
    E:focus

!SLIDE
# target pseudo-class #

    @@@ CSS
    E:target

!SLIDE
# UI element states pseudo-classes #

    @@@ CSS
    E:enabled
    E:disabled
    E:checked

!SLIDE
# Pseudo elements #

    @@@ CSS
    E::first-line
    E::first-letter
    E::before
    E::after

!SLIDE
# Class + ID selectors #

    @@@ CSS
    E.warning
    E#myid

!SLIDE
# Negation pseudo-class #

    @@@ CSS
    E:not(s)
    *:not(foo)
    input:not([type="submit"])

!SLIDE
# Combinators #

    @@@ CSS
    E F (Descendant)
    E > F (Child)
    E + F (Adjacent sibling)
    E ~ F (General sibling)

