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

