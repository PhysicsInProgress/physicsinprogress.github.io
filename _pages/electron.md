---
layout: single
classes: wide
section: "Historic electron measurements"
permalink: "/vol1-1/historic-electron-measurements/"
title: "Historic electron measurements"
tagline: "Some stuff about electrons"
header:
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
# {{page.title}}

{% assign posts = site.vol1_1 | where: "section", page.section %}
{% for post in posts%}

	{% capture colstring%} {% cycle "one","two"%} {% endcapture %}	
	{% include article_feature.html color=colstring%}

{% endfor %}
<p align="center">
	<a href="" class="btn btn--light-outline btn--large"> 
		&larr;
	</a>
	&nbsp;
	<a href="/vol1-1/index/" class="btn btn--inverse btn--large"> 
		Return to collection
	</a>
	&nbsp;
	<a href="/vol1-1/waves-and-optics/" class="btn btn--primary btn--large"> 
		&rarr;
	</a> 
</p>