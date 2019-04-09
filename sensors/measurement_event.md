# Measurement Event

## Purpose

This draft specification describes the structure, entities and properties to record Measurements taken by a Sensor in a specific Context. It is expected that these data records will be collected by a system that will relate the data to other information, such as timetables and student activities.

This specification is for the collection of data for the use in Intelligent Campus systems. It does not define specific data output by any actual type of sensor, but instead the target data format to be used, typically by mapping real world data to it.

# DEV NOTES

- Consider whether UDD or XAPI style is preferable (XAPI style adopted here).
- This is based on Safehouse. Others need to be compared.
- Consider latency. May prefer averages over time (eg average temp over an hour). For limiting data stream. So, time period rather than point in time. Big architecture implications for a Jisc service. This spec now revised to cover the possibility of time ranges or averages over time.
- Potential issue over averages: do we need to know the time period (eg average temp over an hour), or should we leave that detail to the provider? I favour the latter.
- Consider a measurement.range property, to show possible or likely ranges of values?
- Suggestion: add measurement.type property for type of reading, for example "temperature", "humidity", and so on. Currently, this can be inferred from method, but it is almost certainly better to include this explicitly.

# Measurement_Event
## Description

See https://github.com/Cetis/intelligent-campus/blob/master/sensors/measurements%20E-R%20diagram.png.

A single instance of a particular type of Measurement taken by a Sensor within a given Context (at a specific point in space and at a specific moment in time or time range through a defined method). A Measurement_Event consists of the Measurement itself, its Sensor and its Context. A Measurement_Event may cover a range of real world data instances, for example a mid-point of a highest and lowest value over a time period, or an average of a series of data points. This may be important to reduce the volume of data transferred.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>measurement_event</td>
		<td>As above</td>
		<td>JSON Object containing Context, Measurement and Sensor</td>
		<td></td>
	</tr>
</table>

## Context Entity
### Description
Describes the Location, Timestamp, Frequency and Transmission Method used by the Sensor. Necessary because a single Sensor may provide multiple types of data within a single payload.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>context.event_frequency [0..1]</td>
		<td>Describes how often the Sensor records the measurement.</td>
		<td>string</td>
		<td>Called event_frequency to avoid confusion with wavelenght frequency.</td>
	</tr>
	<tr>
		<td>context.id [1]</td>
		<td>Identifier for this Context. Applies to the delivery of a particular Sensor payload, which may include several Measurement_event items. If there is only 1 data item, Context may be a 1:1 mapping to Measurement_events.</td>
		<td>string</td>
		<td>This is currently derived from Safehouse data supplied by Jisc.</td>
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
		<td>context.location.sensorLocation [0..1]</td>
		<td>An optional geoJSON Object with geolocation details for the sensor (see Example)</td>
		<td>geoJSON Object</td>
		<td>Follows Jisc xapi context.extensions.devicelocation.</td>
	</tr>
	<tr>
		<td>context.location.site_id [0..1]</td>
		<td>The identifier of the site as supplied by the provider, typically an identifier supplied from the timetable or building management system.</td>
		<td>string (255)</td>
 		<td>Uses site entity in IntCamp.UDD.</td>
	</tr>
	<tr>
		<td>context.timestamp [1]</td>
		<td>Date and time the Measurement was taken.</td>
		<td>YYYY-MM-DDThh:mm:ss.sssZ</td>
		<td>Might some sensors record timestamp of measurement and timestamp of transmission? Would we need both? In addition, if a range of values is used, we should take whatever relevant timestamp is available.</td>
	</tr>
	<tr>
		<td>context.transmission [0..1]</td>
		<td>Describes how the recorded data is sent to the collecting system at the provider.</td>
		<td>string</td>
		<td>For example, WiFi, Bluetooth, email. Not sure if this is useful?</td>
	</tr>
 </table>

## Measurement Entity
### Description
An estimate of the value of a natural phenomenon involving a sensor.

<table>
	<tr><th>Property [cardinality]</th><th>Description</th><th>Value information</th><th>Notes</th></tr>
	<tr>
		<td>measurement.id [1]</td>
		<td>Uniquely identifies the measurement instance.</td>
		<td>string</td>
		<td>If we use a composite primary key, for example, this may optional?</td>
	</tr>
	<tr>
		<td>measurement.method [0..1]</td>
		<td>Describes the way in which the Detector detects the measure, for example, Wifi positioning by signal strength, Bluetooth, Thermometer, and so on. Probably use a commonly-used term from a controlled list. </td>
		<td>Vocabulary term from ontology of measurement methods.</td>
		<td>This could use a locally controlled list, not one controlled centrally, in much the same way as for subType extensions in Jisc xAPI.</td>
	</tr>
	<tr>
		<td>measurement.scale_name [0..1]</td>
		<td>Label for the commonly-used name of the scale of values (for example, Celsius)</td>
		<td>string</td>
		<td></td>
	</tr>
	<tr>
		<td>measurement.value [1]</td>
		<td>The observed value or returned value (for example an average of observed values) describing the phenomenon</td>
		<td>Numeric value</td>
		<td></td>
	</tr>
</table>

## Sensor Entity
### Description
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
		<td>sensor.ip-address [0..1]</td>
		<td>Sensor's IP address</td>
		<td>ip address</td>
 		<td>Could be IPv4 or IPv6. May need a label to provide this detail.</td>
	</tr>
	<tr>
		<td>sensor.mac [0..1]</td>
		<td>MAC address of sensor</td>
		<td>Mac address format: this could be 48-bit or 64-bit hexadecimal or formated to traditional nn:nn:nn:nn:nn:nn or nn:nn:nn:nn:nn:nn:nn:nn.</td>
		<td>Should we specify? I think we leave it to the provider.</td>
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

## JSON example with everything

``` JSON
{
"measurement_event": {
    "context": {
        "event_frequency": "hourly",
        "id": "kccBCAICAQYR/zMBF2QOEAABARoB1gCfAQAJCUQ2QjI3ODiP",
        "location": {
            "room_id": "AS34",
            "sensorLocation": {
		"type": "Feature",
		"geometry": {
			"type": "Point",
			"coordinates": [51.510531, -0.118930]
			},
		"properties": {
		    "name": "University of Jisc"
		}
	    },
            "site_id": "Main1234"
        },
        "timestamp": "2018-07-23T16:27:10.418789Z",
        "transmission": "WiFi"
    },
    "measurement": {
        "id": 129,
	"method": "thermometer",
	"scale_name": "Celsius",
        "value": 27.5
    },
    "sensor": {
	"id": "15",
	"ip-address": "34.248.41.184",
	"mac": "008000000000ba34",
	"name": "safehouse:test",
	"type": "safehouse"
    }
}
}
```

## JSON example with only mandatory elements

``` JSON
{
"measurement_event": {
    "context": {
        "id": "kccBCAICAQYR/zMBF2QOEAABARoB1gCfAQAJCUQ2QjI3ODiP",
        "location": {
            "room_id": "AS34"
        },
        "timestamp": "2018-07-23T16:27:10.418789Z"
    },
    "measurement": {
        "id": 129,
        "value": 27.5
	},
	"sensor": {
		"id": "15"
	}
}
}
