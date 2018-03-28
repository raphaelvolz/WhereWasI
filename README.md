(c) March 2018 by Raphael Volz - Hopefully written in a few hours at London, UK

# WhereWasI
A simple test of the serverless offerings by AWS:

- DynamoDB for storing user data (in two tables)
- Cognito for user login, registration and such
- Lambda for reading, writing data to DynamoDB, if needed
- JavaScript for calculating air distance and time 

Non-Amazon services used:
- HTML5 Geolocation for location detection
- Leaflet for Map Display
- Possibly, GraphHopper or other OSM-based routing service for calculation of way home

# DynamoDB tables
- User (EMail, HomeLat, HomeLon, SecretKey)
- Location (EMail, Lat, Lon, TimeStamp)

# Screens
- Login Screen (Cognito)
- Logged In Screen > Post User Location based on HTML5 GeoID, calculate Distance to Home Location, Form to Capture Home Location, And Secret Key
- Non-
- Not Logged In Screen > Given Key, find last location

# Build Log

## Create Cognito User Poo
At [https://eu-west-2.console.aws.amazon.com/cognito/users/?region=eu-west-2#/pool/new/create?_k=wfhmqu](AWS Cognito)
- MFA Off
- Verification via E-Mail
- Required Attribute email
- Custom attributes HomeLat, HomeLon, SecretKey to avoid user table
- App Client WhereAmI
