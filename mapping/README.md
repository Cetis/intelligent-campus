# Intelligent Campus Service Point Ontology

The Intelligent Campus Mapping ontology is a service point ontology based upon the Open Street Maps concepts of [OpenStreetMap key pairs called tags](https://wiki.openstreetmap.org/wiki/Tags). Each entity in the ontology is made up of at least one required key:value, with sugguested additional key pairs that may be recommended or optional.  

The documentation describes ib in two formats, a GeoJSON JSON object and in Open Street Map XML. Since objects and their properties are derived from popular Open Street Maps tags, users should be able to use which ever is applicable.

The objects and properties lists are not exhaustive. Implementors may wish to look on the Open Street Map Tag page for an objects for other properties and their key pairs 

- [List of Objects](./items.md)
- [List of Properties](./properties.md)

### Useful Tools

- [OSM & GeoJSON converts between OSM XML and GeoJSON](https://gist.github.com/tecoholic/1396990)
- [Hosted OSM & GeoJSON converts between OSM XML and GeoJSON](http://bretagne-vivante-dev.org/js/osm-and-geojson/)

### University Building Example

<table>
<tr><th align="left">label</th><td>University</td></tr>
<tr><th align="left">Description</th><td>Academic institution for further education</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Open Street Map Key pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity">amenity=university</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"university"</td></tr>
<tr><th align="left">Recommended key pairs</th><td><ul><li><a href="./items.md#entrance">Building</a></li><li><a href="./items.md#operator">Name</a></li><li><a href="./items.md#name">Operator</a></li></ul> </td></tr>
<tr><th align="left">Example of related key pairs</th><td><ul><li><a href="./items.md#capacity">Capacity</a></li><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>


#### Notes

- A University Building should use the [amenity:University](items.md#university) key pair, with keys building, operator, name.
 
- In GeoJSON, a building that spans an area should be supplied with an array of coordinates, which can be converted to an [OSM way](https://wiki.openstreetmap.org/wiki/Way).


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