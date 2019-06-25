# Booking_Event

* [BOOKING_EVENT_ID](#booking_event_id) [1] **
* [BOOKING_ID](#booking_id) [0..1]
* [NAME](#name) [0..1]
* [ROOM_ID](#room_id) [1]
* [LAYOUT_ID](#layout_id) [0..1]
* [MOD_INSTANCE_ID](#mod_instance_id) [1]
* [REQUESTED_CAPACITY](#requested_capacity) [0..1]
* [START_DATETIME](#start_datetime) [1]
* [END_DATETIME](#end_datetime) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **booking_event**

## Description of booking entity

A Booking Event links a Module Instance to a Room, and optionally a Layout for that room. A Booking Event may be derived from a Booking that contains the metadata relating to a recurring or block booking.

### Implementation Notes

* In Scientia/Clocks this is equivalent to _booking_
* In CELCAT this is equivlant to _event_

## Notes
A booking is an abstraction of a timetabling entry for a module instance. This specification is derived from the APIs of the
CELCAT and Syllabus Plus solutions typically used for timetabling by UK providers.

## BOOKING_EVENT_ID
## Description
The provider's own ID for the booking event

## BOOKING_ID
### Description
The provider's own ID for the booking; used to link an booking_event to a booking

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable name for the booking

### Purpose
For display purposes

### Derivation
Jisc

### Valid Value
Any

### Format
String (255)

### Notes

## LAYOUT_ID
### Description
A link to the room layout used for the event.

### Purpose
To link relational database tables

### Derivation
CELCAT

### Valid Value
Any

### Format
String (255)

## ROOM_ID
### Description
A link to the Room entity for this booking.

### Purpose
To link relational database tables

### Derivation
CELCAT/Scientia

### Valid Value
Any

### Format
String (255)

### Notes

## MOD_INSTANCE_ID
### Description
A link to the Module Instance entity for this booking.

### Purpose
To link relational database tables

### Derivation
Jisc

### Valid Value
Any

### Format
String (255)

### Notes

## REQUESTED_CAPACITY
### Description
The capacity used for booking the booking. Usually this is the number of people expected in this booking

### Purpose
Analytics

### Derivation
CLOCKS/Scientia

### Format
Integer

## START_DATETIME
### Description
Date and Time when the booked event starts, in W3C DateTime format.

### Format
W3C DateTime

## END_DATETIME
### Description
Date and Time when the booked event ends, in W3C DateTime format.

### Format
W3C DateTime


