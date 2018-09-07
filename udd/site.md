# site
* [SITE_ID](#site_id) [1] **
* [NAME](#name) [0..1]
* [TYPE](#type) [0..1]
* [PARENT_SITE_ID](#parent_site_id) [0..1]
* [OSM_WAY_ID](#osm_way_id) [0..1]
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

## TYPE
### Description
A human-readable label for the type of site.

### Purpose
Display

### Valid Values
Any. Examples include "Campus", "Building", "Floor"

### Format
String (255)

## OSM_WAY_ID
### Description
The identifier for the site on Open Street Map as a Way (shape).

### Purpose
Linking to mapping and wayfinding

### Valid Values
A valid OSM identifier, typically a 9-digit number.

### Format
64-bit Integer

### Notes
For example, the Humanities building on Bridgeford Street for the University of Manchester has the Way ID of 32605011. See: https://www.openstreetmap.org/way/32605011

## PARENT_SITE_ID
### Description
The site the current site is a part of, for systems that provides a hierarchy of sites (campus, building, floor)

### Purpose
Relational

### Valid Values
Any.

### Format
String (255)
