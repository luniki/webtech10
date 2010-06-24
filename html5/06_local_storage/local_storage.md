!SLIDE bullets
# Web storage
* <http://www.w3.org/TR/webstorage/>

!SLIDE bullets
# Cookies …
* mit jedem Request
* unverschlüsselt
* max. 4Kb

!SLIDE bullets
# Web storage …
* mehr Platz
* im Browser, nicht im Request
* persistent

!SLIDE smaller
    @@@ javascript
    function supports_html5_storage() {
      return ('localStorage' in window)
        && window['localStorage'] !== null;
    }

    localStorage.getItem("foo")
    localStorage["foo"]

    localStorage.setItem("bar", baz)
    localStorage["bar"] = baz

