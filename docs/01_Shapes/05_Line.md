To create a line with `KineticJS`, we can instantiate a `Kinetic.Line()` object.  For a full list of attributes and methods, check out the [Kinetic.Line documentation](http://kineticjs.com/docs/Kinetic.Line.html).

<iframe width="650" height="350" src="../Examples/Shapes/Line.html" frameborder="0" allowfullscreen></iframe>

```html
<!DOCTYPE HTML>
<html>
  <head>
    <style>
      body {
        margin: 0px;
        padding: 0px;
      }
    </style>
  </head>
  <body>
    <div id="container"></div>
    <script src="http://d3lp1msu2r81bx.cloudfront.net/kjs/js/lib/kinetic-v5.1.0.min.js"></script>
    <script defer="defer">
      var stage = new Kinetic.Stage({
        container: 'container',
        width: 600,
        height: 300
      });

      var layer = new Kinetic.Layer();

      var redLine = new Kinetic.Line({
        points: [73, 70, 340, 23, 450, 60, 500, 20],
        stroke: 'red',
        strokeWidth: 15,
        lineCap: 'round',
        lineJoin: 'round'
      });

      // dashed line
      var greenLine = new Kinetic.Line({
        points: [73, 70, 340, 23, 450, 60, 500, 20],
        stroke: 'green',
        strokeWidth: 2,
        lineJoin: 'round',
        /*
         * line segments with a length of 33px
         * with a gap of 10px
         */
        dash: [33, 10]
      });

      // complex dashed and dotted line
      var blueLine = new Kinetic.Line({
        points: [73, 70, 340, 23, 450, 60, 500, 20],
        stroke: 'blue',
        strokeWidth: 10,
        lineCap: 'round',
        lineJoin: 'round',
        /*
         * line segments with a length of 29px with a gap
         * of 20px followed by a line segment of 0.001px (a dot)
         * followed by a gap of 20px
         */
        dash: [29, 20, 0.001, 20]
      });

      /*
       * since each line has the same point array, we can
       * adjust the position of each one using the
       * move() method
       */
      redLine.move({
        x : 0,
        y : 5
      });
      greenLine.move({
        x : 0,
        y : 55
      });
      blueLine.move({
        x : 0,
        y : 105
      });

      layer.add(redLine);
      layer.add(greenLine);
      layer.add(blueLine);

      // add the layer to the stage
      stage.add(layer);
    </script>
  </body>
</html>

```