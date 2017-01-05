# dev-tools
Various dev tools collected from the internet or written by myself.

## C# Code Format
[Artistic Style](http://astyle.sourceforge.net/) is a source code indenter, formatter, and beautifier for the C, C++, C++/CLI, Objective‑C, C# and Java programming languages. We can download and install Astyle rather quickly without any problems on most platforms.

**Installation**

We will use a simple script below to help us install AStyle on Mac OSX. Installation on other platforms can be done in a similar manner

[setup_astyle.sh](../blob/master/astyle/setup_astyle.sh)

**Usage**

After we have `astyle` available on the command line, applying it for our project is a matter of wrapping everything in a single Make command like so

```
# Supposed our Code is in the Code folder
format:
	find Code -iname "*.cs" -not -path "Code/excludedpath/*" | xargs -n 1 -I {} bash -c "astyle --options=.astylerc \"{}\""
```

Remember to create a file called `.astylerc` and put whatever format options you want to customize for your project there.

## Log Parser
* [general-log-parser](https://pypi.python.org/pypi/general-log-parser)

## Simulate slow network with speedlimit
* [speedlimit](https://github.com/mschrag/speedlimit)

## Generate ASCII art
* `figlet`

## HTML5 sprite sheet generator
* Stitches http://draeton.github.io/stitches/
* [https://github.com/carrotsearch/smartsprites](https://github.com/carrotsearch/smartsprites)

## Pandoc a universal document converter
* http://pandoc.org/


## Image manipulation

### ImageMagic to resize images
```
	convert -quality 100 -resize 24x24 input.png output.png
```

### MULTICROP crops and unrotates multiple images

```
    multicrop [-c coords] [-b bcolor] [-f fuzzval] [-g grid] [-d discard] [-p prune] [-u unrotate] [-e extend] [-m mask] infile outfile
```

### Optimize images for the web
* [ImageOptim](https://github.com/ImageOptim/ImageOptim) is a GUI for lossless image optimization tools: PNGOUT, AdvPNG, Pngcrush, OptiPNG, JpegOptim, MozJPEG, jpegtran, and Gifsicle

## url shortener
* [Bit.ly](https://bitly.com/)
* [goo.gl](https://goo.gl/)

