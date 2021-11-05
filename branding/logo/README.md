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
