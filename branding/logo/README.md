# Scientific Python logo

## How to generate favicon.ico

1. Convert SVG to png:

```
inkscape --export-type=png scientific-python-logo.svg
```

2. Convert png to multi-resolution icon:

```
convert scientific-python-logo.png -define icon:auto-resize=64,48,32,16 -colors 3 favicon.ico
```

## To simplify SVGs for making icons

See the [SimpleIcons guidelines](https://github.com/simple-icons/simple-icons/blob/develop/CONTRIBUTING.md#adding-or-updating-an-icon):

1. Isolate the icon from any text or extraneous items.
2. Merge any overlapping paths.
3. Compound all paths into one.
4. Change the icon's viewbox/canvas/page size to 24x24.
5. Scale the icon to fit the viewbox, while preserving the icon's original proportions. This means the icon should be touching at least two sides of the viewbox.
6. Center the icon horizontally and vertically.
7. Remove all colors. The icon should be monochromatic.
8. Export the icon as an SVG.

They use [SVGO](https://github.com/svg/svgo) to optimize SVGs.  You can also use scour: `pip install scour`.

```
scour --set-precision=2 --strip-xml-prolog --remove-metadata --enable-comment-stripping --enable-viewboxing --indent=none --no-line-breaks --strip-xml-space --shorten-ids --enable-id-stripping scientific-python.svg scientific-python-icon.svg
```
