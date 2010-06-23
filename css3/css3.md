!SLIDE subsection
# CSS3 #


!SLIDE
# Selectors Level 3#
.link http://www.w3.org/TR/css3-selectors/#selectors

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
# User action pseudo-classes CSS 1+2#

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


!SLIDE TODO link-klasse-klar-machen
# CSS Fonts Module Level 3 #
.link http://www.w3.org/TR/css3-fonts/

!SLIDE
# Font-Beispiel #

    @@@ CSS
    @font-face {
      font-family: 'LeagueGothic';
      src: url(LeagueGothic.otf);
    }

    h1 {
      font-family: 'LeagueGothic',
                   sans-serif;
    }

!SLIDE bullets
# Cross-Browser-Probleme #
* IE: EOT
* FF: OTF, TTF
* Safari, Opera: OTF, TTF, SVG
* Chrome: TTF, SVG

!SLIDE tiny

    @@@ CSS
    @font-face {
      font-family: 'DroidSansRegular';
      src: url('droidsans-webfont.eot');
      src: local('☺'),
           url('droidsans-webfont.woff')
              format('woff'),
           url('droidsans-webfont.ttf')
              format('truetype'),
           url('droidsans-webfont.svg#webfontEvqmy5gf')
              format('svg');
      font-weight: normal;
      font-style: normal;
    }

!SLIDE bullets
# @font-face Generator #
* http://www.fontsquirrel.com/fontface/generator

!SLIDE
# Lizenz? #

!SLIDE bullets
# Services #
* http://code.google.com/webfonts
* http://typekit.com/
* http://www.typotheque.com
* http://www.fontslive.com/
* http://kernest.com/

!SLIDE TODO fehlt-noch
CSS Transitions Module Level 3
CSS 2D Transforms Module Level 3
http://dev.opera.com/articles/view/css3-transitions-and-2d-transforms/#combining-transitions


!SLIDE
# CSS Color Module Level 3 #

!SLIDE
* hsl(hue, saturation, lightness)
* cmyk(cyan, magenta, yellow, black)
* hsla(hue, saturation, lightness, alpha)
* rgba(red, green, blue, alpha)

!SLIDE TODO link-fehlt-noch
# Unterschied opacity und rgba #
.link TODO

!SLIDE
# CSS Backgrounds and Borders Module Level 3 #

!SLIDE
border-radius

shorthand for:
* border-top-left-radius
* border-bottom-left-radius
* border-top-right-radius
* border-bottom-right-radius

siehe Beispiel

!SLIDE
multiple backgrounds
http://people.opera.com/zibin/multiple_background_image_zibin.html
The first image in the list is the layer closest to the user, the next one is
painted behind the first, and so on. The background color, if present, is
painted below all of the other layers.

