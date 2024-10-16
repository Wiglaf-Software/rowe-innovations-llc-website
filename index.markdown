---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

# About

<p style="float:right"><img src="./rowe-innovations-llc-square-gray.png" width="100px"></p>

Rowe Innovations, LLC is the intellectual property holder of works by James Rowe.

Check out some of my projects below.

## Books

{% for book in site.books %}
  <p>
    <a href="{{ book.url }}">
      {{ book.title }}
    </a>
  </p>
  <p>{{ book.excerpt | markdownify }}</p>
{% endfor %}

## Software

{% for app in site.software %}
  <p>
    <a href="{{ app.url }}">
      {{ app.title }}
    </a>
  </p>
  <p>{{ app.excerpt | markdownify }}</p>
{% endfor %}

## Doing Business As/AKA

I also do business under trade names as needed.

<p><a href="https://www.omtstudios.com">OMT Studios&trade;</a></p>
<p>A multi-media content production company. Lessons in persistence.</p>

<p><a href="https://www.wiglafsoftware.com">Wiglaf Software&trade;</a></p>
<p>My first technical skill; software engineering. Oath of Devotion.</p>

## Company Updates

<div class="home post-list">
  {%- if site.posts.size > 0 -%}
    {%- for post in site.posts -%}
    <div class="post-item">
      {%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
      <div class="post-flex-container">
        <div class="post-left">
          <div class="post-title">
            <a class="post-link" href="{{ post.url | relative_url }}">
              {{ post.title | escape }}
            </a>
          </div>
          <div class="post-tags">
            {% for tag in post.tags %}
              <span class="post-tag">{{ tag }}</span>
            {% endfor %}
          </div>
        </div>
        <div class="post-date">
          <span class="post-meta">{{ post.date | date: date_format }}</span>
        </div>
      </div>
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </div>
    {%- endfor -%}
  {%- endif -%}

</div>

## More about the owner

<p><a href="https://www.jsrowe.com">James' Thoughts</a></p>
<p>My personal blog where I publish short posts, primarily technology and personal.</p>