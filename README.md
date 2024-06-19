Himalaya API Documentation
Overview
The Himalaya API provides access to information about Himalayan peaks and expeditions. This API allows users to retrieve details about various peaks and expeditions, including the ability to filter results based on specific criteria such as height or year.

Endpoints
1. Get Peaks
Endpoint: /peaks

Method: GET

Description: Retrieve a list of Himalayan peaks with optional filters and pagination.

Parameters:

page: (optional) The page number for pagination (default: 0).
page_size: (optional) The number of records per page (default: 100, max: 100).
height_min: (optional) Filter to include only peaks with a minimum height in meters.
include_details: (optional) Include additional details such as alternative names and first ascent information (0 or 1).


2. Get Peak by ID
Endpoint: /peaks/<peak_id>

Method: GET

Description: Retrieve detailed information about a specific peak by its ID.

3. Get Expeditions
Endpoint: /expeditions

Method: GET

Description: Retrieve a list of expeditions with optional filters and pagination.

Parameters:

page: (optional) The page number for pagination (default: 0).
page_size: (optional) The number of records per page (default: 100, max: 100).
year: (optional) Filter to include only expeditions from a specific year.

4. Get Expedition by ID
Endpoint: /expeditions/<expedition_id>

Method: GET

Description: Retrieve detailed information about a specific expedition by its ID.


Authentication
All endpoints require Basic Authentication. Ensure you provide valid credentials to access the API.

Error Handling
The API returns appropriate HTTP status codes and error messages in case of failures, such as:

404 Not Found: When the requested resource is not found.
400 Bad Request: When the request parameters are invalid.
