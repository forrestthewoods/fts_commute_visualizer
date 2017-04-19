fts_commute_visualizer
===

Build visualizations showing how far you can commute based on transportation mode and traffic.

## Blog Post

For additional information read my extensive [blog post](https://blog.forrestthewoods.com).


## Features

* Visualize time and range you can commute to from your home
* Visualize time and range it takes to commute to your work place
* See commute times for walking, bicycling, public transit, or driving.
* Specify departure time to see commute times WITH TRAFFIC
* Commute on foot, bicycle, public transit, or car
* Specify departure time (driving or transit) or arrival time (transit only)
* Specify traffic conditions (driving only): Best Guess, Optimistic, Pessimistic
* Works in any city for which Google Maps has data


## Installation

fts_commute_visualizer is a single html file. It contains all HTML, CSS, and JS. It can be run locally. There is no build system. You don't need a webserver. 

### Google Maps API Key

You will need your own API key. Creating a new one is free and easy.

1. Enable [Google Dev Console](https://console.developers.google.com) with a Google account.
2. Create a new project.
3. Enable Google Maps Javascript API
4. Enable Google Maps Distance Matrix API
5. Enable Google Maps Time Zone API
6. Replace "YOUR_API_KEY" in index.html with your API key.

The Google cloud free tier is limited to 2500 requests per day. Each hexagon counts as 1 request. After reaching your daily limit Google Maps API calls are heavily throttled.


## Example screenshots. 

Todo.


FAQS
===

#### What is fts_commute_visualizer

A tool I built to help visualize how long it takes to commute