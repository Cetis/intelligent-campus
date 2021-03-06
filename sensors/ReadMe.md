NOTE THIS IS A WORKING DRAFT

# Sensors

This is a data model for recording various types of environmental data from a wide variety of sensors. The current draft is based on Safehouse data from Jisc, so it is highly likely that changes will have to be made to incorporate other sensor data. The [model](measurement_event.md) follows the form of the more volatile "activity data" in the xAPI part of the Learning Data Hub, rather than the more static UDD data.

## How the Sensor data links with the UDD data and with the Learning Data Hub

The sensor data contains not only the data relating to the measured values and the sensors, but also linking data that relates to the geographical location of the sensor, for example Room_ID, Site_ID or Location_ID. Linking in this way means that the sensor data can be related to timetabled and other events within identified modules and courses, located via timetabling and booking systems. See [Intelligent Campus UDD Extension](https://github.com/Cetis/intelligent-campus/blob/master/udd/README.md) for a more detailed explanation and examples of how it might link in to the Learning Data Hub.

## Definitions

We have based our definitions of terms on the [OGC SensorML encoding standard, OGC 12-000](https://portal.opengeospatial.org/files/?artifact_id=55939). Relevant definitions, slightly simplified from the original, are:

- *Context*: A Measurement has a location, time, frequency and way of transmitting the data to a collecting system. This is Context. A Context effectively binds a measurement value to a location, to a sensor and to data transmission.
- *Detector*: A single part of a Measurement System defining sampling and response characteristics of a detection device. A Detector has only 1 input and 1 output, both being scalar quantities. A Detector senses 1 type of measurement. A Sensor may contain several Detectors. Data is transmitted at Sensor level, a Detector is not separately identified.
- *Measure* (noun): A value described using a scale of an appropriate type (may be numerical, boolean or string). _This definition is now different from the OGC one, which uses a numerical scale only._
- *Measurement* (verb): An instance of estimating the value of a natural phenomenon involving a Detector or Sensor. A Measurement also has a Location, Timestamp, and reference to the Method used to determine the value.  
- *Observation*: Act of observing phenomenon, where the goal is to measure, estimate or otherwise determine the value of a property.
- *Sensor*: An entity capable of observing phenomena and returning observed values. A Sensor may contain several Detectors.
- *Value*: An observed value describing a phenomenon, which may use one of a variety of scales.

Note: we use the term Context as a synonym for SensorML's term Measurement Feature.
