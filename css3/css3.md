!SLIDE
# CSS Selectors

Selectors Level 3
Selectors API Level 2



!SLIDE Font-face
CSS Fonts Module Level 3

New font support

@font-face {
  font-family: 'Junction';
  src: url(Junction02.otf);
}
@font-face {
  font-family: 'LeagueGothic';
  src: url(LeagueGothic.otf);
}
@font-face {
  font-family: 'GG250';
  src: url(General250.otf);
}

header {
  font-family: 'LeagueGothic';
}


!SLIDE
CSS Transitions Module Level 3
CSS 2D Transforms Module Level 3
http://dev.opera.com/articles/view/css3-transitions-and-2d-transforms/#combining-transitions


!SLIDE
CSS Color Module Level 3

hsl(hue, saturation, lightness)
cmyk(cyan, magenta, yellow, black)
hsla(hue, saturation, lightness, alpha)
rgba(red, green, blue, alpha)

Unterschied opacity und rgba
background: rgb(255, 255, 255);
opacity: 0.5;

background: rgba(255, 255, 255, 0.5);
opacity: 1;


!SLIDE
CSS Backgrounds and Borders Module Level 3
http://dev.opera.com/articles/view/css3-border-background-boxshadow/

border-radius

shorthand for:
* border-top-left-radius
* border-bottom-left-radius
* border-top-right-radius
* border-bottom-right-radius

siehe Beispiel

multiple backgrounds
http://people.opera.com/zibin/multiple_background_image_zibin.html
The first image in the list is the layer closest to the user, the next one is
painted behind the first, and so on. The background color, if present, is
painted below all of the other layers.

