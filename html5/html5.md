!SLIDE
HTML5 ~= HTML  + CSS  + JS APIs


Implementations and specifications have to do a delicate dance together. You
don't want implementations to happen before the specification is finished,
because people start depending on the details of implementations and that
constrains the specification. However, you also don't want the specification to
be finished before there are implementations and author experience with those
implementations, because you need the feedback. There is unavoidable tension
here, but we just have to muddle on through.

ein Mozilla-Entwickler auf public-html@w3.org

* History

HTML 1997 - 2004

1997
  HTML 4.0
  Auflösen der HTML Working Group
1998
  - XML 1.0
  - Workshop "Shaping the Future of HTML": "Has W3C given up on HTML?"

  In discussions, it was agreed that further extending HTML 4.0 would be
  difficult, as would converting 4.0 to be an XML application. The proposed way
  to break free of these restrictions is to make a fresh start with the next
  generation of HTML based upon a suite of XML tag-sets.

  - Reformulating HTML in XML → XHTML 1.0 (mit Schlupfloch "text/html" anstatt "application/xhtml+xml")
1999
  - XHTML Extended Forms → XForms Working Group

2001
  - XHTML 1.1 (ohne "Anhang C"-Schlupfloch, also verpflichtender MIME-Type und damit mit "Draconian Error Handling":
    "well-formedness errors be treated as fatal errors"

2004
  - W3C Workshop on Web Applications and Compound Documents
  - Präsentation der Vision von Mozilla und Opera:
    - rückwärtskompatibel, vernünftige Fehlerbehandlung, praktischer Nutzen, offener Entwicklungsprozess
  - "Should the W3C develop declarative extension to HTML and CSS and imperative
     extensions to DOM, to address medium level Web Application requirements, as
     opposed to sophisticated, fully-fledged OS-level APIs? (proposed by Ian
     Hickson, Opera Software)"
  - 11 to 8
  - "At present, W3C does not intend to put any resources into the third
     straw-poll topic: extensions to HTML and CSS for Web Applications, other
     than technologies being developed under the charter of current W3C Working
     Groups."
  - WHAT Working Group (Web Hypertext Application Technology)

    "The Web Hypertext Applications Technology Working Group is a loose,
    unofficial, and open collaboration of Web browser manufacturers and
    interested parties. The group aims to develop specifications based on HTML
    and related technologies to ease the deployment of interoperable Web
    Applications, with the intention of submitting the results to a standards
    organisation. This submission would then form the basis of work on formally
    extending HTML in the standards track."

2006
  - Tim Berners-Lee: "Reinventing HTML" Zusammenarbeit W3C und WHAT WG
  - HTML5

2007
  - 5. W3C HTML Working Group

2008
  - erster W3C Working Draft HTML5

2009
  - Auflösung XHTML 2 Working Group





* HTML 5 in 5 seconds:
http://www.w3.org/TR/html5/syntax.html#the-doctype

  <!DOCTYPE html>


* neue semantische Elemente

<section> thematische Gruppierung von Inhalt typischerweise mit Überschrift: Kapitel, tabbed pages
<nav> Navigationslinks
<article> eigenständige Komponente in einer Seite, die auch unabhängig vom Rest verbreited werden kann (Newsfeeds..): Forumsbeitrag, Zeitungsartikel, Blogeintrag, Kommentar
<aside> Teil einer Seite, der nur geringen Bezug zum Rest der Seite hat. In gedruckten Werken häufig als Seitenleiste abgesetzt.
<hgroup> Gruppierung von mehreren Überschriften (<h1>-<h6>)
<header> enthält Sachen wie Überschrift einer <section>, Einleitungen, Navigationshilfen, Suchformulare, Logos
<footer> enthält Autor einer <section>, Links, Copyright usw.
<time> repräsentiert eine Zeitangabe
<mark> ein Stück Text, der wie mit einem Textmarker angestrichen wurde

Achtung: Internet Explorer (< 9) erlauben kein CSS für diese Elemente. Mit JS gibt es aber einen Trick:

<style> mark { background: #ffff88; } </style>
<script>document.createElement("mark");</script>
<p>
  Far far away, <mark>behind the word mountains</mark>, far from the countries
  Vokalia and Consonantia, there live the blind texts.
</p>


http://diveintohtml5.org/examples/blog-original.html
http://diveintohtml5.org/examples/blog-html5.html


* Beispiel: Canvas
<canvas id="canvas" width="400" height="400"></canvas>
<script>
  var canvasContext = document.getElementById("canvas").getContext("2d");
  canvasContext.fillStyle = 'orange';
  canvasContext.fillRect(10, 10, 200, 200);

  canvasContext.fillStyle = "rgba(0, 127, 127, 0.5)";

  canvasContext.beginPath();
  canvasContext.arc(200, 200, 150, 0, Math.PI * 2, true);
  canvasContext.closePath();
  canvasContext.fill();
</script>

Kurzes Minibeispiel
http://diveintohtml5.org/examples/canvas-halma.html

* Video/Audio

  <video src="pr6.webm"></video>
  <video src="pr6.webm" width="320" height="240"></video>
  <video src="pr6.webm" width="320" height="240" controls></video>

Video Containers
  - Ogg .ogv
  - MPEG4  .mp4
  - WebM .webm

  - IE: -
  - FF: Ogg
  - Safari: MPEG4
  - Chrome: Ogg, MPEG4
  - Opera: Ogg, WebM
  - Iphone: MPEG4
  - Android: MPEG4

Video for Everybody

http://camendesign.com/code/video_for_everybody

<audio>




* Geolocation (Geolocation Working Group)
http://www.w3.org/TR/geolocation-API/

your IP address,
your wireless network connection,
which cell tower your phone is talking to,
or dedicated GPS hardware

FF 3.5, Safari 5, Chrome 5, Opera 10.60

function supports_geolocation() {
  return !!navigator.geolocation;
}

function showMap(position) {
  // Show a map centered at (position.coords.latitude, position.coords.longitude).
}

// One-shot position request.
navigator.geolocation.getCurrentPosition(showMap);

http://diveintohtml5.org/detect.html#geolocation

coords.latitude
coords.longitude
coords.altitude
coords.accuracy
coords.heading
coords.speed



* "local storage"


Cookies werden mit jedem Request unverschlüsselt versendet und sind höchstens 4Kb groß.

* mehr Platz
* im Browser, nicht im Request
* persistent

IE 8, FF 3.5, Safari 4, Chrome 4, Opera 10.50

function supports_html5_storage() {
  return ('localStorage' in window) && window['localStorage'] !== null;
}

localStorage.getItem("foo")
localStorage["foo"]

localStorage.setItem("bar", baz)
localStorage["bar"] = baz


* "offline web applications"

FF, Safari, Chrome, Opera

<!DOCTYPE html>
<html lang="en" manifest="halma.manifest">

CACHE MANIFEST
halma.html
../halma-localstorage.js

text/cache-manifest .manifest

* Forms

Neue Input-Types:

search, tel, url,
email, datetime, date,
month, week, time,
datetime-local, number,
range, color, usw.

Neue Input-Attribute:

autofocus, placeholder, max, min, required, usw.

* Drag and drop
http://www.w3.org/TR/html5/editing.html#dnd


* Cross-document messaging http://dev.w3.org/html5/postmsg/
* WebSocket http://www.w3.org/TR/websockets/

* Workers
Web Workers http://www.w3.org/TR/workers/

