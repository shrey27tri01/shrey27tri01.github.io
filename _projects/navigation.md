---
layout: project
title: Navigation System
subtitle: Modelling roads, intersections and routes
---

A navigation system in Java, modelling roads, intersections, and routes. 

Intersections are basically locations where roads join, and routes are basically a series of roads that connect a start location to an end location.

The program consists of two pakages:
- The first package consists of the following:
    - **Class Point:** Defined by two double values – the x,y coordinates of the point. It provides methods to set and get the coordinate values, and get the distance to another point.
    - **Class Line:** Defined by two Point objects. It provides a method to return the length (double) of the Line object. It also has a static method that returns the total length of a list of Line objects.
- The second package consists of the following:
    - **Class Location:** Has a String name and an instance of Point that contains the coordinates.
    - **Class Road:** Builds on Line, is constructed with Locations as its end points, and also contains name (string), width (double). No vehicle wider than “width” can use this road.
    - **Class Route:** Modelled as a list of Roads. Assuming that the roads of a Route connect up end-to-end, it has a method that will return the length of the Route. The class also has a static method that checks if the roads form a connected path, where the end location of a road is the same as the start location of the next road in the list.

The main program reads in a set of Location, Road and Route data in a format specified below, and for each Route, prints out the series of Locations it connects, the Roads traversed and the total length and the max width of a vehicle traversing this route (in a format specified below). If the data for a route does not form a connected path, it prints out that the input data is invalid.


#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/navigation-system-java)   




