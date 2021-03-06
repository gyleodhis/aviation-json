[ ![Codeship Status for cristobal-io/aviation-json](https://codeship.com/projects/78fc3fa0-d958-0133-edc2-427380cff3d6/status?branch=master)](https://codeship.com/projects/143475)
[![Coverage Status](https://coveralls.io/repos/github/cristobal-io/aviation-json/badge.svg?branch=master)](https://coveralls.io/github/cristobal-io/aviation-json?branch=master)

# aviation-json

## Description:

Module created to make available a quick way to update all the aviation related information from wikipedia.

Using the package aviation-scraper to download all the information regarding airports, airlines and their destinations from wikipedia exposes the following files:

* airline_destinations.json (an object where the key is the airline url and an array of destination airport urls)
* airlines.json (an array with all the airlines data)
* airport_airlines.json (an object with all the airports including the airlines that fly to this airport grouped into an array)
* airport_cities.json (an object where the key is the primary key of the airport that includes the name and the url of the city it belongs to.)
* airport_runways.json (an object with the runways for each airport.)
* airports.json (an object with all the airports and their data)
* city_airports.json (an object that includes all the airports into one city.)

## Usage.

install via npm:

```bash
npm install aviation-json --save
```

```javascript
var aviationJson = require("aviation-json");
// then you will have available all the information.

var airlineDestinations = aviationJson.airline_destinations;
var airlines = aviationJson.airlines;
var airportAirlines = aviationJson.airport_airlines;
var airportsCities = aviationJson.airport_cities;
var airportRunways = aviationJson.airport_runways;
var airports = aviationJson.airports;
var cityAirports = aviationJson.city_airports;

```


### Updating the information:

Go to the node_modules/aviation-json directory and run 'make sync'

> This is going to take a while and depending on your internet connection you may have troubles, after the 5 time trying to reach the wikipedia page to scrape the information, it will throw and err.

## Testing.

All the code is properly tested. To run the test:

```bash
# this command lint all the files and runs the tests.
make test
```

if you want to be in watch mode:

```bash
# this command run the test in watch mode.
make dev
```

## Contributions:

If you want to contribute, create your branch and place a PR or open an issue.


