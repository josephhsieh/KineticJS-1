To create an image with `KineticJS`, we can instantiate a `Kinetic.Image()` object.  For a full list of attributes and methods, check out the [Kinetic.Image documentation](http://kineticjs.com/docs/Kinetic.Image.html).

<iframe width="650" height="350" src="../Examples/Shapes/Image.html" frameborder="0" allowfullscreen></iframe>

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

      var imageObj = new Image();
      imageObj.onload = function() {

        var yoda = new Kinetic.Image({
          x: 140,
          y: stage.getHeight() / 2,
          image: imageObj,
          width: 106,
          height: 118
        });

        // add the shape to the layer
        layer.add(yoda);

        // add the layer to the stage
        stage.add(layer);
      };
      imageObj.src = '../../img/yoda.jpg';
    </script>
  </body>
</html>
```