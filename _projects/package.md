---
layout: project
title: Package Shipment Management
subtitle: Modelling Package Shipment Management in Swing
---

A Java Swing program implementing package shipment management.

#### How it works:

A logistics company that manages a large volume of packages, has a number of stations distributed all over the map. Packages are shipped from any station to any other station. To simplify things, all packages from a given station to the same destination are loaded onto one or more Trucks. Stations are connected to Hubs, which are the nodes of a Highway network. Thus, a Truck that goes from a source Station to a destination Station is routed as
follows:
- Move to a Hub that is close to the source Station
- Navigate from Hub to Hub using Highways to the Hub that is close to the destination station.
- Move from this Hub to the destination Station

Constraints: 
- Trucks move at a certain maximum speed between Hubs and Stations and at a different maximum speed between Hubs (on a Highway)
- A Highway has a fixed capacity. At any given instant there is a maximum number of trucks that can be on the Highway. If a truck reaches a Hub, and it needs to get onto to Highway, it waits at the Hub until that Highway has spare capacity
- Hubs have a max capacity. At any given instant, there are a max number of trucks it can process, and that can be waiting at the Hub
- A truck travelling towards a Hub wait (on the road/highway) if that Hub is at full capacity
- To manage scale, entities like Hub, Highway, Truck (and their derived classes) keep minimal state information. For example, Truck does not keep track of the full route - just the source, destination locations, and previous, current and next Hubs.

Different companies manage the hubs and trucks. However, they all conform to some basic design. To model this, we have the following:
- Base classes `Hub`, `Truck`, `Highway` (we have not modelled Station and Road since they can be implicit)
- Each company creates its own derived classes of these, and specifically derived classes of `Hub`, `Highway` and `Truck`.
- A `Network` class maintains information about all the elements of the network
- A given network has instances of different sub-types of these classes, corresponding to the different companies involved.

The files `Hub.java`, `Truck.java`, `Highway.java` contain definitions of the base classes.

#### For the simulation:
- Multiple instances of Hub, Truck, Highway, have been created and added to a Network.
- Source and destination locations for Trucks aredefined at start time. Trucks start moving at their start time
- Each Truck navigates from start location to nearest Hub, and from there through other Hubs (and Highways) to reach the destination location/station.
- On their route, if the next Hub is full, they wait until the Hub becomes free for them to move there. Similarly for getting on to Highways.
- Trucks can move at any speed that does not exceed the speed limit for the road/highway

#### Implementation:

[GitHub Repository](https://github.com/shrey27tri01/Package-shipment-management)




