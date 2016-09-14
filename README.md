[![Stories in Ready](https://badge.waffle.io/fullstackla/fullstackla.github.io.png?label=ready&title=Ready)](https://waffle.io/fullstackla/fullstackla.github.io)  [![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.svg)](https://github.com/ellerbrock/open-source-badge/)

# Fullstack LA

Fullstack LA's main web site.

Fullstack LA is meet up in Los Angeles focused on the coding and open source
communities. Our mission is to encourage developer of all levels to grow there
skills while contributing to open source projects.

To date our events have centered around pair programing which brings with it a
high level of participant engagement.

## Fullstack LA Main Site

This site is built on [Jekyll] and hosted on [Github pages].

[exercism.io]: http://exercism.io/
[Jekyll]: https://jekyllrb.com/
[Github Pages]: https://pages.github.com/

## Adding new Events

Creating a new event is as simple as adding a new markdown file to the events directory. The simplest way is probably, to
duplicate an existing event and change a few things. The steeps below cover the essential unique attributes of an event.

### File name and location

Following the naming convention: `year-month-day-name.md`. _The naming convention is critical. Jekyll uses the file name to know how to handle the file._  For example, you can name the file: `$ touch 2016-09-21-mapillary.md`.

### YAML Frontmatter

The first thing that must appear in the file is a [YAML front matter block](https://jekyllrb.com/docs/frontmatter/). It's a block that opens with three `---` dashes and closes with three `---` dashes. The inside of the block should contains a list of variables which are user when the page is rendered. **Make sure to specify in the layout** whether it's an ongoing event by entering `os-repeat-event` or a onetime event by entering `os-single-event`.
  
+ layout        - The layout used for the event. Available layouts are located in the `/_layouts` directory.
+ title         - The title of the event.
+ event-date    - e.g. __September 21st__
+ location      - Exact GPS cordance. Must be formatted in an array. e.g. __[34.056446, -118.253927]__
+ location-name - Name of location. String with or without quotes.
+ parking       - Path to the parking include for the location. e.g. `events/parking/8thlight.html`. If your event has a never before used location, refer to the `_includes/events/parking/` for reference.
+ tag-line      - (optional) Not in use.
+ rsvp          - link to FSLA meetup.com URL event page. (At present needs to be made by @kpearson or @machiko)
+ image         - Single image asset, which should be stored in the `/img/events` directory. Usually a photo of the speaker. Sourcing and adding the image to the site repo is usual part of adding an event.
  
Example frontmatter:
```yml
---
layout: os-repeat-event
title: So and so introduces Supper cool project name
event-date: September 21st
location: [34.056446, -118.253927]
location-name: 8th Light
parking: events/parking/8thlight.html
tag-line: Talk about Falcor/Mapillary/etc
rsvp: http://www.meetup.com/la-fullstack/events/233276393/
image: https://pbs.twimg.com/profile_images/2373368709/1n6soromrqqzzw6jl9el_400x400.jpeg
---
```

+ Event Description
  + A few sentences describing the project and the speaker(if any) include external link to the speaker and project.
  + Additional instructions for the event, like what to clone down.
+ Save the file and voilà, you've created a new event on the FSLA website! 👍👏
