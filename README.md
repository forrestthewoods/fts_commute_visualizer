fts_commute_visualizer
===

Build visualizations to see how far you can commute based on transportation mode and real world traffic.

## Blog Post

For additional information read my extensive [blog post](blog.forrestthewoods.com).

## Features

* Visualize commute times and range both from home or to a destination
* See commute times for walking, bicycling, public transit, or driving.
* See commute time **with traffic* (driving only)
* Specify driving traffic conditions: Best Guess, Optimistic, Pessimistic
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
6. Replace "YOUR_API_KEY" with your API key.

The Google cloud free tier is limited to 2500 requests per day. Each hexagon counts as 1 request. After reaching your daily limit Google Maps API calls are heavily throttled.


FAQ
===

#### What is fts_commute_visualizer?
A tool I built to help visualize how long it takes to commute based on a mode of transport and travel time.

#### What license?
All source code is embedded with a dual license. Choose either MIT or Unlicense. See fts_commute_visualizer.html for details.

#### What is FTS?
My initials; Forrest Thomas Smith.

#### Why a single file?
Why would this be more than one file? It's a simple project. The whole thing is just 1500 lines long. Google Maps does all the real work.

It doesn't need a framework. It doesn't need a build system. It doesn't even need jquery. [Vanilla JS](http://vanilla-js.com/) is more than enough.

#### Why is your code so bad?
I'm a video game programmer. I don't know how to write idiomatic JavaScript. I tried my best to keep things easy to understand follow. Dynamic languages are hard.


Examples 
===

Here is some example output produced by my tool. For a more detailed look please read my [blog post](blog.forrestthewoods.com).

### South Lake Union

South Lake Union is a booming Seattle neighborhood. Located within are offices for Amazon, Google, Facebook, and more. Here is what it looks like to commute to South Lake Union at 8:00 am.

![](/examples/southlakeunion_0.png?raw=true)
![](/examples/southlakeunion_1.png?raw=true)
![](/examples/southlakeunion_2.png?raw=true)
![](/examples/southlakeunion_3.png?raw=true)
![](/examples/southlakeunion_4.png?raw=true)

### Kenmore, Wa

A few years ago I lived in the Seattle suburb of Kenmore. Located at the northern tip of Lake Washington it allows for access to both the west and east side. Even better there's a large park and ride transit hub. Here's what it looks like to commute from Kenmore at 8:00 am.

![](/examples/kenmore_0.png?raw=true)
![](/examples/kenmore_1.png?raw=true)
![](/examples/kenmore_2.png?raw=true)

### Browser Tool

Here's what the tool actually looks like. There are a variety of controls such as mode of transport, travel direction, and travel time.

![](/examples/tool.png?raw=true)
