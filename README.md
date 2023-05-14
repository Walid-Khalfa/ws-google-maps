# Getting Started with Google Maps API with Places autocomplete and Directions service and renderer.

ws-google-maps
The ws-google-maps project is a lightweight Node.js module for interacting with the Google Maps API. This module provides a simple API for performing common tasks like geocoding, reverse geocoding, and calculating distances between locations.

Installation
To use ws-google-maps in your project, you can install it via npm:

npm install ws-google-maps
Usage
To use the ws-google-maps module, you'll need to get an API key from the Google Cloud Console. Once you have your API key, you can require the module in your Node.js project and create a new instance using your API key:

const WSGoogleMaps = require('ws-google-maps');
const gm = new WSGoogleMaps('YOUR_API_KEY');
With the module instance, you can use the provided methods to interact with the Google Maps API:

gm.geocode('1600 Amphitheatre Parkway, Mountain View, CA 94043')
  .then(result => {
    console.log(result);
  })
  .catch(error => {
    console.error(error);
  });
This example uses the geocode method to look up the coordinates for Google's headquarters in Mountain View, California.

API
The ws-google-maps module provides the following methods:

geocode(address: string): Promise<object>
Given an address string, returns an object containing the latitude and longitude of the location.

reverseGeocode(latlng: string): Promise<object>
Given a latitude and longitude string, returns an object containing information about the location, such as the address.

distance(from: string, to: string): Promise<number>
Given two addresses or latlngs, returns the distance between the two in kilometers.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing
If you would like to contribute to ws-google-maps, please submit a pull request with your changes. Contributions are always welcome!

Contact
If you have any questions or issues with ws-google-maps, please feel free to open an issue on the GitHub repository or contact the author directly.
