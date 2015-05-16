# gridjs

### gridjs.getImageObject

Create an ImageObjet from image URL, imageData or pixel object.

```
gridjs.getImageObject(image, callback)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>string or image data or pixel object</td><td>image</td><td>If you specify the image parameter with string, it should be the URL of the image.</td></tr><tr><td>function</td><td>callback</td><td>The callback parameter should be a function that looks like this:<br><br>function(imageObject) {...};</td></tr></table>

---

### gridjs.open

An alias of `gridjs.getImageObject`.

---

### gridjs.getImageObjectFromURL

Create an ImageObjet from image URL.

```
gridjs.getImageObjectFromURL(url, callback)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>string</td><td>url</td><td>URL of an image for creating ImageObjcet.</td></tr><tr><td>function</td><td>callback</td><td>The callback parameter should be a function that looks like this:<br><br>function(imageObject) {...};</td></tr></table>

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

### gridjs.convolution

Calculate convolution of two two-dimensional arrays. The result has the same size with srcArray. The result is a new two two-dimensional array.

```
two-dimensional array gridjs.convolution(srcArray, maskArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first array of convolution.</td></tr><tr><td>two-dimensional array</td><td>maskArray</td><td>The second array of convolution.</td></tr></table>

---

### gridjs.conv

An alias of `gridjs.convolution`.

---

### gridjs.abs

Return a new two-dimensional array contains absolute values of the given two-dimensional array.

```
two-dimensional array gridjs.abs(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate absolute values with.</td></tr></table>

---

### gridjs.square

Return a new two-dimensional array contains square values of the given two-dimensional array.

```
two-dimensional array gridjs.square(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate square values with.</td></tr></table>

---

### gridjs.sqrt

Return a new two-dimensional array contains square root values of the given two-dimensional array.

```
two-dimensional array gridjs.sqrt(srcArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate square root values with.</td></tr></table>

---

### gridjs.gaussCore

Return a two-dimensional array of Gauss core with the given size and sigma.

```
two-dimensional array gridjs.gaussCore(size, sigma, derivative)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number</td><td>size</td><td>The size of the Gauss core.</td></tr><tr><td>number</td><td><br>(optional) sigma</td><td>Sigma for calculating Gauss core, default value is 1.</td></tr><tr><td>number</td><td><br>(optional) derivative</td><td>0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy.</td></tr></table>

---

### gridjs.gauss

Return a new two-dimensional array with gauss filter.

```
two-dimensional array gridjs.gaussCore(size, sigma, derivative)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The two-dimensional array to calculate Gauss filter with.</td></tr><tr><td>number</td><td>size</td><td>The size of the Gauss core.</td></tr><tr><td>number</td><td><br>(optional) sigma</td><td>Sigma for calculating Gauss core, default value is 1.</td></tr><tr><td>number</td><td><br>(optional) derivative</td><td>0 for the first derivative Gx, 1 for the first derivative Gy, 2 for the second derivative Gxy.</td></tr></table>

---

### gridjs.add

Return a new two-dimensional array contains sum values of the given two two-dimensional arrays.

```
two-dimensional array gridjs.add(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array</td><td>dstArray</td><td>The second two-dimensional array to calculate with.</td></tr></table>

---

### gridjs.minus

Calculate srcArray minus dstArray and return a new two-dimensional array with the result.

```
two-dimensional array gridjs.minus(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array</td><td>dstArray</td><td>The second two-dimensional array to calculate with.</td></tr></table>


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

### gridjs.divide

Calculate every value of srcArray divide by the same position value of dstArray and return a new two-dimensional array with the result.

If dstArray is a number, then calculate every value of srcArray divide by dstArray.

Notice: this method is not a tradition definition of matrix divide.

```
two-dimensional array gridjs.divide(srcArray, dstArray)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>two-dimensional array</td><td>srcArray</td><td>The first two-dimensional array to calculate with.</td></tr><tr><td>two-dimensional array or number</td><td>dstArray</td><td>The second two-dimensional array or number to calculate with.</td></tr></table>

---

### gridjs.zeros

Return a new two-dimensional array contains only zeros with the given size.

```
two-dimensional array gridjs.zeros(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number or two-dimensional array</td><td>width</td><td>The width of size. If width is a two-dimensional array, the result has the same size with it.</td></tr><tr><td>number</td><td>height</td><td>The height of size. if width is a two-dimensional array, this parameter will be ignored.</td></tr></table>

---

### gridjs.ones

Return a new two-dimensional array contains only ones with the given size.

```
two-dimensional array gridjs.ones(width, height)
```

<table class="table table-striped"><tr><th>Parameters</th><th></th><th></th></tr><tr><td>number or two-dimensional array</td><td>width</td><td>The width of size. If width is a two-dimensional array, the result has the same size with it.</td></tr><tr><td>number</td><td>height</td><td>The height of size. if width is a two-dimensional array, this parameter will be ignored.</td></tr></table>

---

# ImageObject

### Data Type