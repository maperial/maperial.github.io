---
layout: page
title: From Grid to Animation
tags:
- codepen
- api
twitter: "Animation: http://bit.ly/1xbTGCj under-5 mortality rate since 1950 @UNICEF @WHO @WorldBank @WeCanEndPoverty #dataoftheday #Promise4Children"
---

I've downloaded under-five mortality rate [data](http://data.unicef.org/child-mortality/under-five) from Unicef ([xlsx](http://data.unicef.org/download.php?file=U5MR_mortality_rate_39_39.xlsx&type=topics)), containing all numbers by countries from 1950.

After having converted it to GeoJson and added latitude/longitude for every 'Feature', the data is ready to be used with Maperial : 26 javascript lines draw the dynamical map and animate the data over the years.


<p data-height="450" data-theme-id="10317" data-slug-hash="XJNLxM" data-default-tab="result" data-user="chrisdugne" class='codepen'>See the Pen <a href='http://codepen.io/chrisdugne/pen/XJNLxM/'>Maperial animation : Under five mortality rate since 1950</a> by Chris (<a href='http://codepen.io/chrisdugne'>@chrisdugne</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
