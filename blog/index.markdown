---
layout: default
---

<!-- I need a script to populate this body section with the 3 Latest Posts -->
<h1>Latest 3 Blog Posts</h1>
<h2>{{ site.posts[0].title }}</h2>
{{ site.posts[0].content }}
<h2>{{ site.posts[1].title }}</h2>
{{ site.posts[1].content }}
<h2>{{ site.posts[2].title }}</h2>
{{ site.posts[2].content }}

<div class="wrapper">
      <nav>
        <ul>
        <li class="active"><a href="/lorman-online-portfolio/">Homepage</a></li>
        <!-- I need a script to populate this navbar list with each CATEGORY-2 of Posts -->
        {% for categ in site.categ_list %}
        <li class="active"><a href="/lorman-online-portfolio/blog/{{ categ }}">{{ categ }}</a></li>
        {% endfor %}
        </ul>
      </nav>
</div>