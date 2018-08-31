# event
* [EVENT_ID](#event_id) [1] **
* [NAME](#name) [0..1]
* [ROOM_ID](#room_id) [1]
* [MOD_INSTANCE_ID](#mod_instance_id) [1]
* [REQUESTED_CAPACITY](#requested_capacity) [0..1]
* [START_TIME](#start_time) [1]
* [END_TIME](#end_time) [1]
* [SPECIFIC_DATE](#specific_date) [0..1]
* [DAY_OF_WEEK](#day_of_week) [0..1]
* [WEEKS](#weeks) [0..1]
* [EVENT_PERIOD](#event_period) [1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **event**

## Description of event entity

An event links a Module Instance to a Room.

### Implementation Notes

* In Scientia/Clocks this is equivalent to _booking_
* In CELCAT this is equivlant to _event_

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

## REQUESTED_CAPACITY
### Description
The capacity used for booking the event. Usually this is the number of people expected in this event

### Purpose
Analytics

### Derivation
CLOCKS/Scientia

### Format
Integer

## START_TIME
### Description
Time when the event starts, in HH:MM format.

## END_TIME
### Description
Time when the event ends, in HH:MM format.

## EVENT_PERIOD
### Description
Period to which event relates (e.g. semester 1)

### Purpose
Analytics

### Derivation
Jisc

### Valid Values
Each different code value in EVENT_PERIOD should have a matching code value in period.PERIOD_CODE.

### Format
String (255)

### Notes
It is expected that sites / organisations will have their own code lists for EVENT_PERIOD values.

## SPECIFIC_DATE
### Description
A single specified date to which the event applies> Use this property if the event is a single non-recurring event, or the event source represents all events as  single events. 

### Format
W3C DateTime

### Derivation
CLOCKS/Scientia

## DAY_OF_WEEK
### Description
The day of the week to which the event applies, if it is a recurring event. Where an event occurs on multiple days per week, use 
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
Where no values for WEEKS and SPECIFIC_DATE are provided, the event is assumed to take place on all weeks within the period specified.



