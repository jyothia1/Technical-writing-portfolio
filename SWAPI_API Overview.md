# SWAPI API Overview

## Introduction

The Star Wars API (SWAPI) provides access to structured data about the Star Wars universe. Users can retrieve information about planets, spaceships, vehicles, people, films and species by sending HTTP requests to the API.
SWAPI returns resource data in JSON format. The API is publicly accessible and does not require authentication to retrieve data.

## Getting Started

To get started with SWAPI, send a HTTP GET request to API. You can use tools such as cURL or httpie to make requests.
For example, the following request retrieves information about the planet Tatooine:
`https://swapi.py4e.com/api/planets/1/`

*Response in httpie:*
```
HTTP/1.0 200 OK
Content-Type: application/json
{
    "climate": "Arid",
    "diameter": "10465",
    "gravity": "1 standard",
    "name": "Tatooine",
    "orbital_period": "304",
    "population": "200000",
    "residents": [
        "https://swapi.py4e.com/api/people/1/",
        "https://swapi.py4e.com/api/people/2/",
        ...
    ],
    "rotation_period": "23",
    "surface_water": "1",
    "terrain": "Dessert",
    "url": "https://swapi.py4e.com/api/planets/1/"
}
```

## Base URL

The base URL is the root address used to access all APIs.
`https://swapi.py4e.com/api/`
Append the appropriate resource endpoint to the base URL to construct a complete request URL.
For example:
`https://swapi.py4e.com/api/people/1/`
This endpoint retrieves information about the person identified by ID 1.

## Rate Limiting
SWAPI limits requests by IP address to help prevent misuse and handle large amount of traffic. The rate limit is 10,000 requests per day per IP address. This limit is sufficient to retrieve all the data from the website.

## Authentication
SWAPI does not require authentication to retrieve data. If you face any issue, contact support team.

## Request and Response format
SWAPI uses JavaScript Object Notation (JSON) schema by default for request and response. It allows user to inspect the attributes of the resource and their types. 
Wookiee users can append `?format=wookiee` to a request URL.
For example:
`https://swapi.py4e.com/api/planets/1/?format=wookiee`

## Searching resources
SWAPI supports a search query parameter for filtering resources. Search terms are matched case-insensitively and can return partial matches for supported fields.
For example:
`https://swapi.py4e.com/api/people/?search=r2`


## Source

[SWAPI Documentation](https://swapi.py4e.com/documentation)
