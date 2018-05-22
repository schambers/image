# Exercise #19: Building Images

[![exercise status: in progress](https://img.shields.io/badge/exercise%20status-in%20progress-yellow.svg?style=for-the-badge)](https://gophercises.com/exercises/transform)

## Exercise details

The basic idea of this exercise is to learn to create images using Go. To do this, we will explore a couple different packages as well as a few different image formats.

### PNG images, pixel by pixel

First up we are going to use the [image](https://golang.org/pkg/image/) package in the standard library to create pretty much any image you want. I will be creating some bar charts using a data slice of integers between 0 and 100, like the one below:

```go
data := []int{10, 33, 73, 64}
```

### PNG images with the draw package

Go also provides us with an [image/draw](https://golang.org/pkg/image/draw/) package that can be used for quite a bit. Try using it to recreated some of the images you made in the past exercise step.

### SVG images with svgo

SVGs have some pretty awesome advantages over PNGs. For starters, we can stop thinking about pixels and start working with things like rectangles, lines, text, etc. We can also create images that scale infinitely without losing quality.

[Anthony Starks](https://twitter.com/ajstarks) created an awesome library for building SVGs in Go called [svgo](https://github.com/ajstarks/svgo). Try using it to recreate some of the images you created in the past two steps, but this time try improving them. Maybe add some font labels or something else that was a little trickier to do with the `image` package.

### Notes and suggestions

**Use an `svgdef` file to learn about svgo**

They say a picture is worth a thousand words; in this case I suspect it is worth mort. Along with great docs, `svgo` has a single image that show you what types of shapes and lines can be created with each function call. Rather than having to experiment, we can just scan the image and quickly figure out which fits our needs. You can find that image in the repo, or here: <https://raw.githubusercontent.com/ajstarks/svgo/master/svgdef.png>

