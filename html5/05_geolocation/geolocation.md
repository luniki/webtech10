!SLIDE bullets
# Geolocation
## Geolocation Working Group
* <http://www.w3.org/TR/geolocation-API/>

!SLIDE bullets
* Beispiel:
* <http://diveintohtml5.org/detect.html#geolocation>

!SLIDE bullets
* IP-Adresse
* WLAN-Netzwerk
* Mobilfunkmast
* GPS

!SLIDE smaller
    @@@ javascript
    function supports_geolocation() {
      return !!navigator.geolocation;
    }

    function showMap(pos) {
      // Show a map centered at
      // pos.coords.latitude
      // pos.coords.longitude
    }

    // One-shot position request
    navigator.geolocation
             .getCurrentPosition(showMap);

!SLIDE
    @@@ javascript
    coords.latitude
    coords.longitude
    coords.altitude
    coords.accuracy
    coords.heading
    coords.speed

