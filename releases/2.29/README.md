# DHIS 2.29 Upgrade Notes

## Database

- Run the database [SQL upgrade script](upgrade-229.sql) once before updating the WAR file.
- DHIS 2 now only supports *PostgreSQL* as database platform. Minimum required version is 9.4, however version 10 is recommended. The *PostGIS* extension for spatial data is also recommended.

## Web API

- The `Tracked Entity` object is renamed to `Tracked Entity Type` in the web API.
- Tracked entity types are associated with tracked entity attributes.
- The link between user roles and data sets and programs has been replaced by the new *data write* sharing levels.
- The system settings API only accepts supported system setting keys. This implies that custom setting keys will no longer be supported. Apps and clients which are using custom system settings for data storage should be migrated to using the data store API.
- Only web API versions from 2.26 and up are now supported (`/api/24`, `/api/25` etc have been removed).
