---
layout: page
title: Epi Projekte
permalink: /epiprojects/
tag: Projekt
---

<div class="container">
	<div class="row">
	{% if site.posts.size > 0 %}
		{% for post in site.posts %}
			{% if post.tags contains page.tag %}
				{% include projekte-content.html %}
			{% endif %}
		{% endfor %}
	{% endif %}
	</div>
</div>
