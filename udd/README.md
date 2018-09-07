# Intelligent Campus UDD Extension

This the data model for the Intelligent Campus UDD Extension. This is a set of classes that extends the UDD for Learning Analytics 
to include concepts related to the Intelligent Campus.

Specifically, the classes enable different kinds of sensor events to be related to stable entities relating to sites, rooms and bookings.

There are two main uses of the UDD:

## 1: Events connected at source

In some implementations, sensor events will be connected directly with UDD entities at source, through integration of applications.

For example, a sensor event may contain references to ROOM_ID, STUDENT_ID, and MOD_INSTANCE_ID.

## 2: Events connected in the Data Warehouse

In some implementations, sensor events need to be connected within the warehouse.

For example, a sensor event may only contain references to ROOM_ID and a timestamp, 
which can then be related to a collection of students via the BOOKING and MODULT_INSTANCE entities.

