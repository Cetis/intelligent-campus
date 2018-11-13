## Ontology entities
The intelligent campus ontology is an approach and not an exhaustive list. Entities map to popular OSM key pairs. This list documents popular entities and properties that may be implemented against them. To avoid mirroring the OSM documentation a list of popular entities with of OSM and geoJSON examples are kept here. Implementers may want to check there OSM documentation for other [key pairs](https://wiki.openstreetmap.org/wiki/Tags).

### University Building

A University should use the [amenity:University](https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity) key pair, with keys building, operator, name.

<table>
<tr><th align="left">label</th><td>University</td></tr>
<tr><th align="left">Description</th><td>Academic institution for further education</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Open Street Map Key pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity">amenity=university</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"university"</td></tr>
<tr><th align="left">Recommended properties</th><td><ul><li><a href="./items.md#building">Building</a></li><li><a href="./properties.md#Name">Name</a></li><li><a href="./properties.md#operator">Operator</a></li></ul> </td></tr>
<tr><th align="left">Example properties</th><td><ul><li><a href="./properties.md#capacity">Capacity</a></li><li><a href="./properties.md#entrance">Entrance</a></li><li><a href="./properties.md#name">Name</a></li><li><a href="./properties.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
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

#### Notes

- In GeoJSON, a building that spans an area should be supplied with an array of coordinates, which can be converted to an [OSM way](https://wiki.openstreetmap.org/wiki/Way).

### Catering

A commercial food service should use the [amenity:restaurant](https://wiki.openstreetmap.org/wiki/Tag:amenity%3Drestaurant) key pair.

<table>
<tr><th align="left">label</th><td>Catering</td></tr>
<tr><th align="left">Description</th><td>Food service</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q777754">Q777754</a> </td></tr>
<tr><th align="left">Open Street Map Page</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Drestaurant"> amenity=restaurant</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"restaurant"</td></tr>
<tr><th align="left">Example properties</th><td><ul><li><a href="./properties.md#capacity">Capacity</a></l1><li><a href="./properties.md#entrance">Entrance</a></li><li><a href="./properties.md#operator">Operator</a></li><li><a href="./properties.md#name">Name</a></li><li><a href="./properties.md#wheelchair">Wheelchair</a></li><li><a href="./properties.md#capacity">Capacity</a></li></ul> </td></tr>
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
        "amenity": "Restaurant",
        "operator": "University of Jisc",
        "name": "The Happy Cafe",
        "wheelchair": "limited"
      }
}
```

#### Open Street Map XML Example

```
<node id="-1" lat="51.517364" lon="-0.140043" >
<tag k="amenity" v="Restaurant"/>
<tag k="operator" v="University of Jisc"/>
<tag k="name" v="The Happy Cafe"/>
<tag k="wheelchair" v="limited"/>
</node>
```

#### Notes

- In GeoJSON, a building that spans an area should be supplied with an array of coordinates, which can be converted to an [OSM way](https://wiki.openstreetmap.org/wiki/Way).

### Library

A commercial food service should use the [amenity:library](https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dlibrary) key pair.


<table>
<tr><th align="left">label</th><td>Library</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q13226383">Q13226383</a> </td></tr>
<tr><th align="left">Open Street Map Key Pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dlibrary"> amenity=library</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"library"</td></tr
<tr><th align="left">Example Properties</th><td><ul><li><a href="./properties.md#opening_hours">Opening Hours</a></li><li><a href="./properties.md#operator">Operator</a></li><li><a href="./properties.md#name">Name</a></li><li><a href="./properties.md.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
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
        "amenity": "Library",
        "operator": "University of Jisc",
        "name": "The Harold Bishop Library",
        "opening_hours": "Mo-Su 08:00-23:00",
        "wheelchair": "limited"
      }
}
```

#### Open Street Map XML Example

```
<node id="-1" lat="51.517364" lon="-0.140043">
<tag k="amenity" v="Library"/>
<tag k="operator" v="University of Jisc"/>
<tag k="name" v="The Harold Bishop Library"/>
<tag k="opening_hours" v="Mo-Su 08:00-23:00"/>
<tag k="wheelchair" v="limited"/>
</node>
```

### Waste Disposal Unit

Medium sized waste bins should use the [amenity:waste_disposal](https://wiki.openstreetmap.org/wiki/Tag:amenity=waste_disposal) key pair.


<table>
<tr><th align="left">label</th><td>Waste Container</td></tr>
<tr><th align="left">Description</th><td>Container that holds waste</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q216530">Q216530</a></td></tr>
<tr><th align="left">Open Street Map Key Pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dwaste_disposal">amenity=waste_disposal</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"waste_disposal"</td></tr
<tr><th align="left">Example Properties</th><td><ul><li><a href="./properties.md.md#operator">Operator</a></li></ul> </td></tr>
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
        "amenity": "waste__disposal",
        "operator": "University of Jisc",

      }
}
```

#### Open Street Map XML Example

```
<node id="-1" lat="51.517364" lon="-0.140043">
<tag k="amenity" v="waste__disposal"/>
<tag k="operator" v="University of Jisc"/>
</node>
```

#### notes

- Smaller waste bins should use the [amenity=waste_basket](./items.md#waste_basket) entity

### Bins

Smaller sized waste bins should use the [amenity:waste_basket](https://wiki.openstreetmap.org/wiki/Tag:amenity=waste_basket) key pair.


<table>
<tr><th align="left">label</th><td>Waste Container</td></tr>
<tr><th align="left">Description</th><td>Container that holds waste</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q216530">Q216530</a></td></tr>
<tr><th align="left">Open Street Map Key Pair</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dwaste_basket">amenity=waste_basket</a></td></tr>
<tr><th align="left">Required key pair</th><td>"amenity":"waste_disposal"</td></tr
<tr><th align="left">Example Properties</th><td><ul><li><a href="./properties.md.md#waste">waste</a></li></ul> </td></tr>
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
        "amenity": "waste__disposal",
        "waste": "plastic",

      }
}
```

#### Open Street Map XML Example

```
<node id="-1" lat="51.517364" lon="-0.140043">
<tag k="amenity" v="waste__disposal"/>
<tag k="waste" v="plastic"/>
</node>
```

#### Notes

- Medium waste bins should use the [amenity=waste_disposal](./items.md#waste_disposal) entity


### Building

The building key can be used with most amenitys or if the user cannot find an appropriate amenity key pair, they may use the [building key](https://wiki.openstreetmap.org/wiki/Buildings) key pair. This follows the wide OSM definition of buildings to include other large outside items such as storage_tanks, static_caravans etc.

<table>
<tr><th align="left">label</th><td>Building</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:building"> building</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q41176">Q41176</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./properties.md#entrance">Entrance</a></li><li><a href="./properties.md.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
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

