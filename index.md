---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---

<div class="home-content">
    {%- if site.discloser_articles.size > 0 -%}
    <h2 class="post-list-heading">{{ page.list_title | default: "Discloser Resources" }}</h2>
    <ul class="post-list">
    {%- for post in site.discloser_articles -%}
    <li>
        <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
            {{ post.title | escape }}
        </a>
        </h3>
        {%- if site.show_excerpts -%}
        {{ post.excerpt }}
        {%- endif -%}
    </li>
    {%- endfor -%}
    </ul>

    {%- endif -%}
</div>