---
layout: page
---

[Linkedkin](https://www.linkedin.com/in/rafalbachorz/)

[Github](https://github.com/rafalbachorz)

[Twitter](https://twitter.com/RafalBachorz)

[Gists](gists_pieces.md)

<ul>
    {% for post in paginator.posts %}
      <li>
          <h2><a href="{{ post.url | prepend: site.baseurl | replace: '//', '/' }}">{{ post.title }}</a></h2>
          <time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date_to_string }}</time>
          <p>{{ post.content | strip_html | truncatewords:50 }}</p>
      </li>
    {% endfor %}
</ul>