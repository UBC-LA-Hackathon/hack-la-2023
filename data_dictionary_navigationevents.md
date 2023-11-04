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
id | UUID
type |
action |
event_time | The time the event occurred (UTC)
ed_app | The app emitting the event (for this event the ed_app is always the same)
course_offering_id | The course ID (the format is known as the Global Canvas ID - which includes our institution code 11224000...). The trailing digits should match the course_id in the url like 'https://canvas.ubc.ca/course/1111'
session_id | 
statement_type |
statement_version |
object_id | This is the unique identifer for each object, and should relate to each event__object_extensions_asset_name. | This should act as your join key, where possible to the additional datasets
membership_role |
event__object_type |
event__object_name |
event__object_extensions_asset_name |
event__object_extensions_asset_type |
event__object_extensions_asset_subtype |
event__object_extensions_entity_id |
event__object_extensions_http_method |
event__referrer |
event__request_id |
event__request_url |

