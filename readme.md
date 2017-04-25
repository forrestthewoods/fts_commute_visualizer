fts_commute_visualizer
===

Build visualizations to see how far you can commute based on transportation mode and real world traffic.

## Blog Post

For additional information read my extensive [blog post](https://blog.forrestthewoods.com/visualizing-commute-times-378009330ffa).

## Features

* Visualize commute times and range both from home or to a destination
* See commute times for walking, bicycling, public transit, or driving.
* See commute time **with traffic* (driving only)
* Specify driving traffic conditions: Best Guess, Optimistic, Pessimistic
* Works in any city for which Google Maps has data


## Installation

[fts_commute_visualizer.html](fts_commute_visualizer.html) is the only file you need. It contains all HTML, CSS, and JS. It can be run locally. There is no build system. You don't need a webserver.


### Google Maps API Key

You will need your own API key. Creating a new one is free and easy.

1. Enable [Google Dev Console](https://console.developers.google.com) with a Google account.
2. Create a new project.
3. Enable Google Maps Javascript API
4. Enable Google Maps Distance Matrix API
5. Enable Google Maps Time Zone API
6. Replace "YOUR_API_KEY" with your API key.

The Google cloud free tier is limited to 2500 requests per day. Each hexagon counts as 1 request. After reaching your daily limit Google Maps API calls are heavily throttled.

If you give Google your credit card and sign up for a [free trial](https://cloud.google.com/free/?hl=en_US&_ga=1.18292089.1130590081.1487912420) you can get $300 in free credits. Curiously I'm still not being charged for Distance Matrix queries. I am still throttled, but it's significantly faster. I strongly recommend doing this if you're building large maps or many maps.

## Using the Tool

This is, ahem, a bit of a programmer tool. There are several gotchas and silent errors. Here's what the tool looks like.

![](/examples/tool.png?raw=true)

### Drawing

On the bottom of the map there's a draw button. (It says 'Clear' in the image above). You want to click that then click and drag on the map. This lets you draw an arbitrary outline for the area you wish to search.

### Advanced Search

When performing an advanced search you must search for a time in the future. If you specify a time in the past it will silently fail. I need to add error messaging.

### Transit

When doing a transit search you almost always want to do an advanced search. Otherwise you will search for routes with a time of "now". Which if you're doing this at home at 8pm is probably not very many routes!

In hindsight I should have made those settings mandatory and always on. It'd prevent a lot of confusion.

### Secret Options

If you open [fts_commute_visualizer.html](fts_commute_visualizer.html) and go to [line 452](https://github.com/forrestthewoods/fts_commute_visualizer/blob/master/fts_commute_visualizer.html#L452) you should see the following line.
            
```
<div id="styleOptionsDiv" style="display:none">
```

Change "display:none" to "display:block". This turns on some secret options. Of particular note is the ability to hide map UI elements. Which is useful for taking screenshots. You can also mess with hexagon color and opacity at run-time if you feel like changing them.

I wouldn't call these hidden options "officially supported". But they may be of some use.


FAQ
===

#### What is fts_commute_visualizer?
A tool I built to help visualize how long it takes to commute based on a mode of transport and travel time.

#### What license?
All source code is embedded with a dual license. Choose either MIT or Unlicense. See [fts_commute_visualizer.html](fts_commute_visualizer.html) for details.

#### What is FTS?
My initials; Forrest Thomas Smith.

#### Why a single file?
Why would this be more than one file? It's a simple project. The whole thing is just 1500 lines long. Google Maps does all the real work.

It doesn't need a framework. It doesn't need a build system. It doesn't even need jquery. [Vanilla JS](http://vanilla-js.com/) is more than enough.

#### Why is the code so bad?
I'm a video game programmer. I don't know how to write idiomatic JavaScript. I tried my best to keep things easy to understand. Dynamic languages are hard.


Examples 
===

Here is some example output produced by my tool. For a more detailed look please read my [blog post](https://blog.forrestthewoods.com/visualizing-commute-times-378009330ffa).

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

