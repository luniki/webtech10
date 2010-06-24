!SLIDE
# Canvas #

<canvas id="canvas" width="400" height="400"></canvas>
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

!SLIDE tiny
    @@@ HTML
    <canvas id="canvas" width="400" height="400">
    </canvas>
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
# [Beispiel](http://diveintohtml5.org/examples/canvas-halma.html)
