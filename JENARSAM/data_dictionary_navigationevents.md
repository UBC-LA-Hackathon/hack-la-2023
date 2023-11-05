# Hackathon Data

## **Navigation Events** 
Student-level navigation events in a given Canvas course. This dataset has been simplified for the purpose of this hackathon. **Note**: if you are using the event data shared with you from the Canvas Hackathon course, this is **your own data** and should be treated appropriately (as indicated in the release/consent form and other materials)
 
Original Navigation Events (not used in this hackathon) are in the following format: https://canvas.instructure.com/doc/api/file.data_service_caliper_navigation_events.html

> {your-events-here}.csv (note, any starter materials refer to this as `events.csv`)

### Caliper Events
Caliper events follow certain profiles depending on their type. In general, a Caliper Event described the relationship between an actor and an object, where the actor acts upon the object. In our case, the actor NavigatedTo an object, where the object is some part of the Canvas course.

![](https://www.imsglobal.org/sites/default/files/specs/images/caliper/1p2/caliper-event_model_no_title-v1p2.png)
> Image from [IMS Global](https://www.imsglobal.org/spec/caliper/v1p2#event)

More about the Caliper information model: https://www.imsglobal.org/spec/caliper/v1p2#the-information-model

[Navigation events](https://www.imsglobal.org/spec/caliper/v1p2#navigationevent) are a type of Caliper event. In the original data, Caliper events are in JSON format and each event includes a list of "data". In the transformed csv, each item in the data list is an "event". The field will contain the prefix event__ for each.


### Field Descriptions
- We have only included the fields included in the dataset, and partial definitions. You should find everything you need to know in the Caliper documentation.

 See:
 1. https://www.imsglobal.org/spec/caliper/v1p2#event

 2. https://www.imsglobal.org/spec/caliper/v1p2#navigationevent

Fields that start with event__ are parsed from an event object. See more: https://canvas.instructure.com/doc/api/file.data_service_caliper_navigation_events.html 

> 🧐 Stuck on your hackathon idea? Help us build the data dictionary! Submit a pull request from a branch named `dictionary_update_{TEAMNAME}`. This shouldn't just by a replication of the Caliper dictionaries above - but should provide more meaningful Descriptions and Notes.

Field | Description | Note
---------|---------|---------
canvas_user_id | Your Canvas user id!
name | Your name (as it appears in Canvas)
id | UUID that is expressed as a URN in the form     “urn:uuid:<UUID>” | Each Caliper Event must be assigned a UUID
type | String value corresponding to the term corresponding to Event or subtype of Event
action | Something performed or done to accomplish a purpose | Each Event may only specified one action
event_time | The time the event occurred (UTC)
ed_app | The app emitting the event (for this event the ed_app is always the same)
course_offering_id | The course ID (the format is known as the Global Canvas ID - which includes our institution code 11224000...). The trailing digits should match the course_id in the url like 'https://canvas.ubc.ca/course/1111'
session_id | This is the unique identifier for each session representing a web application user session

statement_type | It provides a way to classify and understand the nature of statements within a dataset, making it easier to analyse and work with the data.

statement_version | This field is used to track and manage different versions of statements in a dataset.


object_id | This is the unique identifer for each object, and should relate to each event__object_extensions_asset_name. | This should act as your join key, where possible to the additional datasets
membership_role | An ordered collection of organisational roles assigned to the member. | Whenever a subrole is specified, the core context role should also be included

event__object_type |  It is a data element that is used to specify the classification of the object within the context of the event.

event__object_name | It is a data element that represents the name or identifier of an object associated with an event | This field is used to provide a specific, human-readable reference for the object involved in the event.

event__object_extensions_asset_name | Name of the asset from the map of additional attributes (extensions) of the object described in event

event__object_extensions_asset_type | It represents a data type that is associated with an event and is used to describe and categorise the type of assets related to the event.

event__object_extensions_asset_subtype |  It represents a data element associated with an event that further details and subcategories the type of asset related to that event.

event__object_extensions_entity_id | The id of entity (object) within the map of additional attributes of the object described by the event

event__object_extensions_http_method |  a structured way to categorise data elements associated with events and objects, including relevant details and their use with HTTP methods in a system or application 

event__referrer |  An entity that represents the referring context | a referrer value must be expressed either as an object or as a string corresponding to the referrer’s IRI

event__request_id | The field that is associated with an event and is used for tracking and organising events and their corresponding requests, providing a unique identifier for each request associated with a particular event.

event__request_url | the field that is associated with an event and stores the URL (Uniform Resource Locator) related to a specific request within that event | this field would contain the URI that was used to make the request as part of the event.  


