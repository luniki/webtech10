
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
