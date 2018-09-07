# Features

For analytic purposes it may be useful to capture some additional features of rooms and sites to use as dimensions. 

Features are fixed properties of a location - or at least, slowly changing - that are not measured by sensors. Different systems are likely to capture a different range of room or site features; for example, BIMs are likely to have very detailed information on all fixtures, whereas timetable systems will tend to mostly maintain accessibility features and some fixtures related to teaching use.

* [FEATURE_NAME](#feature_name) 1
* [SITE_ID](#site_id) 1
* [ROOM_ID](#room_id) 0..1

## Example feature names

* DEAF_LOOP
* WHEELCHAIR_ACCESS
* SMARTBOARD
* PROJECTOR

## FEATURE_NAME
### Description
A human-readable label for the feature.

### Purpose
Display

### Valid Values
Any. See examples at top.

### Format
String (255)

### Notes

## SITE_ID
### Description
The site the feature belongs to.

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes

## ROOM_ID
### Description
The room the feature belongs to. 

### Purpose
To link relational database tables

### Valid Values
Any

### Format
String (255)

### Notes
If omitted, the feature applies to all rooms for the specified site.
