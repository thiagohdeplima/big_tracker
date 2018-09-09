# Big Tracker

The Big Tracker will be a general purpose geospatial and distribuited server application, which aims to implement resources to solve most of problems related with object monitoring and queries by position / time.

## Data Model

Big Tracker represents all data using GeoJSON. For more details, read [GeoJSON](https://tools.ietf.org/html/rfc7946)

## Distribuited System

In context of geospatial data, the majority of applications might support eventual consistence when availability is garanteed. Having that in mind, Big Tracker is a cAP application.

For more details, read about [CAP Theorem](https://en.wikipedia.org/wiki/CAP_theorem).

## Communication Protocols

This application implements communication's interfaces in this two following protocols:

### MQTT

MQTT is a extremely lightweight messaging protocol, whereby positions of objects will be sent to Big Tracker.

### HTTP

Big Tracker will implements a GraphQL API to query several informations, like:
* Last position of an object;
* Position history of an object between hours;
* All objects that who have been in a radius of some location in certain time;
* etc.
