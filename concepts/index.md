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

With your `maperial` you can now :

- Draw [MapViews](#mapviews) with [Layers](#layers)
- Share [Data](#data)
- Attach [Tools](#tools)



# MapViews

A MapView can be either :

- a [Map](#map)
- an [Anchor](#anchor)
- a [Lens](#lens)
- a [Minifier](#minifier)

If you don't specify layers on a child MapView, it will use the same ones as
the parent MapView.



## Map

A Map is the parent of all other types of MapView.

Use your `maperial` to create maps, then you will be able to attach every other
type of [MapView](#mapviews) to a Map.

Each Map is linked with an html container :
{% highlight js %}
var map = maperial.createMap({
    container: 'map1'
});
{% endhighlight %}

Therefore, you will need an html tag for every `map` in your web page. Here is
the container for the previous `map`.
{% highlight html %}
<div id="map1"></div>
{% endhighlight %}

Read more on the [documentation](/documentation/Maperial.html#createMap).




## Anchor
An Anchor is the exact same thing as a [Map](#map), but instead of attaching it
to a html container, you place it inside a [MapView](#mapviews).

{% highlight js %}
var anchor = map.addAnchor(options);
{% endhighlight %}

- Requires a [theme](#theme)
- Read more on the [documentation](/documentation/Maperial.html#addAnchor).

<p data-height="450" data-theme-id="10317" data-slug-hash="myemdv" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/myemdv/'>Maperial : Anchors</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>





## Lens
A Lens is a view to zoom in your map, centered on where the Lens is placed.
A Lens allows to highlight an area using a greater zoom.

{% highlight js %}
var lens = map.addLens(options);
{% endhighlight %}

Use options to set it fixed or draggable, customize the size, position etc...

- Requires a [theme](#theme)
- Read more
on the [documentation](/documentation/Maperial.html#addLens).

<p data-height="450" data-theme-id="10317" data-slug-hash="EaVoVV" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/EaVoVV/'>Maperial : Lens</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Drag the Lens over the Map to see details as you wish !





## Minifier
A Minifier is a view to zoom out your map, with the same center.
It allows to understand where is situated the area using a lower zoom.

{% highlight js %}
var minifier = map.addMinifier(options);
{% endhighlight %}

Use options to set it fixed or draggable, its size, position etc...

- Requires a [theme](#theme)
- Read more on the [documentation](/documentation/Maperial.html#addMinifier).

<p data-height="450" data-theme-id="10317" data-slug-hash="pvjpgB" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/pvjpgB/'>Maperial : Minifier</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

In this example you may drag the Minifier over the Map.


# Layers

- You may add and remove any layers to any [MapView](#mapviews).
- Each Layer may contain either [Images](#image-layers) or [Data](#data-layers).
- Use [Fusion](#fusion) to merge your layers with custom settings
and draw unique maps.



# Image Layers

We provide our own unhackneyed tiles but you may use an evergrowing collection of external tiles.

- [Maperial Tiles](#maperial-tiles)
- Tiles from [Open Street Map](#open-street-map)
- Tiles from [Thunderforest](#thunderforest)
- Tiles from [Stamen](#stamen)
- Tiles from [Mapquest](#mapquest)
- Tiles from numerous [WMS](#wms)

## Maperial tiles

<div class="half">
<h4> Shaded Relief :</h4>

{% highlight js %}
view.addShade()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/shade.jpg" alt="">


<div class="half">
<h4> City lights at night :</h4>

{% highlight js %}
view.addEarthLight()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/earthlight.jpg" alt="">


<div class="half">
<h4> Aerosol :</h4>

{% highlight js %}
view.addAerosol()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/aerosol.jpg" alt="">


<div class="half">
<h4> Normalized Difference Vegetation Index :</h4>

{% highlight js %}
view.addNDVI()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/ndvi.jpg" alt="">


<div class="half">
<h4> Shuttle Radar Topography Mission :</h4>

{% highlight js %}
view.addSRTM()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/srtm.jpg" alt="">


<div class="half">
<h4> Sea Surface Temperature :</h4>

{% highlight js %}
view.addSST()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/sst.jpg" alt="">


<div class="half">
And soon more to come : vectorial layers using Data from
[OpenStreetMap contributors](http://www.openstreetmap.org/copyright)
</div>


## Open Street Map

<div class="half">
<h4> Classic OSM :</h4>

{% highlight js %}
view.addOSM()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/osm.jpg" alt="">


## Thunderforest


<div class="half">
<h4> OpenCycleMap :</h4>

{% highlight js %}
view.addOCM()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/ocm.jpg" alt="">


<div class="half">
<h4> Transport :</h4>

{% highlight js %}
view.addTransport()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/transport.jpg" alt="">


<div class="half">
<h4> Landscape :</h4>

{% highlight js %}
view.addLandscape()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/landscape.jpg" alt="">



<div class="half">
<h4> Outdoors :</h4>

{% highlight js %}
view.addOutdoors()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/outdoors.jpg" alt="">


<div class="half">
<h4> Transport Dark :</h4>

{% highlight js %}
view.addTransportDark()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/transport-dark.jpg" alt="">


Tiles © [Thunderforest](http://www.thunderforest.com/), Data © [OpenStreetMap contributors](http://www.openstreetmap.org/copyright)

## Stamen

<div class="half">
<h4> Watercolor :</h4>

{% highlight js %}
view.addWatercolor()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/watercolor.jpg" alt="">


<div class="half">
<h4> Terrain :</h4>
(Available in the USA only.)

{% highlight js %}
view.addTerrain()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/terrain.jpg" alt="">


<div class="half">
<h4> Toner :</h4>

{% highlight js %}
view.addToner()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/toner.jpg" alt="">


<div class="half">
<h4> Toner background :</h4>

{% highlight js %}
view.addTonerBG()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/toner-bg.jpg" alt="">


## Mapquest

<div class="half">
<h4> Classic :</h4>

{% highlight js %}
view.addMapquest()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/mapquest.jpg" alt="">


<div class="half">
<h4> Satellite :</h4>

{% highlight js %}
view.addSatellite()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/satellite.jpg" alt="">



## WMS

<div class="half">
<h4> Corine Land Cover :</h4>

{% highlight js %}
view.addCorineLandCover()
{% endhighlight %}
</div>
<img class="right" src="/images/layers/corine-land-cover.jpg" alt="">




# Data Layers
Before to add data layers, you need to create your [Data](#data) first.

Then you can attach it to any [MapView](#mapviews) by adding a layer
depending on the data type :

- view.addDynamicalLayer(data, options);
- view.addHeamapLayer(data, options);

@todo : links to /doc


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



# Fusion
Use custom settings to fuse 2 layers
@todo settings panel + doc

- AlphaBlend (param float [0,1])
- AlphaClip  (param float [0,1])
- XBlend

You can allow users to change your settings manually by including the
Fusion Settings [tool](#fusion-settings)



# Tools

#### Simple Zoom
You can add +/- buttons in a container, and attach this tool
to a set of MapViews

{% highlight js %}
maperial.addSimpleZoom(options)
{% endhighlight %}

- Requires a [theme](#theme) on your page
- @todo : Example on [codepen](http://codepen.io/chrisdugne)
- Read more on the [documentation](/documentation/Maperial.html#addSimpleZoom).




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

- Requires a [theme](#theme) on your page
- Example on [codepen](http://codepen.io/chrisdugne/pen/qEEYRp?editors=101)
- Read more on the [documentation](/documentation/Maperial.html#addShadeControls)


#### Theme
Most of the tools require a default theme, provided by this css :
{% highlight html %}
<link href="http://static.maperial.com/css/maperial.css" rel="stylesheet" type="text/css" />
{% endhighlight %}
