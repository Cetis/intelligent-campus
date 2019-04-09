# zone
* [ZONE_ID](#zone_id) [1] **
* [NAME](#name) [0..1]
* [TYPE](#type) [0..1]
* [OSM_WAY_ID](#osm_way_id) [0..1]
* [ROOM_ID](#room_id) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **location**


## Description of zone entity
An area within a room at a provider that is logically distinct either for sensor reading purposes, or by function. Examples include open 
plan offices separated into fixed desks and hot desking zones, and flexible open plan areas in schools separated into lobby, cafe and 
study zones

### Implementation Notes

### DEV NOTES

## ZONE_ID
### Description
The identifier of the zone as supplied by the provider, typically an identifier supplied from the 
facilities management system.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable label for the zone.

### Purpose
Display

### Valid Values
Any

### Format
String (255)

### Notes

## TYPE
### Description
A human-readable type for the zone.

### Purpose
Display

### Valid Values
Any

### Format
String (255)

### Notes
For example, "Entrance", "Study Area", "Casual Seating Area"

## OSM_WAY_ID
### Description
The identifier for the zone on Open Street Map as a Way (polygon).

### Purpose
Linking to mapping and wayfinding

### Valid Values
A valid OSM identifier, typically a 9-digit number.

### Format
64-bit Integer

### Notes

## ROOM_ID
### Description
The room the zone belongs to.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

