# gridjs

### gridjs.abs

Return a new two-dimensional array contains absolute values of the given two-dimensional array.

```
two-dimensional array gridjs.abs(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate absolute values with.</td></tr></table>

---

### gridjs.add

Return a new two-dimensional array contains sum values of the given two two-dimensional arrays.

```
two-dimensional array gridjs.add(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array</td><td>dstArray</td><td>The second two-dimensional array to calculate with.</td></tr></table>

---

### gridjs.conv

An alias of `gridjs.convolution`.

---

### gridjs.convolution

Calculate convolution of two two-dimensional arrays. The result has the same size with srcArray. The result is a new two two-dimensional array.

```
two-dimensional array gridjs.convolution(srcArray, maskArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first array of convolution.</td></tr><tr><td>two-dimensional array</td><td>maskArray</td><td>The second array of convolution.</td></tr></table>

---

### gridjs.div

An alias of `gridjs.divide`.

---

### gridjs.divide

Calculate every value of srcArray divide by the same position value of dstArray and return a new two-dimensional array with the result.

If dstArray is a number, then calculate every value of srcArray divide by dstArray.

Notice: this method is not a tradition definition of matrix divide.

```
two-dimensional array gridjs.divide(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array or number</td><td>dstArray</td><td>The second two-dimensional array or number to calculate with.</td></tr></table>

---

### gridjs.gauss

Return a new two-dimensional array with gauss filter.

```
two-dimensional array gridjs.gaussCore(srcArray, size, sigma, derivative)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate Gauss filter with.</td></tr><tr><td>number</td><td>size</td><td>Size of the Gauss core.</td></tr><tr><td>number</td><td><br>(optional) sigma</td><td>Sigma for calculating Gauss core, default value is 1.</td></tr><tr><td>number</td><td><br>(optional) derivative</td><td>0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy.</td></tr></table>

---

### gridjs.gaussCore

Return a two-dimensional array of Gauss core with the given size and sigma.

```
two-dimensional array gridjs.gaussCore(size, sigma, derivative)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>size</td><td>Size of the Gauss core.</td></tr><tr><td>number</td><td><br>(optional) sigma</td><td>Sigma for calculating Gauss core, default value is 1.</td></tr><tr><td>number</td><td><br>(optional) derivative</td><td>0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy.</td></tr></table>

---

### gridjs.getImageObject

Create an ImageObjet from image URL, imageData or pixel object.

```
gridjs.getImageObject(image, callback)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>string or image data or pixel object</td><td>image</td><td>If you specify the image parameter with string, it should be the URL of the image.</td></tr><tr><td>function</td><td>callback</td><td>The callback parameter should be a function that looks like this:<br><br>function(imageObject) {...};</td></tr></table>

---

### gridjs.getImageObjectFromImageData

Create an ImageObject from image data.

```
ImageObject gridjs.getImageObjectFromImageData(imageData)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>image data</td><td>imageData</td><td>Image data of an image for creating ImageObjcet.</td></tr></table>

---

### gridjs.getImageObjectFromPixel

Create an ImageObject from pixel object.

```
ImageObject gridjs.getImageObjectFromPixel(pixel)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>pixel object</td><td>pixel</td><td>Pixel object of an image for creating ImageObjcet.</td></tr></table>

---

### gridjs.getImageObjectFromURL

Create an ImageObjet from image URL.

```
gridjs.getImageObjectFromURL(url, callback)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>string</td><td>url</td><td>URL of an image for creating ImageObjcet.</td></tr><tr><td>function</td><td>callback</td><td>The callback parameter should be a function that looks like this:<br><br>function(imageObject) {...};</td></tr></table>

---

### gridjs.minus

Calculate srcArray minus dstArray and return a new two-dimensional array with the result.

```
two-dimensional array gridjs.minus(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array</td><td>dstArray</td><td>The second two-dimensional array to calculate with.</td></tr></table>

---

### gridjs.mul

An alias of `gridjs.multiply`.

---

### gridjs.multiply

Calculate every value of srcArray multiply the same position value of dstArray and return a new two-dimensional array with the result.

If dstArray is a number, then calculate every value of srcArray multipy dstArray.

Notice: this method is not a tradition definition of matrix multiply.

```
two-dimensional array gridjs.multiply(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array or number</td><td>dstArray</td><td>The second two-dimensional array or number to calculate with.</td></tr></table>

---

### gridjs.norm

An alias of `gridjs.normalize`.

---

### gridjs.normalize

Normalize values in the two-dimensional array between the given min and max value. This method modifies origin data.

```
two-dimensional array gridjs.normalize(srcArray, min, max)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to normalize.</td></tr><tr><td>number</td><td>(optional) min</td><td>Min value to normalize with, default value is 0.</td></tr><tr><td>number</td><td>(optional) max</td><td>Max value to normalize with, default value is 1.</td></tr></table>

---

### gridjs.ones

Return a new two-dimensional array contains only ones with the given size.

```
two-dimensional array gridjs.ones(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number or two-dimensional array</td><td>width</td><td>Width of size. If width is a two-dimensional array, the result has the same size with it.</td></tr><tr><td>number</td><td>height</td><td>Height of size. if width is a two-dimensional array, this parameter will be ignored.</td></tr></table>

---

### gridjs.open

An alias of `gridjs.getImageObject`.

---

### gridjs.sqrt

Return a new two-dimensional array contains square root values of the given two-dimensional array.

```
two-dimensional array gridjs.sqrt(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate square root values with.</td></tr></table>

---

### gridjs.square

Return a new two-dimensional array contains square values of the given two-dimensional array.

```
two-dimensional array gridjs.square(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate square values with.</td></tr></table>

---

### gridjs.zeros

Return a new two-dimensional array contains only zeros with the given size.

```
two-dimensional array gridjs.zeros(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number or two-dimensional array</td><td>width</td><td>Width of size. If width is a two-dimensional array, the result has the same size with it.</td></tr><tr><td>number</td><td>height</td><td>Height of size. if width is a two-dimensional array, this parameter will be ignored.</td></tr></table>

---

# ImageObject

### Data Type

<table class="table table-striped"><tr><th>Attributes</th><th></th><th></th></tr><tr><td>number</td><td>width</td><td>Width of the image.</td></tr><tr><td>number</td><td>height</td><td>Height of the image.</td></tr><tr><td>image data</td><td>imageData</td><td>Image data of the image. See https://developer.mozilla.org/en-US/docs/Web/API/ImageData.</td></tr><tr><td>pixel object</td><td>pixel</td><td>Pixel object of the image.</td></tr><tr><td>ImageObject</td><td>origin</td><td>The origin image object of the current image object. This parameter is only available when current image object is created from ImageObject.load method.</td></tr><tr><td>number</td><td>originLeft</td><td>Left position of the origin image. This parameter is only available when current image object is created from ImageObject.load method.</td></tr><tr><td>number</td><td>originTop</td><td>Top position of the origin image. This parameter is only available when current image object is created from ImageObject.load method.</td></tr></table>

---

### Pixel Object

<table class="table table-striped"><tr><th>Attributes</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>r</td><td>Red channel of the image. Values are between 0 and 255.</td></tr><tr><td>two-dimensional array</td><td>g</td><td>Green channel of the image. Values are between 0 and 255.</td></tr><tr><td>two-dimensional array</td><td>b</td><td>Blue channel of the image. Values are between 0 and 255.</td></tr><tr><td>two-dimensional array</td><td>a</td><td>alpha channel of the image. Values are between 0 and 1.</td></tr><tr><td>two-dimensional array</td><td>G</td><td>luminance of the image. Values are between 0 and 255. This attribute is only available when the image object is converted to grayscale. If the image is grayscale, r, g and b will point to G, that is to say, if you change a pixel in G, channel r, g and b will be changed as well. You should only edit G channel in a grayscale image object.</td></tr></table>

---

### ImageObject.blank

Create a new blank image object with the given size.

```
ImageObject ImageObject.blank(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>width</td><td>Width of the blank image object.</td></tr><tr><td>number</td><td>height</td><td>Height of the blank image object.</td></tr></table>

---

### ImageObject.blend

Blend two image object. This method modifies origin data.

The current image object will be blended with the given image object. If you'd like to cover the current image object with another image object, see `ImageObject.paste`.

```
ImageObject ImageObject.blend(srcImageObject, offsetX, offsetY)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>ImageObject</td><td>srcImageObject</td><td>The image object to blend on the current image object.</td></tr><tr><td>number</td><td>offsetX</td><td>The x offset of srcImageObject on the current image object.</td></tr><tr><td>number</td><td>offsetY</td><td>The y offset of srcImageObject on the current image object.</td></tr></table>

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

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>left</td><td>Left position of the image object to crop.</td></tr><tr><td>number</td><td>top</td><td>Top position of the image object to crop.</td></tr><tr><td>number</td><td>cropWidth</td><td>Width of the size to crop.</td></tr><tr><td>number</td><td>cropHeight</td><td>Height of the size to crop.</td></tr></table>

---

### ImageObject.flip

Flip the image object with the given axis. This method modifies origin data.

```
ImageObject ImageObject.flip(axis)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>axis</td><td>0 means y axis(flip horizontal), 1 means x axis(flip vertical), 2 means x and y axis(same as rotate 180 degrees). If the given axis is none of these options, the image object will not be changed.</td></tr></table>

---

### ImageObject.grayBlank

Create a new grayscale blank image object with the given size.

```
ImageObject ImageObject.grayBlank(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>width</td><td>Width of the grayscale blank image object.</td></tr><tr><td>number</td><td>height</td><td>Height of the grayscale blank image object.</td></tr></table>

---

### ImageObject.grayscale

Convert an image object to grayscale. This method modifies origin data.

```
ImageObject ImageObject.grayscale()
```

---

### ImageObject.load

Create a new dynamic crop image object of the current image object.

You should always call `ImageObject.update` method after edit a dynamic crop image object to make changes effective on the origin image object.

```
ImageObject ImageObject.load(left, top, width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>left</td><td>Left position of the image object to load.</td></tr><tr><td>number</td><td>top</td><td>Top position of the image object to load.</td></tr><tr><td>number</td><td>width</td><td>Width of the size to load.</td></tr><tr><td>number</td><td>height</td><td>Height of the size to load.</td></tr></table>

---

### ImageObject.paste

Past another image object to the current image object with the given position.

```
ImageObject ImageObject.paste(srcImageObject, left, top)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>ImageObject</td><td>srcImageObject</td><td>The image object to paste.</td></tr><tr><td>number</td><td>(optional) left</td><td>Left position of the image object to paste, default value is 0.</td></tr><tr><td>number</td><td>(optional) top</td><td>Top position of the image object to paste, default value is 0.</td></tr></table>

---

### ImageObject.resize

Resize the current image object. This method modifies origin data.

The image object will be stretched with the given size. If you'd like to crop an image object, see `ImageObject.crop`.

```
ImageObject ImageObject.resize(newWidth, newHeight)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>newWidth</td><td>New width of the image object.</td></tr><tr><td>number</td><td>newHeight</td><td>New height of the image object.</td></tr></table>

---

### ImageObject.rotate

Rotate the image object counterclockwise with the given degree. This method modifies origin data.

Notice: this method probably change the size of image data. For exmaple, if the origin image is a square, the width and height will change to 1.414 times after rotating 45 degress.

```
ImageObject ImageObject.rotate(degree)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>degree</td><td>Degree to rotate the image object with.</td></tr></table>

---

### ImageObject.show

Show the image object on the given canvas element.

```
ImageObject ImageObject.show(canvas)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>canvas element</td><td>canvas</td><td>The canvas on which to show the image object.</td></tr></table>

---

### ImageObject.update

A alias of `ImageObject.updateImageData`.

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