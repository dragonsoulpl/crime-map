# Crime Map

## Overview

This is a React app that uses Google Maps API and crime data to determine and display the safest route for your travels. The application includes both a frontend and backend to process and display data interactively.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Before you start, make sure you have:

- Node.js installed (at least v14.0.0)
- npm (which comes with Node.js)
- A modern web browser

### Installation

1. Clone the repo

```bash
git clone https://github.com/dragonsoulpl/crime-map.git
cd crime-map
npm install
npm start
```

Usage
Once you have started the app, navigate to http://localhost:3000 in your web browser. You will be greeted with a homepage and a navbar to redirect to the directions page. On the homepage, the user will be able to see the all crimes in their area. The direction map page will allow the user to input an origin and destination to get three routes from least safe to safest.

Technologies Used
React: A JavaScript library for building user interfaces
Google Maps API: Used for map and route rendering
Node.js: The JavaScript runtime used
OpenCage Geocoder API: Used to convert text into latitude and longitude.

# Example Usage
This is the homepage where the user can see all recent crimes in their area and can click each marker for more details.

![image](https://github.com/dragonsoulpl/crime-map/assets/91435678/d39c201b-1ade-4d6f-ae7a-0282816603c9)

This is the direction map page, where the user can input the origin and destination addresses

![image](https://github.com/dragonsoulpl/crime-map/assets/91435678/8c7cddb1-e9a7-4881-b71f-bd55d9bf4229)

This is the example output
![image](https://github.com/dragonsoulpl/crime-map/assets/91435678/d435bd06-79b8-47f5-b1dd-4d1499b83ef3)

Shown above are three routes categorized using red, yellow, and green. Red indicates the least safe route, but can be more time efficient. Yellow is typically a middle ground. Green is the safest route, and will go out of its way to find blocks with the least amount of crimes. All of these routes will stay within reason so the user doesn't travel outside of boundaries.

The app applies Dijkstra’s algorithm using weights calculated from the tier system, to generate
a potential route that the user could take. The tier system is shown below.

![image](https://github.com/dragonsoulpl/crime-map/assets/91435678/8e38f92d-6175-4977-84ba-26b871781a4e)
