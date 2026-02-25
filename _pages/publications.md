---
layout: page
permalink: /publications/
title: publications
description: (*) denotes equal contribution.
nav: true
nav_order: 1
---
<!-- _pages/publications.md -->
<div class="publications">
{% assign pubs = site.scholar.publications | reverse %}
{% assign pubs_by_year = pubs | group_by: "year" %}
</div>
