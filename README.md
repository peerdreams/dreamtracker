# dreamtracker

a private, federated bittorrent tracker

## why

bittorrent networks have only one centralized component: the tracker. 
this centralized point-of-failure makes network-breaking takedowns (relatively) easy.

meanwhile, private bittorrent trackers (in which only specified peers can share only specified files) face additional challenges.
enforcing access policies require a separate component (e.g. a [torrent server](https://github.com/WhatCD/Gazelle)) which ends up being tightly coupled with the tracker.

## dreamtracker approach

dreamtracker aims to increase the redundancy of BT networks by federating tracker functionality across multiple nodes.

at the same time, dreamtracker integrates private tracker (user management, torrent curation) into the core tracker functionality.

## timeline

- basic tracker functionality
  - incorporate signed updates
  - mock distributed store using shared message bus
  - successfully find peers over [the http(s) protocol](https://wiki.theory.org/BitTorrent_Tracker_Protocol)
- full private tracker spec implemented
  - inject per-user hash into torrent file ([BEP 27](http://www.bittorrent.org/beps/bep_0027.html))
- distributed datastore backend 
  - (perhaps with [akka](http://doc.akka.io/docs/akka/current/scala/distributed-data.html)).


