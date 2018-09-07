# Intelligent Campus Mapping Ontology

The Intelligent Campus Mapping ontology is a simple ontology that can be used with GeoJSON, the ontology maps directly to[OpenStreetMap Keys](https://wiki.openstreetmap.org/wiki/Keys) or [OpenStreetMap tags](https://wiki.openstreetmap.org/wiki/Tags) for practicle easy mappint

[List of items](./items.md)
[List of properties](./properties.md)


### Buildings Example

A simple should use the [University entity](https://wiki.openstreetmap.org/wiki/Tags) with a recommended minimum of the building, operator, name. A building that spans an area should be supplied with an array of coordinates, which can be converted to an OSM way.

#### GeoJSON JSON Example
`

``` Javascript
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-0.140043, 51.5173639]
  },
  "properties": {
        "Operator": "University of Jisc",
        "Name": "The Frank Herbert Building",
        "Building": "yes"
      }
}
```

#### Open Street Map XML Example

```
 <node id="1345484518" lat="51.5173639" lon="-0.140043">
  <tag k="amenity" v="university"/>
  <tag k="building" v="yes"/>
  <tag k="name" v="The Frank Herbert Building"/>
  <tag k="operator" v="University of Cambridge"/>
 </node>
```

#### Examples on Open Street Map

A single long lat example: [Combination room at the University of Cambridge](https://www.openstreetmap.org/node/1345484518)

An area: [Anglia Ruskin University]: https://www.openstreetmap.org/way/135077623