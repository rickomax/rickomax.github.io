---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Welcome
title_nav: Home
permalink: /
projects:
  -
    title: The Varginha Incident
    url: /varginha-incident/
    image: /assets/img/varginha-incident-preview.png
    description: Hello world
  -
    title: PSXPrev
    url: /psxprev/
    image: /assets/img/psxprev-preview.png
    description: Hello world
---
You can either add links to landing pages for individual programs/games here, or add them to the navbar, or both. Or make a Projects page in the navbar that lists them.

***

### [The Varginha Incident](/varginha-incident/)
The Varginha Incident (Alien Anarchy) game port made in Unity 3D

***

### [PSXPrev](/psxprev/)
PlayStation (PSX) Files Previewer/Extractor

***

<!-- ## Projects

* [PSXPrev](/psxprev/)
* [The Varginha Incident](/varginha-incident/) -->

<!-- {%- if page.projects.size > 0 -%}
  <ul class="post-list project">
    {%- for projects in page.projects -%}
    <li>
      <div class="image"><img src="{{ projects.image | relative_url }}"></div>
      <div class="info">
        <h3>
          <a class="post-link" href="{{ projects.url | relative_url }}">
            {%- comment -%}
            <!-- We do the split here just so long library names with dots in them wrap. --!>
            {%- endcomment -%}
            {{ projects.title | escape | split: '.' | join: '.<wbr>'}}
          </a>
        </h3>
        <p>{{ projects.description | escape }}</p>
      </div>
    </li>
    {%- endfor -%}
  </ul>
{%- endif -%} -->

<!-- {%- if page.projects.size > 0 -%}
  <ul class="post-list">
    {%- for post in page.projects -%}
    <li>
      <h3>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
      </h3>
        <p>{{ post.description | escape}}</p>
    </li>
    {%- endfor -%}
  </ul>

{%- endif -%} -->

##### (Preview the [404 page here](/404.html))
