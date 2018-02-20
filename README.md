# Goldfish

## Idea

The idea is to have a tool that is basically able to log all findings that analysts collect during incident response / forensic investigations.
Most people start with a spreadsheet with the following columns:

|date|time|Source|Hostname|Content / Raw Entry |Comment | 
|---|---|---|---|---|---|
|2018-02-20| 07:00:01Z   |RegKey:Modified   |TargetHost   |Lorem Ipsum   |This is vary interesting   |

However that approach does not really scale when a team is working on a case maybe involving multiple systems.

### Structure

There is a central Goldfish instance running that is being exposed via WebUi and / or REST-API. Thus analysts can add / modify delete data using both methods.

Within the WebUI different filter / search options would be ideal and an export to CSV is planned to enable analysts to take the latest data back to various other tools.


### Differences to xyz

Of couse the idea behind can be achieved with other tools like ticketing tools, SIEM solutions or any other cyber related tool. Goldfish is not intended to be a Swiss Army knife to solve dozen of problems but a bottle opener, made for a single task.


## Installation

How to install the goldfish to the fishbowl

## Sample requests

### GET /findings/_design/by_host/_view/by_host?key="hostname123"

Will return a json array of all findings to a given hostname.
By appending "&include_docs=true" it will also contain the whole entry

### POST finding

