# Winnipeg Jets API

This Winnipeg Jets API uses simple GET methods to request for JSON formatted data about team and player information of Winnipeg Jets hockey team.

## Contents
- [API Reference Index](#api-reference-index)
  - [Team Roster](#team-roster)
    - [Parameters](#parameters)
    - [Resources Description as JSON](#resources-description-as-json)
    - [Sample Request](#sample-request)
    - [Response](#response)
  - [Player Stats](#player-stats)
    - [Parameters](#parameters-1)
    - [Resources Description as JSON](#resources-description-as-json-1)
    - [Sample Request Without Year](#sample-request-without-year)
    - [Response](#response-1)
    - [Sample Request With Year](#sample-request-with-year)
    - [Response](#response-2)
- [Authors](#authors)


## API Reference Index

### Team Roster

This retrieves the Winnipeg Jets roster, based on the year specified on the request. 

#### Parameters

`year (int)`: Specific year. Required.

#### Resources Description as JSON
```
{
	"resource" : "player",
	"endpoint" : {
		"type" : "GET",
		"path" : "/player/roster/{year}"
	},
	"pathParameters" : {
		"year" : "int"
	},
	"queryParameters" : null,
}
```
#### Sample Request

This uses a GET request to obtain the information on the roster.
``` 
https://api.winnipegjets.ca/player/roster/{2020}
```
#### Response

The result of the request will be formatted using JSON.

<details>
  <summary> SEE SAMPLE RESPONSE {...} </summary>
  
```
{
  {
    "firstName": "Mason",
    "lastName": "Appleton",
    "position": "F",
    "jerseyNumber": 82,
    "age": 24
  },
  {
    "firstName": "Nathan",
    "lastName": "Beaulieu",
    "position": "D",
    "jerseyNumber": 88,
    "age": 27
  },
  {
    "firstName": "Anthony",
    "lastName": "Bitetto",
    "position": "D",
    "jerseyNumber": 2,
    "age": 29
  },
  {
    "firstName": "Gabriel",
    "lastName": "Bourque",
    "position": "F",
    "jerseyNumber": 57,
    "age": 29
  },
  {
    "firstName": "Laurent",
    "lastName": "Brossoit",
    "position": "G",
    "jerseyNumber": 30,
    "age": 26
  },
  {
    "firstName": "Eric",
    "lastName": "Comrie",
    "position": "G",
    "jerseyNumber": 1,
    "age": 24
  },
  {
    "firstName": "Kyle",
    "lastName": "Connor",
    "position": "F",
    "jerseyNumber": 81,
    "age": 23
  },
  {
    "firstName": "Andrew",
    "lastName": "Copp",
    "position": "F",
    "jerseyNumber": 9,
    "age": 25
  },
  {
    "firstName": "Carl",
    "lastName": "Dahlstrom",
    "position": "D",
    "jerseyNumber": 23,
    "age": 25
  },
  {
    "firstName": "Dylan",
    "lastName": "DeMelo",
    "position": "D",
    "jerseyNumber": 2,
    "age": 26
  },
  {
    "firstName": "Cody",
    "lastName": "Eakin",
    "position": "F",
    "jerseyNumber": 20,
    "age": 28
  },
  {
    "firstName": "Nikolaj",
    "lastName": "Ehlers",
    "position": "F",
    "jerseyNumber": 27,
    "age": 23
  },
  {
    "firstName": "David",
    "lastName": "Gustafsson",
    "position": "F",
    "jerseyNumber": 19,
    "age": 19
  },
  {
    "firstName": "Jansen",
    "lastName": "Harkins",
    "position": "F",
    "jerseyNumber": 12,
    "age": 22
  },
  {
    "firstName": "Connor",
    "lastName": "Hellebuyck",
    "position": "G",
    "jerseyNumber": 37,
    "age": 26
  },
  {
    "firstName": "Dmitry",
    "lastName": "Kulikov",
    "position": "D",
    "jerseyNumber": 7,
    "age": 29
  },
  {
    "firstName": "Patrik",
    "lastName": "Laine",
    "position": "F",
    "jerseyNumber": 29,
    "age": 21
  },
  {
    "firstName": "Mark",
    "lastName": "Letestu",
    "position": "F",
    "jerseyNumber": 22,
    "age": 34
  },
  {
    "firstName": "Adam",
    "lastName": "Lowry",
    "position": "F",
    "jerseyNumber": 17,
    "age": 26
  },
  {
    "firstName": "Josh",
    "lastName": "Morrisey",
    "position": "D",
    "jerseyNumber": 44,
    "age": 24
  },
  {
    "firstName": "Sami",
    "lastName": "Niku",
    "position": "D",
    "jerseyNumber": 8,
    "age": 23
  },
  {
    "firstName": "Mathieu",
    "lastName": "Perreault",
    "position": "F",
    "jerseyNumber": 85,
    "age": 32
  },
  {
    "firstName": "Neal",
    "lastName": "Pionk",
    "position": "D",
    "jerseyNumber": 4,
    "age": 24
  },
  {
    "firstName": "Tucker",
    "lastName": "Poolman",
    "position": "D",
    "jerseyNumber": 3,
    "age": 26
  },
  {
    "firstName": "Jack",
    "lastName": "Roslovic",
    "position": "F",
    "jerseyNumber": 28,
    "age": 23
  },
  {
    "firstName": "Luca",
    "lastName": "Sbisa",
    "position": "D",
    "jerseyNumber": 5,
    "age": 30
  },
  {
    "firstName": "Mark",
    "lastName": "Scheifele",
    "position": "F",
    "jerseyNumber": 29,
    "age": 26
  },
  {
    "firstName": "Logan",
    "lastName": "Shaw",
    "position": "F",
    "jerseyNumber": 20,
    "age": 27
  },
  {
    "firstName": "Nicholas",
    "lastName": "Shore",
    "position": "F",
    "jerseyNumber": 21,
    "age": 27
  },
  {
    "firstName": "Blake",
    "lastName": "Wheeler",
    "position": "F",
    "jerseyNumber": 26,
    "age": 33
  }
}
```

  </details>
  
### Player Stats
This retrieves the stats for a particular Winnipeg Jets player, based on the name specified on the request. If year is mentioned it gives stats for that particular season.

#### Parameters

`firstName (string)`: First name of the player. Required.

`lastName (string)`: Last name of the player. Required.

`year (int)`: Year of the season. Optional.

#### Resources Description as JSON
```
{
	"resource" : "player",
	"endpoint" : {
		"type" : "GET",
		"path" : "/player/stats/"
	},
	"pathParameters" : null,
	"queryParameters" : {
		"firstName" : "string",
		"lastName" : "string"
		"year" : "int"
	}
}
```

#### Sample Request Without Year
``` 
https://api.winnipegjets.ca/player/stats?firstName=Nikolaj&lastName=Ehlers
```

#### Response
The result of the request will be formatted using JSON.
```
{
  {
    "id": 66,
    "league": "NHL"
    "gamesPlayed": 369,
    "goals": 115,
    "assist": 142,
    "points": 257,
    "penaltyMinute": 130
  }
}
```
#### Sample Request With Year
``` 
https://api.winnipegjets.ca/json?firstName=Nikolaj&lastName=Ehlers&year=2019
```
#### Response
```
{
  {
    "id": 66,
    "league": "NHL",
    "gamePlayed": 71,
    "goals": 25,
    "assist": 33,
    "points": 33,
    "penaltyMinute": 58
  }
}
```
## Authors
- [Marielle Manlulu](https://github.com/mariellemanlulu)
- [Prakhar Sharma](https://github.com/Neil3108)
- [Chris Ciceron](https://github.com/chrisciceron)

