---
layout: page
title: About Maperial
---

# Maperial : a new way to create maps

Maperial is a free javascript API to create *dynamical* maps for your web
applications.

Configure your own set of layers and parameters to visualize, analyze, and understand your data.

For now we stick on enhancing this API and hope to see a community
gathering around, which would mean we are on the right path to provide a new
map tool.

Enjoy drafting and sharing your maps, and don't forget
to let us know your feedback !

# Let me play !
- Get [started](#getting-started) with a first map
- Check out a whole bunch of Codepen [examples](http://codepen.io/chrisdugne/)
- Understand [Maperial](./concepts.md)'s concepts
- Explore the complete API [reference](http://static.maperial.com/doc)
to draft your own maps.



# The 3 Maperial's keys

### The ability to style your basemaps quickly and easily.

Meaning to give the roads your prefered color and size, change the forests' color, fonts...

Maperial innovates by rendering all this on client side. Interesting services like CloudMade or Mapbox help you style your maps as well, but forget about the ergonomy, and the speed as their images are built server side berfore to be sent to the client.

Maperial sends directly vectorial data to the client, and uses javascript to render the maps on the user's computers (alike GeoJson).

The user can therefore see instant changes on the basemap styles or data and the UX is enhanced more than ever.

### The ability to fuse layers with purpose.

Contrary to MapBox, GoogleMap API or GoogleEarth's alphablending fuse, Maperial performs beautiful fuse allowing the better basemap visibility, meanwhile emphasing the client's data. You may customize all your layers' fusions (basemaps, satellite images, elevations, your data...)

### Data interpolation from many formats.

In order to display high quality rendering. Definitely better than the classical Mapbox 'heat-map' for instance. You can obviously use many interpolation algorithms to get the broadest display possibilities from the data set (density, isotropy, partitions...)




# Why ?

Three engineers experts on their own domain and interested by geolocalised data rendering, got the idea, motivation and energy to start Maperial.

Today geospatial analysis, georeference and georeferenced data rendering is expanding quickly.

Many quality projects arise or get stronger like OpenSteetMap, CloudMade, Mapbox, CartoDB, GoogleMapAPI...

Only a few of them get interested on scatter plots rendering as raster (image) using high quality algorithms for interpolation.

This is what Maperial brings for you.



# How ?

Maperial is built on a broad technology choice and a real knowledge gathering.

A great number of tools, langages and libraries is used, in every parts of the solution : web application, georeferenced data, calculation development and optimisation.

Maperial's client side is therefore based on javascript and HTML5.

Our maps servers use many python scripts, Tornado and Nginx servers dealing with the numerous requests to Postgres/PostGIS and mongoDB databases.

Interpolation calculations and projections are done with an optimised C++ code using proj4 and GDAL libraries, and validated interpolation algorithms.


# Who is this for ?

Maperial is the tool you need to visualize, question, analyze, interpret, and understand your georeferenced data on 2D basemaps.

We could think of ground quality studies, meteorological data rendering, air quality or water quality data rendering, statistical data rendering (criminality, economy, politics, town planning...)...

Surely there is not enough room to gather here the many domains that could join the list.

Maperial could be used without any data as well, just to draw awesome styled maps with the basemaps we provide and maperial's style editor ergonomy.

The variety of custom styles can be useful to webmasters, teachers (geography, history, biology...), graphists...

Everyone willing to draw a map willing to master its content and rendering !

### Keep in mind Maperial is entirely customisable to suit your needs,

so if you find anything you miss in our API just let us know !

