# layout

* [LAYOUT_ID](#layout_id) [1]
* [ROOM_ID](#room_id) [1]
• [NAME](#name) [1]
• [CAPACITY](#capacity) [0..1]

\** indicates that the property is the primary key for this entity.

API endpoint name: **layout**


## Description of layout entity
A configuration for a space, usually for a particular use such as lecture or exam, or for a particular style of use, such as "cabaret" or "forward facing", and with an associated capacity.

### Implementation Notes
* In Clocks/Scientia, this is equivalent to a _capacity_ tag on a _zone_
* In CELCAT, this is equivalent to a _layout_
