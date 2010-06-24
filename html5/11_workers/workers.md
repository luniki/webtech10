!SLIDE bullets
# Web Workers
* <http://www.w3.org/TR/workers/>

!SLIDE smaller
    @@@ javascript
    // worker.html
    var worker = new Worker('worker.js');
    worker.onmessage = function (event) {
      var result = document.getElementById('result');
      result.textContent = event.data;
    };

!SLIDE smaller
    @@@ javascript
    // worker.js
    var n = 1;
    search: while (true) {
      n += 1;
      for (var i = 2; i <= Math.sqrt(n); i += 1)
        if (n % i == 0)
         continue search;
      // found a prime!
      postMessage(n);
    }

!SLIDE
# → [Beispiel](http://coll.virtuos.uos.de/webtech10/examples/workers/)
## (Opera)

