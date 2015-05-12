# Method

## open

```
grid.open(image, callback);
```

* `image` : string(URL of a image) or object(imageData or pixel object)
* `callback` : function

```
callback(imageObject)
```

## getGrayScale

```
grid.getGrayScale(imageObject);
```

* return : imageObject

## blend

```
grid.blend(srcImageObject, dstImageObject, offsetX, offsetY);
```

* srcImageObject : imageObject
* dstImageObject : imageObject
* (option)offsetX : number
* (option)offsetY : number
* retrun : imageObject

# Data Type

## imageObject

```
{
  'width' : number,
  'height' : number,
  'imageData' : imageData,
  'pixel' : pixelObject
}
```

## pixelObject

```
{
  'r' : two-dimensional array,
  'g' : two-dimensional array,
  'b' : two-dimensional array,
  'a' : two-dimensional array
}
```

* refer example: `pixelObject.r[y][x]`
* numbers of channel r, g and b are integers between 0 and 255
* numbers of channel a are floats between 0 and 1
