---
title: "Blog"
layout: home
permalink: /blog/
author_profile: true
---

Welcome to my blog. Here you'll find articles covering clinical oncology, medical education, research, and personal adventures.

## Browse by Category

<div class="feature__wrapper">
<div class="feature__item">
  <div class="archive__item">
    <h2><a href="/blog/ctDNA/">ctDNA</a></h2>
    <p>Ongoing clinical research in circulating tumor DNA.</p>
  </div>
</div>
<div class="feature__item">
  <div class="archive__item">
    <h2><a href="/blog/AI-education/">AI Education</a></h2>
    <p>Ongoing projects in educating physicians in the effective use of AI.</p>
  </div>
</div>
<div class="feature__item">
  <div class="archive__item">
    <h2><a href="/blog/reading/">Reading</a></h2>
    <p>Personal reading on latest journal articles.</p>
  </div>
</div>
<div class="feature__item">
  <div class="archive__item">
    <h2><a href="/blog/PRS/">PRS</a></h2>
    <p>Old blog postings on PRS research from 2022.</p>
  </div>
</div>
</div>

---

## Recent Posts

{% include base_path %}

{% capture written_year %}'None'{% endcapture %}

{% for post in site.categories.clinical %}

  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}

  {% if year != written_year %}

    <h2 id="{{ year | slugify }}" class="archive__subtitle">{{ year }}</h2>

    {% capture written_year %}{{ year }}{% endcapture %}

  {% endif %}

  {% include archive-single.html %}

{% endfor %}
