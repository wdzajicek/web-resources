# SVG Graphics and Screen Readers

If and SVG Graphic contains meaningful information—user's with screen readers and assistive technologies need to be able to know what this information is.

Traditionally, we would use an image tag with an alt attribute for graphics that add meaning to the content (e.g. `<img alt="Description of image's meaningful content">`.) This works perfectly if we are using an `<img>` tag to house our SVG graphic.

However, what if we want to use an inline SVG, where the SVG tag and code appear directly in our HTMl markup?  We cannot use the `alt=""` attribute on an SVG tag—this would not be valid markup.  How do we get around this issue...?

## The SVG `<title>` Tag

>The <title> element provides an accessible, short-text description of any SVG container element or graphics element.
>
>Text in a <title> element is not rendered as part of the graphic, but browsers usually display it as a tooltip. If an element can be described by visible text, it is recommended to reference that text with an aria-labelledby attribute rather than using the <title> element.
>
> - MDN web docs, "`<title>` — the SVG accessible name element" | <https://developer.mozilla.org/en-US/docs/Web/SVG/Element/title>

To use a title tag you need the following:

1. A `<title></title>` tag containing the descriptive text for the SVG
2. Give the title an `id=""` attribute
3. Give the title a `lang=""` attribute (`en` for english)
4. Add an `aria-labeledby` attribute—the value should be the same as the value in the `<title>`'s _id_

```html
<svg version="1.1" id="svgId" ...OTHER ATTRIBUTES REMOVED... aria-labelledby="svgTitleId">
  <title  id="svgTitleId" lang="en">Accessible short description of the graphic</title>
  <!-- More SVG code -->
</svg>
```
