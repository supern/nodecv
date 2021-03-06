# nodecv

[![NPM version][npm-image]][npm-url]
[![build status][travis-image]][travis-url]
[![node version][node-image]][node-url]

[npm-image]: https://img.shields.io/npm/v/nodecv.svg?style=flat-square
[npm-url]: https://npmjs.org/package/nodecv
[travis-image]: https://img.shields.io/travis/xudafeng/nodecv.svg?style=flat-square
[travis-url]: https://travis-ci.org/xudafeng/nodecv
[node-image]: https://img.shields.io/badge/node.js-%3E=_6-green.svg?style=flat-square
[node-url]: http://nodejs.org/download/

> Node.js binding to [OpenCV](//github.com/opencv/opencv)

## Installment

``` bash
$ npm i nodecv --save-dev
```

## Usage

Image IO:

``` javascript
nodecv.imread(imagePath, callback)
nodecv.imread(buffer, callback)
nodecv.imwrite(outputPath, mat);
```

Image Dissimilarity:

``` javascript
nodecv.imageDissimilarity(mat, mat, callback)
```

Mat properties:

``` javascript
im.width()
im.height()
im.size()
im.ellipse(x, y, width, height)
im.rectangle(x, y, width, height, color, thickness)
```

Cascade detect:

``` javascript
const haarcascade = 'path/to/haarcascade.xml';
const cascade = new nodecv.CascadeClassifier(haarcascade);
cascade.detectMultiScale(mat, callback)
```

NodeCV follow [Google's C++ style conventions](//google.github.io/styleguide/cppguide.html), and [opencv@2.4.13.2](http://docs.opencv.org/2.4.13.2/).

## Test

``` bash
$ make test
```

## License

The MIT License (MIT)
