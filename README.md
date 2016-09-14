[![Stories in Ready](https://badge.waffle.io/fullstackla/fullstackla.github.io.png?label=ready&title=Ready)](https://waffle.io/fullstackla/fullstackla.github.io)
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
[Github pages]: https://pages.github.com/

## To Add Future Events to the Main Site:

1. Go to the `_events` folder with the `$ cd _events` command in the Terminal.

2. Use the `$ touch` command in the Terminal to create a new markdown file with the following name syntax: `year-month-day-name.md`. For example, you can name the file: `$ touch 2016-09-21-mapillary.md`. 

3. The first thing that must appear in the file is a [YAML front matter block](https://jekyllrb.com/docs/frontmatter/). It's a block that opens with three `---` dashes and closes with three `---` dashes. The inside of the block should contain the information below. **Make sure to specify in the layout** whether it's an ongoing event by entering `os-repeat-event` or a onetime event by entering `os-single-event`.
<pre>`---`
layout: **os-repeat-event** or **os-single-event**
title: 
event-date: 
location: can be geolocation formatted as [34.056446, -118.253927]
location-name: 
parking: info should be an html file located in **events/parking** dir
tag-line: 
rsvp: link to FSLA meetup.com URL event page
image: place image assets in **/img/events** dir
`---`</pre>

4. There should be one space between the closing `---` dashes and the first sentence of the body. Enter a brief description of the event. It should have:

    + A few sentences describing the event, with an external link to the speaker/event.
    + Additional instructions for the event (if any).

5. Save the file and voilà, you've created a new event on the FSLA website! 👍👏
