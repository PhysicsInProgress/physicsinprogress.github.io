---
title: "Phys. in Prog. | Home"
layout: splash
classes: wide
permalink: /
date: 2016-03-23T11:48:41-04:00
header:
  overlay_filter: rgba(122,35,47,.8)
  title: "A journal for <i>physicists</i> still in progress"
  overlay_image: "/assets/images/banner.svg"
  image: /assets/images/rubensFeature.jpeg
  actions:
    - label: "Learn More"
      url: "/about/"
excerpt: "Showcasing undergraduate experiments and excellence in scientific writing at Carthage College"
feature_row:
  - title: "For students, by students"
    excerpt: "Physics in Progress features student work, both in the form of rapid communications and original articles. <br> Each contribution was peer-reviewed by students, and the final editorial decisions were made by students. <br>For more about the journal or the peer-review process, explore our about section. "
    url: "/about/"
    btn_label: "About <i>Physics in Progress</i>"
    btn_class: "btn--primary"
    image_path: /assets/images/looking_out.png
    alt: "placeholder image 2"
feature_rowHighlightHead:
  - excerpt: 'Featuring rapid communications and original articles that stand out from the crowd.'
    url: "/highlights/"
    btn_label: "Explore all Editor's Suggestions"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /assets/images/eovermplot.png
    alt: "shrink"
    title: '<a href="/vol1-1/PIP-412018RC045/">Measuring the radius of circular electron beams to determine the charge-to-mass ratio of the electron</a>'
    excerpt: '**Rapid Communication** <br> *Author*: Justin Wheeler'
  - image_path: /assets/images/CMB.png
    alt: "Cosmic Microwave Background"
    title: '<a href="/vol1-1/PIP-412007OA042/">An undergraduate review of general relativity and cosmology</a>'
    excerpt: '**Original Article** <br> *Author*: Andrew Valentini'
  - image_path: /assets/images/electroncharge.png
    alt: "Discrete Electron Charge"
    title: '<a href="/vol1-1/PIP-412015RC038/">Measuring the charge of an electron from the Millikan oil drop experiment</a>'
    excerpt: '**Rapid Communication** <br> *Author*: Kassia Schraufnagel'
---

{% include feature_row id="feature_row" type="right"%}

# Highlights from the latest issue
Featuring rapid communications and original articles that stand out from the crowd.

<p><a href="/highlights/" class="btn btn--primary"> Explore all Editor's Suggestions</a></p>

{% include feature_row id="feature_row3" class="teaser-shrink" h2="true" %}

# Collections in our latest issue
{% assign feature_row = site.data.sections["vol1-1"] %}
{% include feature_row assigned="true" uselabel="true" class="teaser-shrink" column="true"%}