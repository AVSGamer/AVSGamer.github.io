---
layout: default
---
<div class="wrapper">
      <nav>
        <ul>
        <li><a href="/lorman-online-portfolio/">Homepage</a></li>
        <li><a href="/lorman-online-portfolio/blog/">Back to Blogs</a></li>
        {% for categ in site.categ_list %}
        <li class="active"><a href="/lorman-online-portfolio/blog/{{ categ }}">{{ categ }}</a></li>
        {% endfor %}
        </ul>
      </nav>
</div>

{% if page.url == "/blog/0-sentiments/" %}
{% assign categ = "0-sentiments" %}
{% endif %}

{% if page.url == "/blog/1-college/" %}
{% assign categ = "1-college" %}
{% endif %}

{% if page.url == "/blog/2-notgametools/" %}
{% assign categ = "2-notgametools" %}
{% endif %}

{% if page.url == "/blog/3-fgorder/" %}
{% assign categ = "3-fgorder" %}
{% endif %}

{% if page.url == "/blog/4-pgraven/" %}
{% assign categ = "4-pgraven" %}
{% endif %}

{% if page.url == "/blog/5-gensokishi/" %}
{% assign categ = "5-gensokishi" %}
{% endif %}

{% if page.url == "/blog/98-changelog/" %}
{% assign categ = "98-changelog" %}
{% endif %}

{% if page.url == "/blog/99-jekylldefault/" %}
{% assign categ = "99-jekylldefault" %}
{% endif %}

<h1>{{categ}} Posts</h1>

{% for item in site.posts %}
{% if item.categories[1] == categ %}
{{ item.content }}
{% endif %}
{% endfor %}
<!-- I need a script to populate this body section with All Posts' Contents from this Category -->