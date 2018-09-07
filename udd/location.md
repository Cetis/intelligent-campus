# location
* [LOCATION_ID](#location_id) [1] **
* [NAME](#name) [0..1]
* [TYPE](#type) [0..1]
* [OSM_NODE_ID](#osm_node_id) [0..1]
* [SITE_ID](#site_id) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **location**


## Description of location entity
An identified location at a provider, although not one where scheduled learning takes place. Examples include helpdesks, cycle racks, 
and other general location points around campus or within buildings. 

### Implementation Notes

### DEV NOTES

## LOCATION_ID
### Description
The identifier of the location as supplied by the provider, typically an identifier supplied from the 
timetable or building management system.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable label for the location.

### Purpose
Display

### Valid Values
Any

### Format
String (255)

### Notes

## TYPE
### Description
A human-readable type for the location.

### Purpose
Display

### Valid Values
Any

### Format
String (255)

### Notes
For example, "Helpdesk", "Bathroom", "Entrance", "Cycle rack"

## OSM_NODE_ID
### Description
The identifier for the location on Open Street Map as a Node (point).

### Purpose
Linking to mapping and wayfinding

### Valid Values
A valid OSM identifier, typically a 9-digit number.

### Format
64-bit Integer

### Notes
For example, the main entrance on level one to the Murray Building at the University of Southampton has the Node ID of 2505968634. 
See: https://www.openstreetmap.org/node/2505968634

## SITE_ID
### Description
The site the location belongs to.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

