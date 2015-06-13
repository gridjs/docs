# Get Start

GridJS is a JavaScript imaging library for web programming, it makes image processing easier in browsers. You can download it from <https://cdn.jsdelivr.net/gridjs/0.1.0/gridjs.min.js>.

To use GridJS in your code, just create a script element within any web page:

```
<script src="gridjs.js"></script>
```

### Open An Image

GridJS provides three ways to open image, from URL, from image data and from pixel object. To open an image from URL, you can call `gridjs.open` method:

```
gridjs.open('picture.jpg', function(im) {
  // do something with im.
});
```

You may notice `gridjs.open` has a callback function parameter to take the returned image object. We do know most people do not like callbacks, that's fine, only when you open an image from URL you have to touch callback, otherwise, you won't find any callback in GridJS any more.

To open an image from image data, you can call `gridjs.getImageObjectFromImageData` method:

```
content = canvas.getContent('2d');
imageData = content.getImageData(0, 0, width, height);
im = gridjs.getImageObjectFromImageData(imageData);
// do something with im.
```

To open an image from pixel, you can call `gridjs.getImageObjectFromPixel` method:

```
im = gridjs.getImageObjectFromPixel(pixel);
```

`pixel` in above code is a pixel object, you can learn more at <http://gridjs.org/docs/API.html#index_Pixel%20Object>.

### Create A Blank Image

You can also create a blank image with `gridjs.blank` method:

```
im = gridjs.blank(500, 400, [255, 255, 255, 1]);
```

### Process An Image Object

Now we have an image object, then we can call all methods belone to `ImageObject` to process. You can find a full list of `ImageObject` at <http://gridjs.org/docs/API.html#index_ImageObject>.

An image object has 4 attributes, width, height, imageData and pixel. You should never edit width and height attribute, and to edit imageData is not recommended. And you should always call `ImageObject.update` after you edit pixel, and call `ImageObject.updatePixel` after you edit imageData.

Code below will resize the image object:

```
im.resize(200, 100);
```

Most `ImageObject` methods modify the origin data, that is to say, for example, after you call `ImageObject.resize` method, the image object itself will be resized, but not get a copy. If you don't like to modify the origin data, you can call `ImageObject.copy` method to create a copy, then modify the copy:

```
im2 = im.copy(); // im2 is a copy of im
im2.resize(200, 100); // im2 is resized to 200 by 100, and im is not modified
```

All methods of `ImageObject` return `ImageObject`, that means you can call methods in one line:

```
im2 = im.copy().resize(200, 100);
```

To show an image object, you can call `ImageObject.show` method. To use this method, you need assign a canvas element or an img element to place the image:

```
canvas = document.getElementsByTagName('canvas')[0];
img = document.getElementsByTagName('img')[0];

im.show(canvas);
im.resize(200, 100);
im.show(img);
```

Do you remember we can call methods in only one line? So let's change code above to this:

```
im.show(canvas).resize(200, 100).show(img);
```

# Basic Image Processing

GridJS provides several basic image processing methods, you can call them very comfortably.

### Resize And Rotate

Resize an image to 200 by 100 then rotate it with 90 degree:

```
im.resize(200, 100).rotate(90);
```

### Grayscale

Grayscale method converts image to grayscale:

```
im.grayscale();
```

### Splice Images

Splice two images:

```
im = gridjs.blank(400, 200);
im.paste(im1, 0, 0).paste(im2, 200, 0);
```

More methods can be found at <http://gridjs.org/docs/API.html#index_ImageObject>.

# Image Processing With Pixel

Basic image processing methods are very limited, so you may need edit pixel to process the image. GridJS provides a pixel object in every image object, so you can edit pixel very easy with GridJS.

You can learn more about pixel object at <http://gridjs.org/docs/API.html#index_Pixel Object>.

### Find Image Edges

```
var mask = [
  [-1, -2, -1],
  [-2, 12, -2],
  [-1, -2, -1],
];

im.grayscale();
im.pixel.G = gridjs.conv(im.pixel.G, mask);
im.pixel.G = gridjs.cutoff(im.pixel.G, 255);
im.update().reverse().show(canvas);
```

### Modify Image Color

```
var newR, newG, newB;

newR = gridjs.multiply(im.pixel.r, 0.393);
newR = gridjs.add(newR, gridjs.multiply(im.pixel.g, 0.769));
newR = gridjs.add(newR, gridjs.multiply(im.pixel.b, 0.189));

newG = gridjs.multiply(im.pixel.r, 0.349);
newG = gridjs.add(newG, gridjs.multiply(im.pixel.g, 0.686));
newG = gridjs.add(newG, gridjs.multiply(im.pixel.b, 0.168));

newB = gridjs.multiply(im.pixel.r, 0.272);
newB = gridjs.add(newB, gridjs.multiply(im.pixel.g, 0.534));
newB = gridjs.add(newB, gridjs.multiply(im.pixel.b, 0.131));

im.pixel.r = newR;
im.pixel.g = newG;
im.pixel.b = newB;

im.update().show(canvas);
```

# Computer Visual

### Corner Detector

```
function harris(srcArray) {
  var imx, imy, wxx, wyy, wxy, wdet, wtr, H,
      g = gridjs;

      imx = g.gauss(srcArray, 5, 1, 0);
      imy = g.gauss(srcArray, 5, 1, 1);

      wxx = g.gauss(g.square(imx), 5);
      wyy = g.gauss(g.square(imy), 5);
      wxy = g.gauss(g.mul(imx, imy), 5);

      wdet = g.minus(g.mul(wxx, wyy), g.square(wxy));
      wtr = g.add(wxx, wyy);

      H = g.div(wdet, wtr, 0);

      g.norm(H);

      return H;
}

function getHarrisPoint(harrisArray, threshold, minDistance) {
  var x, y, i, j, distance2,
      minDistance2 = minDistance * minDistance,
      index = 0,
      width = harrisArray[0].length,
      height = harrisArray.length,
      points = [];

  for (y = 0; y < height; y++) {
    for (x = 0; x < width; x++) {
      if (harrisArray[y][x] >= threshold) {
        points[index++] = {
          'x' : x,
          'y' : y,
          'h' : harrisArray[y][x]
        }
      }
    }
  }

  points.sort(function(a, b) {
    return b.h - a.h;
  });

  for (i = 0; i < points.length; i++) {
    for (j = 0; j < i; j++) {
      distance2 = (points[i].x - points[j].x) * (points[i].x - points[j].x) +
                  (points[i].y - points[j].y) * (points[i].y - points[j].y);

      if (distance2 < minDistance2) {
        points.splice(i, 1);
        i--;
        break;
      }
    }
  }

  return points;
}

var H, corners, i;

im.grayscale();
H = harris(im.pixel.G);
corners = getHarrisPoint(H, 0.015, 10);
im.rgba();

for (i = 0; i < corners.length; i++) {
  im.pixel.r[corners[i].y][corners[i].x] = 255;
  im.pixel.g[corners[i].y][corners[i].x] = 0;
  im.pixel.b[corners[i].y][corners[i].x] = 0;
}

im.update().show(canvas);
```

# Data Analysis

### Clustering

```
im = gridjs.blank(500, 500, [64, 64, 64, 1]);
colors = ['c', 'g', 'y', 'r', 'm', 'b'];
points = [];

for (i = 0; i < 100; i++) {
  x = Math.round(Math.random() * 100);
  y = Math.round(Math.random() * 100);
  points[i * 3] = [x + 50, y + 50];
  points[i * 3 + 1] = [Math.round(Math.random() * 200) + 250, Math.round(Math.random() * 200) + 100];
  points[i * 3 + 2] = [Math.round(Math.random() * 100) + 100, Math.round(Math.random() * 100) + 300];
}

vq = gridjs.kmeans(points, 3);
im.hold();
for (i = 0; i < vq.cluster.length; i++) {
  im.plot(vq.cluster[i], colors[i % 6] + '.');
}
im.plot(vq.center, 'k*');
im.flush().show(canvas);
```