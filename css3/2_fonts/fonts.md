!SLIDE bullets
# CSS Fonts Module Level 3
* <http://www.w3.org/TR/css3-fonts/>

!SLIDE smaller
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

!SLIDE smbullets
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

!SLIDE smbullets
# Services #
* http://code.google.com/webfonts
* http://typekit.com/
* http://www.typotheque.com
* http://www.fontslive.com/
* http://kernest.com/

