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
  - image_path: /assets/images/Semaje_bulb.png
    alt: "shrink"
    title: '<a href="/vol2-1/PIP-412031RC007/">Determining the interplanar spacing of graphite using electron diffraction</a>'
    excerpt: '**Rapid Communication** <br> *Author*: Sema''Je Farmer'
  - image_path: /assets/images/BV_interferometer.png
    alt: "Cosmic Microwave Background"
    title: '<a href="/vol2-1/PIP-412022RC009/">Riding the wave: determining laser wavelength using a Michelson interferometer</a>'
    excerpt: '**Rapid Communication** <br> *Author*: Brookelyn Velmont'
  - image_path: /assets/images/SF_interferometer.jpg
    alt: "Discrete Electron Charge"
    title: '<a href="/vol2-1/PIP-412038RC024/">
Dispersing doubt: how wavelength affects refraction</a>'
    excerpt: '**Rapid Communication** <br> *Author*: Skylar Farr'
---

{% include feature_row id="feature_row" type="right"%}

# Highlights from the latest issue
Featuring rapid communications and original articles that stand out from the crowd.

<p><a href="/vol2-1/highlights/" class="btn btn--primary"> Explore all Editor's Suggestions</a></p>

{% include feature_row id="feature_row3" class="teaser-shrink" h2="true" %}

# Collections in our latest issue
{% assign feature_row = site.data.sections["vol2-1"] %}
{% include feature_row assigned="true" uselabel="true" class="teaser-shrink" column="true"%}