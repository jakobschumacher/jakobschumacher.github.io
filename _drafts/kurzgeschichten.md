---
layout: page
title: Geschichten
permalink: /geschichten/
tag: Kurzgeschichte
---

<div class="container">
	<div class="row">
	{% if site.posts.size > 0 %}
		{% for post in site.posts %}
		{% if post.tags contains page.tag %}
			{% include article-content.html %}
		{% endif %}
		{% endfor %}
	{% endif %}
	</div>
</div>
