---
layout: page
title: Getting Started
---

# Getting started
First of all, add the js script on your page
{% highlight html %}
<script src="http://static.maperial.com/js/maperial.js" type="text/javascript"></script>
{% endhighlight %}

Now add your html container
{% highlight html %}
<div id="map"></div>
{% endhighlight %}

Call upon Maperial

{% highlight js %}
var maperial = new Maperial();
{% endhighlight %}

Use it to add a view, linked with your html container

{% highlight js %}
var map = maperial.createMap({
    container: 'map'
});
{% endhighlight %}

Now you can add to your map :
- any [Layer] (./concepts.md#layers)
- any other [MapView] (./concepts.md#mapview)
- any [Data] (./concepts.md#data)
- any [Tool] (./concepts.md#tools)

For example, ask for a new layer :
{% highlight js %}
map.addMapquest();
{% endhighlight %}

Well, you got your first map !

Check the full example on this
[codepen](http://codepen.io/chrisdugne/pen/yyyYVr?editors=101)
