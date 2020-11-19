## Winnipeg Jets API

#### Contents
- [API Documentation](#api-documentation)
- [Parameters](#parameters)
- [Sample Requests](#sample-requests)
- [Authors and Acknowledgements](#authors-and-acknowledgements)

#### API Documentation

#### Parameters

- year (int): Specific year. Required. 

- player (string): Name of the player. Required.

- pos (string): Position in the game. Required.


#### Sample Requests

``` 
https://api.winnipegjets.ca/json/year=2012 	= Current players in Winnipeg Jet

https://api.winnipegjets.ca/json?player=Name 	= Stats of the player

https://api.winnipegjets.ca/?year=2008&pos=middle 	= Name of the player that played that position on that year, how many goals in that game, years in the game.

```

#### Response

The result of the request will be formatted using JSON

**Insert examples here**

#### Authors and Acknowledgements

- [Marielle Manlulu](https://github.com/mariellemanlulu)
- [Prakhar Sharma](https://github.com/Neil3108)
- [Chris Ciceron](https://github.com/chrisciceron)
