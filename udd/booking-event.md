# Booking Event

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

API endpoint name: **booking**

## Description of booking entity

A booking links a Module Instance to a Room, and optionally a Layout for that room.

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
Date and Time when the booked event starts, in ISO8601 format.

## END_DATETIME
### Description
Date and Time when the booked event ends, in ISO8601 format.

## BOOKING_PERIOD
### Description
Period to which booking relates (e.g. semester 1)

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
Each different code value in EVENT_PERIOD should have a matching code value in period.PERIOD_CODE.

### Format
String (255)

### Notes
It is expected that sites / organisations will have their own code lists for BOOKING_PERIOD values.

## SPECIFIC_DATE
### Description
A single specified date to which the booking applies> Use this property if the event is a single non-recurring event, or the event source represents all events as  single events. 

### Format
W3C DateTime

### Derivation
CLOCKS/Scientia

## DAY_OF_WEEK
### Description
The day of the week to which the booking applies, if it is a recurring event. Where an event occurs on multiple days per week, use 
additional EVENT instances.

### Derivation
CELCAT

### Valid Values
Week days in lowercase; one of "monday","tuesday","wednesday","thursday","friday","saturday","sunday".

### Format
String (9)

### Notes
Where no day of week is given, and there is no SPECIFIC_DATE specified, the event is assumed to take place on all days within the period specified.

## WEEKS
### Description
The weeks of the period on which the event occurs, if it is a recurring event.

### Derivation
CELCAT

### Valid Values
A string of letters 'Y' and 'N' signifying whether the event applies in the week. For example: "YYYYYNNNYYYNNNY"

### Format
String (255)

### Notes
Where no values for WEEKS and SPECIFIC_DATE are provided, the booking is assumed to take place on all weeks within the period specified.



