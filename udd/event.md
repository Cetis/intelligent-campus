# event
* [EVENT_ID](#event_id) [1] **
* [NAME](#name) [0..1]
* [ROOM_ID](#room_id) [1]
* [MODULE_INSTANCE_ID](#module_instance_id) [1]
* [START_TIME](#start_time) [1]
* [END_TIME](#end_time) [1]
* [DAY_OF_WEEK](#day_of_week) [0..1]
* [WEEKS](#weeks) [0..1]
* [PERIOD](#period) [1]
* [PROVIDED_AT](#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **event**

## Description of event entity

An event links a Module Instance to a Room.

## Notes
An event is an abstraction of a timetabling entry for a module instance. This specification is derived from the APIs of the
CELCAT and Syllabus Plus solutions typically used for timetabling by UK providers.

## EVENT_ID
### Description
The provider's own ID for the event

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable name for the event

### Purpose
For display purposes

### Derivation
Jisc

### Valid Value
Any

### Format
String (255)

### Notes

## ROOM_ID
### Description
A link to the Room entity for this event.

### Purpose
To link relational database tables

### Derivation
Jisc

### Valid Value
Any

### Format
String (255)

### Notes

## MOD_INSTANCE_ID
### Description
A link to the Module Instance entity for this event.

### Purpose
To link relational database tables

### Derivation
Jisc

### Valid Value
Any

### Format
String (255)

### Notes
