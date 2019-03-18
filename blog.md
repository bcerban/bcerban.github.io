---
layout: default
title: Blog
permalink: /blog/
---

<!-- blog -->
<section class="blog py-5" id="blog">
	<div class="container py-3">
		<h3 class="heading">Blog</h3>
		<div class="row blog-grids">
			<div class="col-lg-7">
				<h4 class="left-grid-blog">I write beautiful things</h4>
				<p class="left-grid-blog">Nulla viverra pharetra sem, eget pulvinar neque pharetra ac int. lorem ipsum Vestibulum. placerat placerat dolor. Vestibulum at dui nunc.</p>
			</div>
		</div>
		<ul>
			<div class="row">
			{% for post in site.posts %}
				<div class="col-lg-4 col-md-6 w3ls">
					<div class="blog-grid1">
						<h5>{{ post.date | date_to_string }}</h5>
						<h4>{{ post.title }}</h4>
						<p>{{ post.content | strip_html | truncate: 100, '...' }}</p>
						<a href="{{ post.url }}">Read More </a>
					</div>
				</div>	
			{% else %}
				<h4 class="left-grid-blog">No posts available yet!</h4>
			{% endfor %}
			</div>
		</ul>
	</div>
</section>
<!-- //blog -->