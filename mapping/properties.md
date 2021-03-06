## Ontology entities
The intelligent campus ontology is an approach and not an exhaustive list. Properties map to popular OSM key pairs. This list documents popular entities and properties that may be implemented against them. To avoid mirroring the OSM documentation a list of popular entities with of OSM and geoJSON examples are kept here. Implementers may want to check there OSM documentation for other [key pairs](https://wiki.openstreetmap.org/wiki/Tags).


### Capacity

<table>
<tr><th align="left">label</th><td>Capacity</td></tr>
<tr><th align="left">Description</th><td>Capacity an entity is suitable for.</td></tr>
<tr><th align="left">Data Type</th><td>Integer</td></tr>
<tr><th align="left">Value Space</th><td>Any positive integer</td></tr>
<tr><th align="left">Example Space</th><td>450</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:capacity">Capacity</a></td></tr>
<tr><th align="left">Wikidata</th><td>None?</a> </td></tr>
</table>

### Entrance

<table>
<tr><th align="left">label</th><td> Entrance</td></tr>
<tr><th align="left">Description</th><td>The point where you can go into a building or enclosed area </td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>main,service,exit,emergency,staircase,other</td></tr>
<tr><th align="left">Example Space</th><td>main</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:entrance">Entrance</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q1137365">Q1137365</a> </td></tr>
</table>

### Opening_Hours

<table>
<tr><th align="left">label</th><td> Opening Hours</td></tr>
<tr><th align="left">Description</th><td>Opening hours of entity</td></tr>
<tr><th align="left">Data Type</th><td></td></tr>
<tr><th align="left">Value Space</th><td></td></tr>
<tr><th align="left">Example Space</th><td></td></tr>
<tr><th align="left">Open Street Map</th><td></td></tr>
</table>

### Operator

<table>
<tr><th align="left">label</th><td> Operator</td></tr>
<tr><th align="left">Description</th><td>Organisation that operates the facility or service</td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>Any string</td></tr>
<tr><th align="left">Example Space</th><td>University of Jisc</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:operator">Operator</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Property:P137">P137</a> </td></tr>
</table>

### Name

<table>
<tr><th align="left">label</th><td> Name</td></tr>
<tr><th align="left">Description</th><td> Noun that refers to entity</td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>Any string</td></tr>
<tr><th align="left">Example Value</th><td>Thompson Building</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:name">name</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q147276">Q147276</a> </td></tr>
</table>

### Waste

<table>
<tr><th align="left">label</th><td>Waste</td></tr>
<tr><th align="left">Description</th><td>Type of waste</td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>trash, oil, drugs, organic, plastic, rubble, dog_excrement, cigarettes</td></tr>
<tr><th align="left">Example Value</th><td>plastic</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:waste">ref</a></td></tr>
</table>


### Wheelchair_Accessibility

<table>
<tr><th align="left">label</th><td> Wheelchair Accessibility</td></tr>
<tr><th align="left">Description</th><td>Describes wheelchair accessibility of location or event </td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>yes, limited, no, designated</td></tr>
<tr><th align="left">Example Value</th><td>yes</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:wheelchair">wheelchair</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Property:P2846">P2846</a> </td></tr>
</table>
