# HE Service Point Mapping Ontology 

## Development notes and idea

- I have really struggled to work out what to do in the time, a full machine readable ontology isn't really a days job nor should it be, settled on a human readable stab of used Service Points
- This should be the repo and not the wiki as it is sucject to change/ evolving ontology
- There is no quick win in implementing OSM, Southampton's approach is not  
- Ontology is split into properties and items, properties can relate to OSM keys and items can related to tags (keys and values), this also maps onto wikidata's use of entitys
- Cambridge spent a lot of time in this space and I am following a lot of their best practices to build the ontology
- Currently it is just in tables, what should a machine readable format look like? Is it even sustainable in tables.


### Universities using OSM

<table>
<tr><th>University</th><th>University Page</th><th>Additional Information</th></tr>
<tr><td>University of Cambridge</td><td><a href="http://map.cam.ac.uk/">http://map.cam.ac.uk/</a></td><td><a href="https://wiki.openstreetmap.org/wiki/Cambridge/University_of_Cambridge">Open Street Map Wiki</a></td></tr>
<tr><td>University of Leicester</td><td><a href="https://www.le.ac.uk/maps/">https://www.le.ac.uk/maps/</a></td><td></td></tr>
<tr><td>University of Oxford</td><td><a href="http://maps.ox.ac.uk">http://maps.ox.ac.uk </a></td><td></td></tr>
<tr><td>University of Southampton</td><td><a href="http://maps.southampton.ac.uk">http://maps.southampton.ac.uk </a></td><td><a href="https://wiki.openstreetmap.org/wiki/University_of_Southampton">Open Street Map Wiki</a></td></tr>
</table>


# Table of Contents
*	1.0	Point of Service Entities
    *	1.1	[Items](./Mapping-ontology#items)
	*	1.2 [Properties](./Mapping-ontology#properties)

## Rationale
The HE service point ontology is based upon [OpenStreetMap tags](https://wiki.openstreetmap.org/wiki/Tags) and where possible a link to an Open Street Map key (typically for properties in the vocab) OR key:value pair (typically for items in the vocab) will be supplied. Where there is no suitable Open Street Map key or keypair pair, a wikidata entry will be provided.


## Items

### ATM
<table>
<tr><th align="left">label</th><td>ATM</td></tr>
<tr><th align="left">Description</th><td>An automated teller machine (ATM)</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Datm"> amenity=atm</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q81235">Q81235</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontology#reference">Reference</a></li></td></tr>
</table>

### Building
<table>
<tr><th align="left">label</th><td>Building</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:building"> building</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q41176">Q41176</a> </td></tr>
<tr><th align="left">Properties</th><td><ul><li><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontology#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Catering
<table>
<tr><th align="left">label</th><td>Catering</td></tr>
<tr><th align="left">Description</th><td>Food service</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Drestaurant"> amenity=restaurant</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q777754">Q777754</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#capacity">Capacity</a></l1><li><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontology#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Defibrillator (need a higherlevel entity for things like this)

### Library
<table>
<tr><th align="left">label</th><td>Library</td></tr>
<tr><th align="left">Description</th><td>Organised collection of resources</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dlibrary"> amenity=library</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q13226383">Q13226383</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Parking
<table>
<tr><th align="left">label</th><td>Parking</td></tr>
<tr><th align="left">Description</th><td>Area that is intended for parking vehicles</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dparking"> amenity=parking</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q6501349">Q6501349</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#capacity">Capacity</a><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Place of Worship
<table>
<tr><th align="left">label</th><td>Place of Worship</td></tr>
<tr><th align="left">Description</th><td>Specially designed structure or consecrated space for use in worshipping</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dplace_of_worship"> amenity=place_of_worship</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q1370598">Q1370598</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#capacity">Capacity</a><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>


### University
<table>
<tr><th align="left">label</th><td>University</td></tr>
<tr><th align="left">Description</th><td>Academic institution for further education</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Duniversity">amenity=university</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#capacity">Capacity</a></li><li><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>


### Laboratory 
<table>
<tr><th align="left">label</th><td>Laboratory</td></tr>
<tr><th align="left">Description</th><td>Facility that provides controlled conditions or equipment</td></tr>
<tr><th align="left">Open Street Map</th><td>?</td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q3918">Q3918</a> </td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#capacity">Capacity</a></li><li><a href="./Mapping-ontology#entrance">Entrance</a></li><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li><li><a href="./Mapping-ontology#wheelchair">Wheelchair</a></li></ul> </td></tr>
</table>

### Waste_container

<table>
<tr><th align="left">label</th><td>Waste Container</td></tr>
<tr><th align="left">Description</th><td>Container that holds waste</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Tag:amenity%3Dwaste_disposal">amenity=disposal</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q216530">Q216530</a></td></tr>
<tr><th align="left">Releated Properties</th><td><ul><li><a href="./Mapping-ontology#operator">Operator</a></li><li><a href="./Mapping-ontologymd#name">Name</a></li><li><a href="./Mapping-ontologymd#reference">Reference</a></li></ul> </td></tr>
</table>

## Properties

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
<tr><th align="left">Wikidata</th><td>None</a> </td></tr>
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

### Reference

<table>
<tr><th align="left">label</th><td>ref</td></tr>
<tr><th align="left">Description</th><td>Reference number or code</td></tr>
<tr><th align="left">Data Type</th><td>String</td></tr>
<tr><th align="left">Value Space</th><td>Any string</td></tr>
<tr><th align="left">Example Value</th><td>1</td></tr>
<tr><th align="left">Open Street Map</th><td><a href="https://wiki.openstreetmap.org/wiki/Key:ref">ref</a></td></tr>
<tr><th align="left">Wikidata</th><td> <a href="https://www.wikidata.org/wiki/Q1334113">Q1334113</a> </td></tr>
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
