---
layout: category
title: Announcements
tag: annoucements
permalink: /category/announcements/
categories:
- announcements 
---

{% assign categories = site.categories | sort %}
	{% for category in categories %}
		{% assign name = category[0] %}
		{% assign posts = category[1] %}
		{% assign size = posts | size %}
		<section class="category">
				<h3>
					{{ name | replace: "-", " " }}
				</h3>

			<ul>
				{% assign tutorials = posts | sort: "title" %}
					<li><a href="{{ site.baseurl }}{{ tutorial.url }}">{% include document-icon.html icon=tutorial.type %}{{ tutorial.title }}</a></li>
			</ul>
		</section>
	{% endfor %}
