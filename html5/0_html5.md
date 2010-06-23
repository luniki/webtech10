!SLIDE subsection
# Html 5 #

!SLIDE
Implementations and specifications have to do a delicate dance together. You
don't want implementations to happen before the specification is finished,
because people start depending on the details of implementations and that
constrains the specification. However, you also don't want the specification to
be finished before there are implementations and author experience with those
implementations, because you need the feedback. There is unavoidable tension
here, but we just have to muddle on through.

ein Mozilla-Entwickler auf public-html@w3.org

!SLIDE
# Html 5 in 5 seconds #
.link http://www.w3.org/TR/html5/syntax.html#the-doctype

    <!DOCTYPE html>

!SLIDE
# Neue semantische Elemente #

!SLIDE
    <section>
### thematische Gruppierung von Inhalt typischerweise mit Überschrift: Kapitel, tabbed pages ###
!SLIDE
    <nav>
### Navigationslinks ###
!SLIDE
    <article>
### eigenständige Komponente in einer Seite, die auch unabhängig vom Rest verbreited werden kann (Newsfeeds…): Forumsbeitrag, Zeitungsartikel, Blogeintrag, Kommentar
!SLIDE
    <aside>
### Teil einer Seite, der nur geringen Bezug zum Rest der Seite hat. In gedruckten Werken häufig als Seitenleiste abgesetzt.
!SLIDE
    <hgroup>
### Gruppierung von mehreren Überschriften (&lt;h1>-&lt;h6>)
!SLIDE
    <header>
### enthält Sachen wie Überschrift einer &lt;section>, Einleitungen, Navigationshilfen, Suchformulare, Logos
!SLIDE
    <footer>
### enthält Autor einer &lt;section>, Links, Copyright usw.
!SLIDE
    <time>
### repräsentiert eine Zeitangabe
!SLIDE
    <mark>
### ein Stück Text, mit Textmarker angestrichen

!SLIDE TODO
Bild

!SLIDE smaller
# Internet Explorer Blues #
### Internet Explorer (&lt; 9) erlaubt kein CSS für diese Elemente, aber:

    @@@ HTML
    <style>
      mark { background: #ffff88; }
    </style>
    <script>
      document.createElement("mark");
    </script>
    <p>
      Far far away, behind the
      <mark>word mountains</mark>
    </p>
<hr>
#### Far far away, behind the <mark>word mountains</mark>

!SLIDE TODO lieber-ein-bild
http://diveintohtml5.org/examples/blog-original.html
http://diveintohtml5.org/examples/blog-html5.html


!SLIDE
# Canvas #

<canvas id="canvas" width="400" height="400"></canvas>
<script>
var ctx = document.getElementById("canvas").getContext("2d");
ctx.fillStyle = 'orange';
ctx.fillRect(10, 10, 200, 200);

ctx.fillStyle = "rgba(0, 127, 127, 0.5)";

ctx.beginPath();
ctx.arc(200, 200, 150, 0, Math.PI * 2, true);
ctx.closePath();
ctx.fill();
</script>

!SLIDE tiny
    @@@ HTML
    <canvas id="canvas" width="400"
            height="400"></canvas>
    <script>
    var canvas = document.getElementById("canvas"),
        ctx = canvas.getContext("2d");

    ctx.fillStyle = 'orange';
    ctx.fillRect(10, 10, 200, 200);

    ctx.fillStyle = "rgba(0, 127, 127, 0.5)";

    ctx.beginPath();
    ctx.arc(200, 200, 150, 0, Math.PI * 2, true);
    ctx.closePath();
    ctx.fill();
    </script>

!SLIDE
Kurzes Minibeispiel
http://diveintohtml5.org/examples/canvas-halma.html

!SLIDE
* Video/Audio

  &lt;video src="pr6.webm"></video>
  &lt;video src="pr6.webm" width="320" height="240"></video>
  &lt;video src="pr6.webm" width="320" height="240" controls></video>

!SLIDE
Video Containers
  - Ogg .ogv
  - MPEG4  .mp4
  - WebM .webm

!SLIDE
  - IE: -
  - FF: Ogg
  - Safari: MPEG4
  - Chrome: Ogg, MPEG4
  - Opera: Ogg, WebM
  - Iphone: MPEG4
  - Android: MPEG4

!SLIDE
Video for Everybody
http://camendesign.com/code/video_for_everybody

!SLIDE
<audio>


!SLIDE
Geolocation (Geolocation Working Group)
http://www.w3.org/TR/geolocation-API/

!SLIDE
your IP address,
your wireless network connection,
which cell tower your phone is talking to,
or dedicated GPS hardware

!SLIDE
FF 3.5, Safari 5, Chrome 5, Opera 10.60

!SLIDE
function supports_geolocation() {
  return !!navigator.geolocation;
}

function showMap(position) {
  // Show a map centered at (position.coords.latitude, position.coords.longitude).
}

// One-shot position request.
navigator.geolocation.getCurrentPosition(showMap);

!SLIDE
coords.latitude
coords.longitude
coords.altitude
coords.accuracy
coords.heading
coords.speed

!SLIDE
http://diveintohtml5.org/detect.html#geolocation



!SLIDE
* "local storage"


!SLIDE
Cookies werden mit jedem Request unverschlüsselt versendet und sind höchstens 4Kb groß.

!SLIDE
* mehr Platz
* im Browser, nicht im Request
* persistent

!SLIDE
IE 8, FF 3.5, Safari 4, Chrome 4, Opera 10.50

!SLIDE
function supports_html5_storage() {
  return ('localStorage' in window) && window['localStorage'] !== null;
}

localStorage.getItem("foo")
localStorage["foo"]

localStorage.setItem("bar", baz)
localStorage["bar"] = baz


!SLIDE
* "offline web applications"

!SLIDE
FF, Safari, Chrome, Opera

!SLIDE
<!DOCTYPE html>
<html lang="en" manifest="halma.manifest">

!SLIDE
CACHE MANIFEST
halma.html
../halma-localstorage.js

!SLIDE
AddType text/cache-manifest .manifest

!SLIDE
* Forms

!SLIDE
Neue Input-Types:

search, tel, url,
email, datetime, date,
month, week, time,
datetime-local, number,
range, color, usw.

!SLIDE
Neue Input-Attribute:

autofocus, placeholder, max, min, required, usw.


!SLIDE
* Drag and drop
http://www.w3.org/TR/html5/editing.html#dnd
.link zur demo

!SLIDE TODO
* Cross-document messaging http://dev.w3.org/html5/postmsg/

!SLIDE TODO
* Workers
Web Workers http://www.w3.org/TR/workers/

