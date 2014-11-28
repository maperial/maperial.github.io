---
layout: page
title: Concepts
---

# Main concepts

You'll find here how to use Maperial to create maps and layers,
how to manipulate your data and how to add tools to your maps.

You may want to check some [examples](http://codepen.io/chrisdugne/) before anything.

Once you're ready to go further, explore the complete
API [documentation](/documentation).

Ok let's go !



# Maperial

Instanciate and use **one** single Maperial to build every map on your web page.
{% highlight js %}
var maperial = new Maperial();
{% endhighlight %}

With your maperial you can now :
- Draw [MapViews](#mapviews)
- Share [Data](#data)
- Attach [Tools](#tools)



# MapViews

There are 5 types of MapView :
- a [Map](#map)
- an [Anchor](#anchor)
- a [Lens](#lens)
- a [Magnifier](#magnifier)
- a [Minifier](#minifier)

If you don't specify layers on a child MapView, it will use the same ones as
the parent MapView.



### Map

A Map is the parent of all other types of MapView.

Use your *maperial* to create maps, then you will be able to attach every other
type of [MapView](#mapviews) to a Map.

Each Map is linked with an html container :
{% highlight js %}
var map = maperial.createMap({
    container: 'map1'
});
{% endhighlight %}

Therefore, you will need an html tag for every map in your web page. Here is
the container for the previous map.
{% highlight html %}
<div id="map1"></div>
{% endhighlight %}

Read [more](/documentation/Maperial.html#createMap)...
about the options




### Anchor
An Anchor is the exact same thing as a [Map](#map), but instead of attaching it
to a html container, you place it inside a [MapView](#mapviews).

{% highlight js %}
var anchor = map.addAnchor(options);
{% endhighlight %}

- Require a [theme](#theme)
- Example on [codepen](http://codepen.io/chrisdugne/pen/VYYbEv?editors=101)
- Read [more](/documentation/Maperial.html#addAnchor)
about the options





### Lens
A Lens is a view to zoom in your map, centered on where the Lens is placed.
A Lens allows to highlight a part of map using a different zoom.

{% highlight js %}
var lens = map.addLens(options);
{% endhighlight %}

Use options to set it fixed or draggable, its size, position etc...

- Require a [theme](#theme)
- Example : @todo jsbin + link
- Read [more](/documentation/Maperial.html#addLens)
about the options




### Magnifier
A Magnifier is a view to zoom in your map, with the same center.

{% highlight js %}
var magnifier = map.addMagnifier(options);
{% endhighlight %}

Use options to set it fixed or draggable, its size, position etc...

- Require a [theme](#theme)
- Example : @todo jsbin + link
- Read [more](/documentation/Maperial.html#addMagnifier)
about the options




### Minifier
A Minifier is a view to zoom out your map, with the same center.

{% highlight js %}
var minifier = map.addMinifier(options);
{% endhighlight %}

Use options to set it fixed or draggable, its size, position etc...

- Require a [theme](#theme)
- Example : @todo jsbin + link
- Read [more](/documentation/Maperial.html#addMinifier)
about the options




# Layers

- You may add and remove any layers to any [MapView](#mapviews).
- Each Layer may contain either [Images](#image-layers) or [Data](#data-layers).
- Use [Fusion](#fusion) to merge your layers with custom settings
and draw unique maps.



## Image Layers
- todo : thumbnails + links to /doc

#### External layers
- view.addOCMTransport()
- view.addOCMLandscape()
- view.addWatercolor()
- view.addMapquest()
- view.addSatellite()

#### Maperial layers

###### Shade
- view.addShade()

###### City lights at night
- view.addEarthLight()

- view.addAerosol()
- view.addNDVI()
- view.addSRTM()
- view.addSST()
- todo : maperialOSM

#### WMS Layers
- todo : few examples




## Data Layers
Before to add data layers, you need to create your [Data](#data) first.

Then you can attach it to any [MapView](#mapviews) by adding a layer
depending on the data type :

- view.addDynamicalLayer(data, options);
- view.addHeamapLayer(data, options);

@todo : links to /doc



## Fusion
Use custom settings to fuse 2 layers
@todo settings panel + doc

- AlphaBlend (param float [0,1])
- AlphaClip  (param float [0,1])
- XBlend

You can allow users to change your settings manually by including the
Fusion Settings [tool](#fusion-settings)




# Data

#### Types
- [DynamicalData](/documentation/DynamicalData.html)
allows to add/remove points with custom properties.
  ([Codepen example](http://codepen.io/chrisdugne/pen/ZYYWbx?editors=101))

- [HeatmapData](/documentation/HeatmapData.html)
allows to draw heatmaps with custom colorbars.
  ([Codepen example](http://codepen.io/chrisdugne/pen/Wbbggr?editors=101))

#### Sharable
You may create one Data and apply it on many [data layers](#data-layers).

Then, adding one point on this Data would display the point on every layer.

- @todo : Example sharing data on 2 maps : jsbin + link

#### GeoJson
Use <a href="http://geojson.org">GeoJson</a> to represent your Data.

Check the different [types](#types) of data
to set your Feature Collections accordingly.



# Tools

#### Simple Zoom
You can add +/- buttons in a container, and attach this tool
to a set of MapViews

{% highlight js %}
maperial.addSimpleZoom(options)
{% endhighlight %}

- Require a [theme](#theme) on your page
- @todo : Example on [codepen](http://codepen.io/chrisdugne)
- Read [more](/documentation/Maperial.html#addSimpleZoom)
about the options




#### Slider Zoom
@todo : (1-18 slider and +/- buttons)
  maperial.addSliderZoom(options)



#### Fusion settings
@todo




#### Shade controls
Play with your [shade](#shade) dynamically by using 4 sliders modifying :
- The light x,y and z
- The shade scale.

{% highlight js %}
maperial.addShadeControls({
    layer : shadeLayer
});
{% endhighlight %}

- Require a [theme](#theme) on your page
- Example on [codepen](http://codepen.io/chrisdugne/pen/qEEYRp?editors=101)
- Read [more](/documentation/Maperial.html#addShadeControls) about the options



#### Theme
Most of the tools require a default theme, provided by this css :
{% highlight html %}
<link href="http://static.maperial.com/css/maperial.css" rel="stylesheet" type="text/css" />
{% endhighlight %}
