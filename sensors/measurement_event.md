# Environmental Sensing

## Definitions

For this specification, we have based our definitions of terms on the OGC SensorML encoding standard (OGC 12-000; https://portal.opengeospatial.org/files/?artifact_id=55939). Relevant definitions, slightly simplified from the original, are:

- *Context*: A Measurement has a location, time, and reference to the method used to determine the value. This is Context. A Context effectively binds a value to a location and to a method, detector or sensor.
- *Detector*: A single part of a Measurement System defining sampling and response characteristics of a detection device. A detector has only 1 input and 1 output, both being scalar quantities. A detector senses 1 type of measurement. A sensor may contain several detectors.
- *Measure* (noun): A value described using a numerical scale. Measure is a synonym for physical quantity.
- *Measurement* (verb): An instance of estimating the value of a natural phenomenon involving a detector or sensor. A measurement also has a location, time, and reference to the method used to determine the value - See Context.  
- *Observation*: Act of observing phenomenon, where the goal is to measure, estimate or otherwise determine the value of a property.
- *Sensor*: An entity capable of observing a phenomenon and returning an observed value.
- *Value*: An observed value describing a phenomenon, which may use one of a variety of scales.

Note: we use the term Context as a synonym for SensorML's term Measurement Feature.

## Purpose

This draft specification describes the structure, entities and properties to record a Measurement taken by a Detector in a specific Context. It is expected that these data records will be collected by a system that will relate the data to other information, such as timetables and student activities.

This specification is for the collection of data for the use in Intelligent Campus systems. It does not define specific data output by any actual type of sensor, but instead the target data format to be used, typically by mapping real world data to it.


# DEV NOTES

- Consider splitting Context into components such as Location, Timestamp, and so on.
- Consider whether UDD or XAPI style is preferable (XAPI style adopted here).
- This is based on Safehouse. Others need to be compared.


# Measurement_Event
## Description
A single instance of a particular type of Measurement taken by a Detector within a given Context (at a specific point in space and at a specific moment in time through a defined method). A Measurement_Event consists of the Measurement itself, its Detector and its Context.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>measurement_event</td>
		<td>As above</td>
		<td>JSON Object containing Measurement, Context and Detector</td>
		<td></td>
	</tr>
</table>

# Measurement Entity

## Description
An instance of estimating the value of a natural phenomenon involving a detector or sensor.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>measurement.id [1]</td>
		<td>Uniquely identifies the measurement instance.</td>
		<td>string</td>
		<td>If we use a composite primary key, for example, this may optional?</td>
	</tr>
	<tr>
		<td>measurement.value</td>
		<td>The observed value describing the phenomenon</td>
		<td>Numeric value</td>
		<td></td>
	</tr>
	<tr>
		<td>measurement.scale_name</td>
		<td>Label for the commonly-used name of the scale of values (for example, Celsius)</td>
		<td>string</td>
		<td></td>
	</tr>
	<tr>
		<td>measurement.range</td>
		<td></td>
		<td></td>
		<td>Consider using something like our result.score in XAPI</td>
	</tr>
</table>


# Context Entity
### Description
Describes the location, measurement type and method used by the Detector. Necessary because a single Detector may provide multiple types of data and use variable methods. May include a timestamp that applies to all the data in the event, so timestamp is included in this entity.


<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>context.id [1]</td>
		<td>Identifier for this Context. Applies to the delivery of a particular Sensor payload, which may include several Measurement_event items. If there is only 1 data item, Context may be a 1:1 mapping to Measurement_events.</td>
		<td>string</td>
		<td>This is currently derived from Safehouse data supplied by Jisc.</td>
	</tr>
	<tr>
		<td>context.timestamp [1]</td>
		<td>Date and time the Measurement was taken.</td>
		<td>YYYY-MM-DDThh:mm:ss.sssZ</td>
		<td>Might some sensors record timestamp of measurement and timestamp of transmission? Would we need both?</td>
	</tr>
	<tr>
		<td>context.location [1]</td>
		<td>Information about the physical location of the Detector, typically a room</td>
		<td>JSON object</td>
 		<td>Presume mandatory but business rules to determine content.</td>
	</tr>
	<tr>
		<td>context.location.room_id [0..1]</td>
		<td>The identifier of the room as supplied by the provider, typically an identifier supplied from the timetable or building management system.</td>
		<td>string (255)</td>
 		<td>Uses room entity in IntCamp.UDD.</td>
	</tr>	
	<tr>
		<td>context.location.site_id [0..1]</td>
		<td>The identifier of the site as supplied by the provider, typically an identifier supplied from the timetable or building management system.</td>
		<td>string (255)</td>
 		<td>Uses site entity in IntCamp.UDD.</td>
	</tr>
	<tr>
		<td>context.location.geoJSON [0..1]</td>
		<td>An optional geoJSON Object with geolocation details for the sensor (see Example)</td>
		<td>geoJSON Object</td>
		<td>Follows Jisc xapi context.extensions.devicelocation.</td>
	</tr>
	<tr>
		<td>context.method [0..1]</td>
		<td>Describes the way in which the Detector detects the measure, for example, Wifi positioning by signal strength, Bluetooth, Thermometer, and so on.</td>
		<td>JSON Object</td>
		<td></td>
	</tr>
	<tr>
		<td>context.method.type [0..1]</td>
		<td>Describes the method with a commonly-used term from a controlled list.</td>
		<td>Vocabulary term from ontology of method types</td>
		<td>This could use a locally controlled list, not one controlled centrally, in much the same way as for subType extensions in Jisc xAPI.</td>
	</tr>
	<tr>
		<td>context.method.event_frequency [0..1]</td>
		<td>Describes how often the sensor records the measurement.</td>
		<td>string</td>
		<td>Called event_frequency to avoid confusion with wavelenght frequency.</td>
	</tr>
	<tr>
		<td>context.method.transmission</td>
		<td>Describes how the recorded data is sent to the collecting system at the provider.</td>
		<td>string</td>
		<td>For example, WiFi, Bluetooth, email. Not sure if this is useful?</td>
	</tr>
 </table>


# Sensor Entity
## Description
Identifies and describes the particular equipment used for the environmental sensing event. This entity is mandatory for the measurement_event statement.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>sensor.id [1]</td>
		<td>The provider's own ID for the sensor</td>
		<td>string</td>
		<td></td>
	</tr>
	<tr>
		<td>sensor.mac [0..1]</td>
		<td>MAC address of sensor</td>
		<td>Mac address format: this could be 48-bit or 64-bit hexadecimal or formated to traditional nn:nn:nn:nn:nn:nn or nn:nn:nn:nn:nn:nn:nn:nn.</td>
		<td>Should we specify? I think we leave it to the provider.</td>
	</tr>
	<tr>
		<td>sensor.ip-address [0..1]</td>
		<td>Sensor's IP address</td>
		<td>ip address</td>
 		<td>Could be IPv4 or IPv6.</td>
	</tr>
	<tr>
		<td>sensor.name [0..1]</td>
		<td>Human-readable label for the sensor</td>
		<td>string</td>
 		<td>Useful or not?</td>
	</tr>
	<tr>
		<td>sensor.type [0..1]</td>
		<td>Label for model and / or make of sensor</td>
		<td>string</td>
		<td></td>
	</tr>	
 </table>

## JSON Example

``` javascript
	"sensor": {
		"id": "15",
		"mac": "008000000000ba34",
		"ip-address: "34.248.41.184",
		"name": "safehouse:test",
		"type": "safehouse"
	}
```




	<tr>
		<td></td>
		<td></td>
		<td></td>
		<td></td>
	</tr>
