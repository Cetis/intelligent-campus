# room
* [ROOM_ID](#room_id) [1] **
* [NAME](#name) [0..1]
* [OSM_WAY_ID](#osm_way_id) [0..1]
* [SITE_ID](#site_id) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **room**


## Description of room entity
An identified space at a provider, particularly if it can be used for scheduled learning events. 

For an item or a location that is not a room as such, such as a helpdesk or an entrance, use the Location entity instead.

May or may not be a specific "room", for example may be a flexible learning space. 

### Implementation Notes
* In Clocks/Scientia, this is equivalent to a _zone_
* In CELCAT, this is equivalent to a _room_

### DEV NOTES
* Consider renaming to "space".
* Consider adding optional lat/long attributes 
* Consider adding optional capacity value

## ROOM_ID
### Description
The identifier of the room as supplied by the provider, typically an identifier supplied from the timetable or building management system.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable label for the room.

### Purpose
Display

### Valid Values
Any

### Format
String (255)

### Notes

## OSM_WAY_ID
### Description
The identifier for the room on Open Street Map as a Way (shape).

### Purpose
Linking to mapping and wayfinding

### Valid Values
A valid OSM identifier, typically a 9-digit number.

### Format
64-bit Integer

### Notes
For example, room 58-1049 in the Murray Building at the University of Southampton has the Way ID of 243169186. See: https://www.openstreetmap.org/way/243169186

## SITE_ID
### Description
The site the room belongs to.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

