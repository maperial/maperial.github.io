---
layout: page
title: Shade Animation
tags:
- codepen
- api
---

This example allows you to animate a [shade](http://maperial.github.io/concepts/#shade-controls).

Well, you're not on the Moon, this is Mount Fuji : )

<p data-height="450" data-theme-id="10317" data-slug-hash="MYwdap" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/MYwdap/'>Maperial : Shade Controls</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


Add this to play with the fusion controls
{% highlight js %}
maperial.addFusionControls({
  layer : landscape
});
{% endhighlight %}

- Play with the sliders to test the Fusion settings : everything is dynamically refreshed, while the shade animation keeps going on.
- Complete [documentation](/documentation/Maperial.html#addShadeControls) for options.
