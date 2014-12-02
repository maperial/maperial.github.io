---
layout: page
title: Getting Started
---

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

- any [Layer](/concepts#layers)
- any other [MapView](./concepts.md#mapview)
- any [Data](/concepts#data)
- any [Tool](/concepts#tools)

For example, ask for a new layer :
{% highlight js %}
map.addMapquest();
{% endhighlight %}

Well, you got your first map !

<p data-height="450" data-theme-id="10317" data-slug-hash="yyyYVr" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/yyyYVr/'>Maperial : Your first map</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
