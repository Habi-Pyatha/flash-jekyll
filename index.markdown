---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
<!-- {% for post in site.posts %}
  <li>
    <span class="post-meta">{{ post.date | date: "%B %d, %Y" }}</span>
    <h3>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
    </h3>
    {%- if site.show_excerpts -%}
      {{ post.excerpt }}
    {%- endif -%}
  </li>
{% endfor %} -->


<!-- {% for category in site.posts%}
    {{category.category}}  
{% endfor %} -->

{% assign all_categories = site.posts | map: "category" | uniq %}
{% for category in all_categories %}

   [{{ category }}]({{site.baseurl}}/{{category}})
  
{% endfor %}

{%include flashcards.html%}




