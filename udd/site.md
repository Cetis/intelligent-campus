# site
* [SITE_ID](#site_id) [1] **
* [NAME](#name) [0..1]
* [PROVIDED_AT](https://github.com/jiscdev/analytics-udd/blob/master/udd/assessment_instance.md#provided_at) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **site**

## Description of site entity

An identified location at the institution that collects together multiple 'rooms'; typically though not always a building; 
this can also be a designated area within a building or building cluster.

### Implementation notes
* In Clocks/Scientia, this is equivalent to _building_
* In CELCAT, this is equivalent to _site_

### DEV NOTES
* Consider adding a PARENT_SITE_ID reference for nesting sites, e.g. campus > building > floor. CELCAT only has site (which can be anything) as a parent for a room; CLOCKS has the concept of campus, building, floor, and zone in a hierarchy.
* Consider adding optional type attribute e.g. building, zone, floor, other...
* Consider adding optional lat/long attributes
* Consider adding optional bounding box attributes
* Consider adding tenant_id reference for provider

## SITE_ID
### Description
The identifier of the site as supplied by the provider, typically an identifier supplied from the timetable or building management system.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## NAME
### Description
A human-readable label for the site.

### Purpose
Display

### Valid Values
Any
