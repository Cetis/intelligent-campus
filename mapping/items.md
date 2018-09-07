
## Ontology

### University
<table>
<tr><th align="left">label</th><td>University</td></tr>
<tr><th align="left">Description</th><td>Academic institution for further education</td></tr>
<tr><th align="left">Open Street Map Tag</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity">amenity=university</a></td></tr>
<tr><th align="left">GeoJSON property key pair</th><td>"amenity" "university"</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#capacity">Capacity</a></li><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>


### Building
<table>
<tr><th align="left">label</th><td>Building</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:building"> building</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q41176">Q41176</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>



### ATM
<table>
<tr><th align="left">label</th><td>ATM</td></tr>
<tr><th align="left">Description</th><td>An automated teller machine (ATM)</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Datm"> amenity=atm</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q81235">Q81235</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./properties#lon">Lon</a></li><li><a href="./properties#lon">Lat</a></li><li><a href="./properties#operator">Operator</a></li><li><a href="./properties#reference">Reference</a></li></td></tr>
</table>




#### Item Definition

```
  atm[0]
    lon = -0.140043
    lat = 51.5173639
    Operator = University of Jisc
    Reference = ATM1
```

#### JSON


``` Javascript
{
  "atm": [
    {
      "lon": "-0.140043",
      "lat": "51.5173639",
      "Operator": "University of Jisc",
      "Reference": "ATM1"
    }
  ]
}
```

#### Open Street Map Example

```
<node lat="51.5173639" lon="-0.140043">
    <tag k="amenity" v="atm"/>
    <tag k="Operator" v="University of Jisc"/>
    <tag k="Reference" v="ATM1"/>
</node>
```

### Building
<table>
<tr><th align="left">label</th><td>Building</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:building"> building</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q41176">Q41176</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Catering
<table>
<tr><th align="left">label</th><td>Catering</td></tr>
<tr><th align="left">Description</th><td>Food service</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Drestaurant"> amenity=restaurant</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q777754">Q777754</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#capacity">Capacity</a></l1><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Defibrillator (need a higherlevel entity for things like this)

### Library
<table>
<tr><th align="left">label</th><td>Library</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dlibrary"> amenity=library</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q13226383">Q13226383</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Parking
<table>
<tr><th align="left">label</th><td>Parking</td></tr>
<tr><th align="left">Description</th><td>Area that is intended for parking vehicles</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dparking"> amenity=parking</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q6501349">Q6501349</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#capacity">Capacity</a><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Place of Worship
<table>
<tr><th align="left">label</th><td>Place of Worship</td></tr>
<tr><th align="left">Description</th><td>Specially designed structure or consecrated space for use in worshipping</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dplace_of_worship"> amenity=place_of_worship</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q1370598">Q1370598</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#capacity">Capacity</a><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>





### Laboratory 
<table>
<tr><th align="left">label</th><td>Laboratory</td></tr>
<tr><th align="left">Description</th><td>Facility that provides controlled conditions or equipment</td></tr>
<tr><th align="left">Open Street Map</th><td>?</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#capacity">Capacity</a></li><li><a href="./items.md#entrance">Entrance</a></li><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li><li><a href="./items.md#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Waste_container

<table>
<tr><th align="left">label</th><td>Waste Container</td></tr>
<tr><th align="left">Description</th><td>Container that holds waste</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dwaste_disposal">amenity=disposal</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q216530">Q216530</a></td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./items.md#operator">Operator</a></li><li><a href="./items.md#name">Name</a></li><li><a href="./items.md#reference">Reference</a></li></ul> </td></tr>
</table>
