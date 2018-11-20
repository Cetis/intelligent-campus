_NOTE THIS IS A WORKING DRAFT_

# Intelligent Campus UDD Extension

This is the data model for the Intelligent Campus UDD Extension. This is a set of classes that extends the UDD for Learning Analytics 
to include concepts related to the Intelligent Campus.

Specifically, the classes enable different kinds of sensor events to be related to stable entities relating to sites, rooms and bookings.

## How the UDD is used with sensor events

When a sensor event occurs, it will contain a set of context identifiers. These related to UDD entities, both in the original LA UDD model and also in the IC extension. 

For example, the snippet below is an event where both the room where the measurement took place, and the module instance for which
the room was being used have been included in the sensor event context:

~~~~
{
  "context": {
    "room_id": "58-1204",
    "mod_instance_id": "CPU4000-2018-4",
    "timestamp": "2018-01-08:12:00:00Z"
  }
}
~~~~

Another example, this time for a sensor not related to a teaching activity and recorded at a generic location rather than a room:

~~~~
{
  "context": {
    "location_id": "61204",
    "timestamp": "2018-01-08:12:00:00Z"
  }
}
~~~~

An example where the student and location have been identified, e.g. by a student RFID card used to access an information kiosk.

~~~~
{
  "context": {
    "location_id": "61204",
    "student_id": "91374125",
    "timestamp": "2018-01-08:12:00:00Z"
  }
}
~~~~

An example with very limited context, for example a report from a building management system for a whole building.

~~~~
{
  "context": {
    "site_id": "Middleton_1",
    "timestamp": "2018-01-08:12:00:00Z"
  }
}
~~~~

In some cases, sensors may not correlate with any UDD entities:

~~~~
{
  "context": {
    "coordinates": [51.510531, -0.118930],
    "timestamp": "2018-01-08:12:00:00Z"
  }
}
~~~~

## Relating event contexts to UDD entities

There are two main ways you can connect events to the UDD:

### 1: Events connected at source

In some implementations, sensor events will be connected directly with UDD entities at source, through integration of applications.

For example, a sensor event may contain references to ROOM_ID, STUDENT_ID, and MOD_INSTANCE_ID.

### 2: Events connected in the Data Warehouse

In some implementations, sensor events need to be connected within the warehouse.

For example, a sensor event may only contain references to ROOM_ID and a timestamp. However, the event can then be related to a collection of students through correlating the BOOKING via the room and timeframe, and from the BOOKING entity locate the relevent MOD_INSTANCE.

~~~~
"context": {
  "room_id": "58-1204",
  "timestamp": "2018-01-08:12:00:00Z"
}
~~~~

