# room
* [ROOM_ID](#room_id) [1] **
* [NAME](#name) [0..1]
* [SITE_ID](#site_id) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **room**

## Description of room entity
An identified space at a provider where scheduled events for module instances can occur. May or may not be a specific "room", for example may be a flexible learning space.

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

