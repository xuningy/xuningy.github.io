---
layout: default
title: All Publications
title_align: left
---

<p class="pub-legend"><span>* equal contribution</span><span>† project lead</span><span>‡ equal advising</span></p>

<div class="pub-list">
{% for p in site.data.papers %}{% include paper.html paper=p %}{% endfor %}
</div>
