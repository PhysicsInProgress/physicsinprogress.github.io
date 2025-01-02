---
layout: single
classes: wide
permalink: "/vol1-1/highlights/"
title: "Phys. in Prog. | Highlights"
tagline: "High achieving whatever"
EC: TRUE
header:
  title: "Editor's Suggestions from the latest issue"
  overlay_filter: rgba(122,35,47,.8)
  overlay_image: "/assets/images/banner.svg"
sidebar:
  - title: "Physics in Progress"
    image: "/assets/images/RubensFeature.jpeg"
    image_alt: "image"
    text: "**Volume 1**<br>Issue 1<br>January 2024."
    nav: "issuecol"
---
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
{% assign groups = site.vol1_1 | where: "EC",page.EC |group_by: "section" | sort: "name"%}
{% for cat in groups %}{% unless cat.name == ""%}
{% assign f = site.data.sections[cat.name] %}
{% capture colstring%} {% cycle "one","two"%} {% endcapture %}

<div class="section_{{colstring | strip}}_tone">
<h1 id="{{f.label | slugify}}"> {{f.label}} </h1>
<p> {{f.excerpt}} </p>
	{% for page in cat.items %}
		{% assign post = page %}
		
		
		{% include article_feature.html  color=colstring%}
	{% endfor %}
</div>
{% endunless %}{% endfor %}

<div style="display:flex; align-content:center;justify-content:space-around;">
<div style="flex-basis:75%;padding-top:1em;"><a href="/vol1-1/index/" class="btn btn--primary" style="width:100%; text-align:center">Explore the rest of the issue </a></div>
</div>