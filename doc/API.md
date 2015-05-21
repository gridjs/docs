# gridjs

### gridjs.abs

Return a new two-dimensional array contains absolute values of the given two-dimensional array.

```
two-dimensional array gridjs.abs(srcArray)
```

| Parameters |  |  |
|-----------------------|----------|--------------------------------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to calculate absolute values with. |

---

### gridjs.add

Return a new two-dimensional array contains sum values of the given two two-dimensional arrays.

```
two-dimensional array gridjs.add(srcArray, dstArray)
```

| Parameters |  |  |
|-----------------------|----------|-----------------------------------------------------|
| two-dimensional array | srcArray | The first two-dimensional array to calculate with. |
| two-dimensional array | dstArray | The second two-dimensional array to calculate with. |

---

### gridjs.blank

Create a new blank image object with the given size.

```
ImageObject gridjs.blank(width, height, fill)
```

| Parameters |  |  |
|------------|--------|-----------------------------------|
| number | width | Width of the blank image object. |
| number | height | Height of the blank image object. |
| array | (optional) fill | Background fill color with r, g, b and a channel, default value of every channel is 0. For example, [255, 0, 0, 1] means red. |

---

### gridjs.conv

An alias of `gridjs.convolution`.

---

### gridjs.convolution

Calculate convolution of two two-dimensional arrays. The result has the same size with srcArray. The result is a new two two-dimensional array.

```
two-dimensional array gridjs.convolution(srcArray, maskArray)
```

| Parameters |  |  |
|-----------------------|-----------|----------------------------------|
| two-dimensional array | srcArray | The first array of convolution. |
| two-dimensional array | maskArray | The second array of convolution. |

---

### gridjs.cutoff

Cut off values of the two-dimensional array with the given max value, values larger then the given max value will be set to the max value. This method modifis origin data.

```
two-dimensional array gridjs.cutoff(srcArray, max)
```

| Parameters |  |  |
|-----------------------|----------|---------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to cut off. |
| number | max | Max value to cut off srcArray with. |

---

### gridjs.div

An alias of `gridjs.divide`.

---

### gridjs.divide

Calculate every value of srcArray divide by the same position value of dstArray and return a new two-dimensional array with the result.

If dstArray is a number, then calculate every value of srcArray divide by dstArray.

Notice: this method is not a traditional definition of matrix divide.

```
two-dimensional array gridjs.divide(srcArray, dstArray)
```

| Parameters |  |  |
|---------------------------------|-------------------------|------------------------------------------------------------------------------------|
| two-dimensional array | srcArray | The first two-dimensional array to calculate with. |
| two-dimensional array or number | dstArray | The second two-dimensional array or number to calculate with. |
| number | (optional) defaultValue | If this parameter is set, the quotient will be set to it when denominator is zero. |

---

### gridjs.gauss

Return a new two-dimensional array with gauss filter.

```
two-dimensional array gridjs.gaussCore(srcArray, size, sigma, derivative)
```

| Parameters |  |  |
|-----------------------|-----------------------|------------------------------------------------------------------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to calculate Gauss filter with. |
| number | size | Size of the Gauss core. |
| number | (optional) sigma | Sigma for calculating Gauss core, default value is 1. |
| number | (optional) derivative | 0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy. |

---

### gridjs.gaussCore

Return a two-dimensional array of Gauss core with the given size and sigma.

```
two-dimensional array gridjs.gaussCore(size, sigma, derivative)
```

| Parameters |  |  |
|------------|-----------------------|------------------------------------------------------------------------------------------------|
| number | size | Size of the Gauss core. |
| number | (optional) sigma | Sigma for calculating Gauss core, default value is 1. |
| number | (optional) derivative | 0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy. |

---

### gridjs.getImageObject

Create an ImageObjet from image URL, imageData or pixel object.

```
gridjs.getImageObject(image, callback)
```

| Parameters |  |  |
|--------------------------------------|----------|------------------------------------------------------------------------------------------------|
| string or image data or pixel object | image | If you specify the image parameter with string, it should be the URL of the image. |
| function | callback | The callback parameter should be a function that looks like this: function(imageObject) {...}; |

---

### gridjs.getImageObjectFromImageData

Create an ImageObject from image data.

```
ImageObject gridjs.getImageObjectFromImageData(imageData)
```

| Parameters |  |  |
|------------|-----------|--------------------------------------------------|
| image data | imageData | Image data of an image for creating ImageObjcet. |

---

### gridjs.getImageObjectFromPixel

Create an ImageObject from pixel object.

```
ImageObject gridjs.getImageObjectFromPixel(pixel)
```

| Parameters |  |  |
|--------------|-------|----------------------------------------------------|
| pixel object | pixel | Pixel object of an image for creating ImageObjcet. |

---

### gridjs.getImageObjectFromURL

Create an ImageObjet from image URL.

```
gridjs.getImageObjectFromURL(url, callback)
```

| Parameters |  |  |
|------------|----------|------------------------------------------------------------------------------------------------|
| string | url | URL of an image for creating ImageObjcet. |
| function | callback | The callback parameter should be a function that looks like this: function(imageObject) {...}; |

---

### gridjs.kmeans

Calculate k-means clustering.

```
object gridjs.kmeans(points, k, maxStep)
```

| Parameters |  |  |
|----------------------|--------------------|------------------------------------------------------------------------------|
| point list | points | The point list should be a two-dimensional array like [[x0, y0], [x1, y1], ...]. |
| number | k | Number of clusters. |
| number | (optional) maxStep | Max step for calculating, default value is 20. |

| Result |  |  |
|----------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| point list | center | Centers of clusters that is a two-dimensional array like [[x0, y0], [x1, y1], ...]. |
| array of point list | cluster | Center of the *n*th cluster is center[n]. |

---

### gridjs.minus

Calculate srcArray minus dstArray and return a new two-dimensional array with the result.

```
two-dimensional array gridjs.minus(srcArray, dstArray)
```

| Parameters |  |  |
|-----------------------|----------|-----------------------------------------------------|
| two-dimensional array | srcArray | The first two-dimensional array to calculate with. |
| two-dimensional array | dstArray | The second two-dimensional array to calculate with. |

---

### gridjs.mul

An alias of `gridjs.multiply`.

---

### gridjs.multiply

Calculate every value of srcArray multiply the same position value of dstArray and return a new two-dimensional array with the result.

If dstArray is a number, then calculate every value of srcArray multipy dstArray.

Notice: this method is not a traditional definition of matrix multiply.

```
two-dimensional array gridjs.multiply(srcArray, dstArray)
```

| Parameters |  |  |
|---------------------------------|----------|---------------------------------------------------------------|
| two-dimensional array | srcArray | The first two-dimensional array to calculate with. |
| two-dimensional array or number | dstArray | The second two-dimensional array or number to calculate with. |

---

### gridjs.norm

An alias of `gridjs.normalize`.

---

### gridjs.normalize

Normalize values in the two-dimensional array between the given min and max value. This method modifies origin data.

```
two-dimensional array gridjs.normalize(srcArray, min, max)
```

| Parameters |  |  |
|-----------------------|----------------|--------------------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to normalize. |
| number | (optional) min | Min value to normalize with, default value is 0. |
| number | (optional) max | Max value to normalize with, default value is 1. |

---

### gridjs.ones

Return a new two-dimensional array contains only ones with the given size.

```
two-dimensional array gridjs.ones(width, height, value)
```

| Parameters |  |  |
|---------------------------------|------------------|-------------------------------------------------------------------------------------------|
| number or two-dimensional array | width | Width of size. If width is a two-dimensional array, the result has the same size with it. |
| number | height | Height of size. if width is a two-dimensional array, this parameter will be ignored. |
| number | (optional) value | The value the two-dimensional array contains, default value is 1. |

---

### gridjs.open

An alias of `gridjs.getImageObject`.

---

### gridjs.sqrt

Return a new two-dimensional array contains square root values of the given two-dimensional array.

```
two-dimensional array gridjs.sqrt(srcArray)
```

| Parameters |  |  |
|-----------------------|----------|-----------------------------------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to calculate square root values with. |

---

### gridjs.square

Return a new two-dimensional array contains square values of the given two-dimensional array.

```
two-dimensional array gridjs.square(srcArray)
```

| Parameters |  |  |
|-----------------------|----------|------------------------------------------------------------|
| two-dimensional array | srcArray | The two-dimensional array to calculate square values with. |

---

### gridjs.zeros

Return a new two-dimensional array contains only zeros with the given size.

```
two-dimensional array gridjs.zeros(width, height)
```

| Parameters |  |  |
|---------------------------------|--------|-------------------------------------------------------------------------------------------|
| number or two-dimensional array | width | Width of size. If width is a two-dimensional array, the result has the same size with it. |
| number | height | Height of size. if width is a two-dimensional array, this parameter will be ignored. |

---

# ImageObject

### Data Type

| Attributes |  |  |
|--------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| number | width | Width of the image. |
| number | height | Height of the image. |
| image data | imageData | Image data of the image. See <https://developer.mozilla.org/en-US/docs/Web/API/ImageData>. |
| pixel object | pixel | Pixel object of the image. |
| ImageObject | origin | The origin image object of the current image object. This parameter is only available when current image object is created from ImageObject.load method. |
| number | originLeft | Left position of the origin image. This parameter is only available when current image object is created from ImageObject.load method. |
| number | originTop | Top position of the origin image. This parameter is only available when current image object is created from ImageObject.load method. |

---

### Pixel Object

| Attributes |  |  |
|-----------------------|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| two-dimensional array | r | Red channel of the image. Values are between 0 and 255. |
| two-dimensional array | g | Green channel of the image. Values are between 0 and 255. |
| two-dimensional array | b | Blue channel of the image. Values are between 0 and 255. |
| two-dimensional array | a | alpha channel of the image. Values are between 0 and 1. |
| two-dimensional array | G | luminance of the image. Values are between 0 and 255. This attribute is only available when the image object is converted to grayscale. If the image is grayscale, r, g and b will point to G, that is to say, if you change a pixel in G, channel r, g and b will be changed as well. You should only edit G channel in a grayscale image object. |

---

### ImageObject.arc

Draw an arc on the image object.

```
ImageObject ImageObject.arc(centerX, centerY, radius, startDegree, endDegree, fill, stroke)
```

| Result |  |  |
|--------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| number | centerX | Left position of center of the arc on the image object. |
| number | centerY | Top position of center of the arc on the image object. |
| number | radius | Radius of the arc. |
| number | startDegree | Start degree of the arc. |
| number | endDegree | End degree of the arc. |
| array | (optional) fill | Fill color with r, g, b and a channel, default value of every channel is 0. For example, [255, 0, 0, 1] means red. |
| array | (optional) stroke | Stoke color with r, g, b and a channel, and line width, default value of every channel and line width is 0. For example, [0, 0, 255, 1, 2] means stroke with 2px width blue lines. |

---

### ImageObject.blend

Blend two image object. This method modifies origin data.

The current image object will be blended with the given image object. If you'd like to cover the current image object with another image object, see `ImageObject.paste`.

```
ImageObject ImageObject.blend(srcImageObject, offsetX, offsetY)
```

| Parameters |  |  |
|-------------|----------------|-------------------------------------------------------------|
| ImageObject | srcImageObject | The image object to blend on the current image object. |
| number | offsetX | The x offset of srcImageObject on the current image object. |
| number | offsetY | The y offset of srcImageObject on the current image object. |

---

### ImageObject.circle

Draw a circle on the image object.

```
ImageObject ImageObject.circle(centerX, centerY, ra)
```

| Result |  |  |
|--------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| number | centerX | Left position of center of the circle on the image object. |
| number | centerY | Top position of center of the circle on the image object. |
| number | radius | Radius of the circle. |
| array | (optional) fill | Fill color with r, g, b and a channel, default value of every channel is 0. For example, [255, 0, 0, 1] means red. |
| array | (optional) stroke | Stoke color with r, g, b and a channel, and line width, default value of every channel and line width is 0. For example, [0, 0, 255, 1, 2] means stroke with 2px width blue lines. |

---

### ImageObject.copy

Create a copy of the current image object.

```
ImageObject ImageObject.copy()
```

---

### ImageObject.crop

Crop the image object with the given position and size. This method modifies origin data.

If you'd like to create a dynamic crop of the image object(changes on the crop image object will effect the origin image object), see `ImageObject.load`.

```
ImageObject ImageObject.crop(left, top, cropWidth, cropHeight)
```

| Parameters |  |  |
|------------|------------|--------------------------------------------|
| number | left | Left position of the image object to crop. |
| number | top | Top position of the image object to crop. |
| number | cropWidth | Width of the size to crop. |
| number | cropHeight | Height of the size to crop. |

---

### ImageObject.flip

Flip the image object with the given axis. This method modifies origin data.

```
ImageObject ImageObject.flip(axis)
```

| Parameters |  |  |
|------------|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| number | axis | 0 means y axis(flip horizontal), 1 means x axis(flip vertical), 2 means x and y axis(same as rotate 180 degrees). If the given axis is none of these options, the image object will not be changed. |

---

### ImageObject.flush

Update image object with workplace data immediately. You should only call this method after `ImageObject.hold`.

```
ImageObject ImageObject.flush()
```

---

### ImageObject.grayscale

Convert an image object to grayscale. This method modifies origin data.

```
ImageObject ImageObject.grayscale()
```

---

### ImageObject.hold

Do not update image object form workplace data until `ImageObject.flush` is called. This method is only avaliable for `ImageObject.plot`, `ImageObject.rect`, `ImageObject.arc`, `ImageObject.circle` and `ImageObject.poly`. If you have many geometries to draw, and you'd like to do that within a loop, then you should call this method before the loop, and then call `ImageObject.flush` to update the image object.

```
ImageObject ImageObject.hold()
```

---

### ImageObject.load

Create a new dynamic crop image object of the current image object.

You should always call `ImageObject.update` method after edit a dynamic crop image object to make changes effective on the origin image object.

```
ImageObject ImageObject.load(left, top, width, height)
```

| Parameters |  |  |
|------------|--------|--------------------------------------------|
| number | left | Left position of the image object to load. |
| number | top | Top position of the image object to load. |
| number | width | Width of the size to load. |
| number | height | Height of the size to load. |

---

### ImageObject.paste

Past another image object to the current image object with the given position.

```
ImageObject ImageObject.paste(srcImageObject, left, top)
```

| Parameters |  |  |
|-------------|-----------------|-----------------------------------------------------------------|
| ImageObject | srcImageObject | The image object to paste. |
| number | (optional) left | Left position of the image object to paste, default value is 0. |
| number | (optional) top | Top position of the image object to paste, default value is 0. |

---

### ImageObject.plot

Draw dots and lines on an image object. This method modifies origin data.

```
ImageObject ImageObject.plot(points, style)
```

| Parameters |  |  |
|-------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| array or array of array | points | If this parameter is array, it should contain two values, x and y. If this parameter is array of array, it should contain arrays that contain two values, x and y. For example, [x, y] or [[x0, y0], [x1, y1], ...]. You may also call this method with three parameters: x, y and style. For example, ImageObject.plot(10, 100, 'ro'). |
| string | (optional) style | Style contains three commands to define color, dot style and line style. Colors: 'b' for blue, 'g' for green, 'r' for red, 'c' for cyan, 'm' for magenta, 'y' for yellow, 'k' for black and 'w' for white. Dot styles: '.' for dot, 'o' for circle, 's' for square, '\*' for star, '+' for plus and 'x' for cross. Line styles: '-' for dashed, '--' for solid, ':' for dotted. For example, 'go-' means green dashed lines with circle symbols, 'r\*' means red star symbols. The default style is blue solid lines without symbols. |

---

### ImageObject.poly

An alias of `ImageObject.ploygon`.

---

### ImageObject.polygon

Draw a polygon on the image object.

```
ImageObject ImageObject.polygon(points, fill, stroke)
```

| Parameters |  |  |
|----------------------|--------------------|------------------------------------------------------------------------------|
| point list | points | The point list should be a two-dimensional array like [[x0, y0], [x1, y1], ...]. |
| array | (optional) fill | Fill color with r, g, b and a channel, default value of every channel is 0. For example, [255, 0, 0, 1] means red. |
| array | (optional) stroke | Stroke color with r, g, b and a channel, and line width, default value of every channel and line width is 0. For example, [0, 0, 255, 1, 2] means stroke with 2px width blue lines. |

---

### ImageObject.rect

An alias of `ImageObject.rectangle`.

---

### ImageObject.rectangle

Draw a rectangle on the image object. This method modifies origin data.

```
ImageObject ImageObject.rectangle(left, top, width, height, fill, stroke)
```

| Result |  |  |
|--------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| number | left | Left position of the rectangle on the image object. |
| number | top | Top position of the rectangle on the image object. |
| number | width | Width of the rectangle. |
| number | height | Height of the rectangle. |
| array | (optional) fill | Fill color with r, g, b and a channel, default value of every channel is 0. For example, [255, 0, 0, 1] means red. |
| array | (optional) stroke | Stroke color with r, g, b and a channel, and line width, default value of every channel and line width is 0. For example, [0, 0, 255, 1, 2] means stroke with 2px width blue lines. |

---

### ImageObject.resize

Resize the current image object. This method modifies origin data.

The image object will be stretched with the given size. If you'd like to crop an image object, see `ImageObject.crop`.

```
ImageObject ImageObject.resize(newWidth, newHeight)
```

| Parameters |  |  |
|------------|-----------|---------------------------------|
| number | newWidth | New width of the image object. |
| number | newHeight | New height of the image object. |

---

### ImageObject.reverse

Reverse colors of the image object.

```
ImageObject ImageObject.reverse()
```

---

### ImageObject.rgba

Convert an image object to RGBA. This method modifies origin data.

```
ImageObject ImageObject.rgba()
```

---

### ImageObject.rotate

Rotate the image object counterclockwise with the given degree. This method modifies origin data.

Notice: this method probably changes the size of image data. For exmaple, if the origin image is a square, the width and height will change to 1.414 times after rotating 45 degrees.

```
ImageObject ImageObject.rotate(degree)
```

| Parameters |  |  |
|------------|--------|-----------------------------------------|
| number | degree | Degree to rotate the image object with. |

---

### ImageObject.show

Show the image object on the given canvas element.

```
ImageObject ImageObject.show(canvas)
```

| Parameters |  |  |
|----------------|--------|-----------------------------------------------|
| canvas element or img element | canvas | The canvas on which to show the image object. |

---

### ImageObject.update

An alias of `ImageObject.updateImageData`.

---

### ImageObject.updateImageData

Update the image object with pixel object of the image object. This method modifies origin data. Width and height attributes will be updated as well.

You should always call this method after you edit pixel object of an image object.

```
ImageObject ImageObject.updateImageData()
```

---

### ImageObject.updatePixel

Update the image object with image data of the image object. This method modifies origin data. Width and height attributes will be updated as well.

You should always call this method after you edit image data of an image object.

Notice: edit image data is not recommended.

```
ImageObject ImageObject.updatePixel()
```

---

EOF