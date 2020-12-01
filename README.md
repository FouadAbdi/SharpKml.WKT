# sharpkml.wkt

Sharpkml saves the day when it comes to parsing KML files
It's Support Point,LineString,Polygon and multigeometry objects To Convert WellKnown Text To Store in a Geo Server , PostgreSql , SQL Server db and ....

Here's how to use it:

```csharp
//Load your kml just like normal
Parser parser = new Parser();
parser.ParseString(InputKml, false);

//Grab the placemark that has either a MultipleGeometry or Polygon Geomtery object
Placemark placemark = (Placemark)parser.Root;

//Extension doing what it does, giving us well known text ready for inserting into a SQL Geography column
string wkt = placemark.AsWKT();
```


## Note: This repository is a branch of its main repository.[→ Main Repository](https://github.com/jeddawson/sharpkml-wkt)
