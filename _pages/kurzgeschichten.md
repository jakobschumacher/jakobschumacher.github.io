---
layout: page
title: Geschichten
permalink: /geschichten/
---

<div class="container">
	<div class="row">
	{% if site.posts.size > 0 %}
		{% for post in site.posts %}
			{% include article-content.html %}
		{% endfor %}
	{% endif %}
	</div>
</div>
