## 5.1.9 2014-01-09
   * Bug Fixes
      * Correct stage resizing with `FastLayer`
      * `batchDraw` method for `FastLayer`
      * Correct mouseover/mouseout/mouseenter/mouseleave events for groups
      * cache node before adding to layer
      * `intersects` function now works for shapes with shadow
   * Enhancements
      * npm package. See https://github.com/ericdrowell/KineticJS#installation
      * much better dragging performance
      * `browserify` support
      * applying opacity to cached node
      * remove all events with `node.off()`
      * mouse dragging only with left button
      * opacity now affect cached shapes
      * Label corner radius
      * smart changing `width`, `height`, `radius` attrs for circle, start, ellipse, ring.
      * `mousewheel` support. Thanks [@vmichnowicz](https://github.com/vmichnowicz)
      * new Arrow plugin
      * multiple names: `node.name('foo bar'); container.find('.foo');` (thanks [@mattslocum](https://github.com/mattslocum))
      * `Container.findOne()` method. (thanks [@pronebird](https://github.com/pronebird))