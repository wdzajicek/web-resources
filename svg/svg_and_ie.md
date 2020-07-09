# SVG Graphics in Internet Explorer

> Internet explorer version 11 and up (not tested in IE 10)

## Avoid distorting SVG proportions

When using an SVG in Internet Explorer—**especially an inline**-SVG—you may notice the height of the graphic being distorted (i.e. squished or stretched.)

Almost always, this is caused by not having a CSS `height: <height-value>;` explicitly set on the SVG's outermost (i.e. `<svg>`) tag.

_**The easiest fix for this is to set the following CSS rules via a class on the `<svg>` tag itself:**_

```css
.my-class {
  height: auto;
}
```
