# Introduction
API Reference provides information for two endpoints from people resource.

They are:

•	`GET  /people/` -- fetches a list of people

•	`GET  /people/:id/` -- fetches details of a specific person.

# GET – Fetches a list of people
## Resource
People

## Introduction
Retrieves details of people

## Method
GET

## Base URL
`swapi.py4e.com/api/`

## Request URL
`https://swapi.py4e.com/api/people/`

## Path Parameter
| Parameter | Required/Optional | Data Type | Values | Description of the parameter |
|-----------|-------------------|-----------|--------|------------------------------|
| search    | Required	        | string	  | -      | Filters person by name       |

## Response parameter
| Parameter |	Child parameters	| Data Type |	Values |	Description of the parameter |
|-----------|-------------------|-----------|--------|-------------------------------|
| count     |	-                 |	Int64	    | -      |	Total number of people.      |
| next      |	-                 |	string    | -      |	URL of the next page.        |
| previous  |	-                 |	null      | -      |	URL of the previous page.    |
| results   |	name              |	string    | -      |	Name of the person.          |
|           | height            | string    | -      | Height of the person in centimeters. |
|           | mass              | string    | -      | Mass of the person in kilograms. |
|           | hair_color        | string    | <ul><li>color</li><li>unknown</li><li>n/a</li></ul> | Hair color of the person. Values: <ul><li>color - mention the hair color</li><li>unknown - hair color is not known</li><li>n/a - person does not have hair</li></ul> |
|           | skin_color        |	string    |	-	     | Skin color of the person. |
|           | eye_color         |	string	  |<ul><li>color</li><li>unknown</li><li>n/a</li></ul> |	Eye color of the person. Values: <ul><li>color - mention the eye color</li><li>unknown - eye color is not known</li><li>n/a - person does not have an eye</li></ul> |
|           | birth_year	      | string	  |	-       | Birth year of the person, using the star wars calendar. (BBY- Before the Battle of Yavin or ABY - After the Battle of Yavin). For example: 19BBY. |
|           | gender	          | string    |	<ul><li>male</li><li>female</li><li>unknown</li><li>n/a</li></ul> | Gender of the person. Values: <ul><li>male – the person is male</li><li>female – the person is female</li><li>unknown – gender is not known</li><li>n/a – gender is not applicable</li></ul> |
|           | homeworld	        |string	    | -        | URL of the planet where the person was born. |
|           | films	            | array	    |	-        | URLs of films featuring the person. |
|           | species	          | array	    |	-        | URLs of species belong to the person. |
|           | vehicles	        | array		  | -        | URLs of vehicles the person has piloted. |
|           | starships	        | array	    | -        | URLs of starships the person has piloted. |
| created	  | -                 |	string    |	- 	     | Date and time when the resource was created. |
| edited	  |	-                 | string	  |	-        | Date and time when the resource was last edited. |
| url	      | -                 |	string    |	-        | URL of the resource. |

## Response/Example JSON
```
{
  "count": 87,
  "next": "https://swapi.py4e.com/api/people/?page=2",
  "previous": null,
  "results": [
              {
               "name": "Luke Skywalker",
               "height": "172",
               "mass": "77",
               "hair_color": "blond",
               "skin_color": "fair",
               "eye_color": "blue",
               "birth_year": "19BBY",
               "gender": "male",
               "homeworld": "https://swapi.py4e.com/api/planets/1/",
               "films": [
                         "https://swapi.py4e.com/api/films/1/",
                         "https://swapi.py4e.com/api/films/2/",
                         "https://swapi.py4e.com/api/films/3/",
                         "https://swapi.py4e.com/api/films/6/",
                         "https://swapi.py4e.com/api/films/7/"
                        ],
               "species": [
                           "https://swapi.py4e.com/api/species/1/"
                          ],
               "vehicles": [
                         "https://swapi.py4e.com/api/vehicles/14/",
                         "https://swapi.py4e.com/api/vehicles/30/"
                        ],
               "starships": [
                          "https://swapi.py4e.com/api/starships/12/",
                          "https://swapi.py4e.com/api/starships/22/"
                       ],
               "created": "2014-12-09T13:50:51.644000Z",
               "edited": "2014-12-20T21:17:56.891000Z",
               "url": "https://swapi.py4e.com/api/people/1/"
              }
             ]
}
```


# Get – Fetches details of a specific person
## Resource
People

## Introduction
Retrieves details of a specific person using unique ID.

## Method
GET

## Base URL
`swapi.py4e.com/api/`

## Request URL
`https://swapi.py4e.com/api/people/{id}/`

## Example URL
`https://swapi.py4e.com/api/people/1/`

## Path Parameter
| Parameter | Required/Optional | Data Type | Values | Description of the parameter |
|-----------|-------------------|-----------|--------|------------------------------|
| id        | Required	        | Int64 	  | -      | Unique id of the person.     |

## Response parameter
| Parameter |	Child parameters	| Data Type |	Values |	Description of the parameter |
|-----------|-------------------|-----------|--------|-------------------------------|
| name      | -                 |	string    | -      | Name of the person.           |
| height    | -                 | string    | -      | Height of the person in centimeters. |
| mass      | -                 | string    | -      | Mass of the person in kilograms. |
| hair_color | -                | string    | <ul><li>color</li><li>unknown</li><li>n/a</li></ul> | Hair color of the person. Values: <ul><li>color - mention the hair color</li><li>unknown - hair color is not known</li><li>n/a - person does not have hair</li></ul> |
| skin_color | -                |	string    |	-	     | Skin color of the person. |
| eye_color  | -                |	string	  |<ul><li>color</li><li>unknown</li><li>n/a</li></ul> |	Eye color of the person. Values: <ul><li>color - mention the eye color</li><li>unknown - eye color is not known</li><li>n/a - person does not have an eye</li></ul> |
| birth_year | -                | string	  |	-       | Birth year of the person, using the star wars calendar. (BBY- Before the Battle of Yavin or ABY - After the Battle of Yavin). For example: 19BBY. |
| gender	   | -                | string    |	<ul><li>male</li><li>female</li><li>unknown</li><li>n/a</li></ul> | Gender of the person. Values: <ul><li>male – the person is male</li><li>female – the person is female</li><li>unknown – gender is not known</li><li>n/a – gender is not applicable</li></ul> |
| homeworld	| -                 | string	  | -        | URL of the planet where the person was born. |
| films	    | -                 | array	    |	-        | URLs of films featuring the person. |
| species	  | -                 | array	    |	-        | URLs of species belong to the person. |
| vehicles	| -                 | array		  | -        | URLs of vehicles the person has piloted. |
| starships	| -                 | array	    | -        | URLs of starships the person has piloted. |
| created	  | -                 |	string    |	- 	     | Date and time when the resource was created. |
| edited	  |	-                 | string	  |	-        | Date and time when the resource was last edited. |
| url	      | -                 |	string    |	-        | URL of the resource. |


## Response/Example JSON
```
{
  "name": "Luke Skywalker",
  "height": "172",
  "mass": "77",
  "hair_color": "blond",
  "skin_color": "fair",
  "eye_color": "blue",
  "birth_year": "19BBY",
  "gender": "male",
  "homeworld": "https://swapi.py4e.com/api/planets/1/",
  "films": [
            "https://swapi.py4e.com/api/films/1/",
            "https://swapi.py4e.com/api/films/2/",
            "https://swapi.py4e.com/api/films/3/",
            "https://swapi.py4e.com/api/films/6/",
            "https://swapi.py4e.com/api/films/7/"
           ],
  "species": [
              "https://swapi.py4e.com/api/species/1/"
              ],
  "vehicles": [
               "https://swapi.py4e.com/api/vehicles/14/",
               "https://swapi.py4e.com/api/vehicles/30/"
              ],
  "starships": [
                "https://swapi.py4e.com/api/starships/12/",
                "https://swapi.py4e.com/api/starships/22/"
                ],
  "created": "2014-12-09T13:50:51.644000Z",
  "edited": "2014-12-20T21:17:56.891000Z",
  "url": "https://swapi.py4e.com/api/people/1/"
}
```




