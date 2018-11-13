# Intelligent Campus Service Point Ontology

The Intelligent Campus Mapping ontology is a service point ontology. It is based upon the Open Street Maps concepts of [OpenStreetMap tags](https://wiki.openstreetmap.org/wiki/Tags). Each object in the ontology is made up of required key pairs that map to these tags. 

Each object is described as a series of required key-pairs that are described in the documentation in two formats, a GeoJSON object and Open Street Map XML.


- [List of Object](./items.md)

- [List of keys](./properties.md)

### Useful Tools

- [OSM & GeoJSON converts between OSM XML and GeoJSON](https://gist.github.com/tecoholic/1396990)
- [Hosted OSM & GeoJSON converts between OSM XML and GeoJSON](http://bretagne-vivante-dev.org/js/osm-and-geojson/)

### University Building Example
A University should use the [University item](items.md#university) with the keys building, operator, name. In GeoJSON, a building that spans an area should be supplied with an array of coordinates, which can be converted to an [OSM way](https://wiki.openstreetmap.org/wiki/Way).

### University
<table>
<tr><th align="left">label</th><td>University</td></tr>
<tr><th align="left">Description</th><td>Academic institution for further education</td></tr>
<tr><th align="left">Open Street Map Key pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity">amenity=university</a></td></tr>
<tr><th align="left">GeoJSON Required key pairs</th><td>"amenity":"university"</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Keys should be used with </th><td><ul><li><a href="./items.md#entrance">Building</a></li><li><a href="./items.md#operator">Name</a></li><li><a href="./items.md#name">Operator</a></li></ul> </td></tr>
<tr><th align="left">Keys, can be used with </th><td><ul><li><a href="./items.md#capacity">Capacity</a></li><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>



#### GeoJSON JSON Example

``` Javascript
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [-0.140043, 51.5173639]
  },
  "properties": {
        "amenity": "University",
        "operator": "University of Jisc",
        "name": "The Frank Herbert Building",
        "building": "yes"
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

An area making up a building: [Anglia Ruskin University](https://www.openstreetmap.org/way/135077623)