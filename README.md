# Polygon Experiment

- Experiments with finding a center point of a polygon.
- Find approximate center point of an arbitrary polygon on Google Maps.

This will get the centerpoint of any shape as and array [centerLat, centerLng]:
```sh
var coordinatesArray = shape.getPath().getArray();

var center = function(coordinatesArray){
    var minX, maxX, minY, maxY;
    for(var i=0; i< coordinatesArray.length; i++){
        minX = (coordinatesArray[i][0] < minX || minX == null) ? coordinatesArray[i][0] : minX;
        maxX = (coordinatesArray[i][0] > maxX || maxX == null) ? coordinatesArray[i][0] : maxX;
        minY = (coordinatesArray[i][1] < minY || minY == null) ? coordinatesArray[i][1] : minY;
        maxY = (coordinatesArray[i][1] > maxY || maxY == null) ? coordinatesArray[i][1] : maxY;
    }
    return [(minX + maxX) /2, (minY + maxY) /2];
}

var mycenter = center(coords);
console.log(mycenter);
```

# Notes

 You need to supply a Google Maps API key and set this in the link to the Google Maps API JavaScript in index.html. Because we are using google.maps.geometry functions, the link to get the Google Maps API JavaSCript needs to include &libraries=geometry (see index.html).

  - I'am using the Google Maps Javascript API v3
  - add this librarie ``` https://maps.googleapis.com/maps/api/js?key=YourApiKey&libraries=geometry ```

## License
(The MIT License)

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Owner

Agridata is an editor, integrator of IT solutions for 100% of the agricultural ecosystem. Our objective is to help agriculture to be more profitable, more competitive and more environmentally friendly through better use of data.
* Adresse : Agridata Consulting, Imm.Azizia, 2ème ét, Av .Hassan || AGADIR
* Tel     : (212) 66 33 47 093
* Fixe    : (212) 528 82 84 44
* Fax     : (212) 528 82 59 49
* Email   : contact@agridata-consulting.com
* Check-out: [Check-out](http://agridata-consulting.com)





   
