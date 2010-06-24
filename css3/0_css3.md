!SLIDE subsection
# CSS3 #



!SLIDE bullets
# CSS Fonts Module Level 3
* <http://www.w3.org/TR/css3-fonts/>

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

