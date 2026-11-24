---
layout: page
permalink: /blog/
title: blog
description: Short notes and thoughts.
nav: true
nav_order: 1
---

<!-- Blog index: only cards. Each card opens the full post. -->
<div class="row row-cols-1 row-cols-md-2 blog-cards">
  {% assign posts = site.posts | sort: "date" | reverse %}
  {% for post in posts %}
    {% if post.redirect %}
      {% assign post_url = post.redirect | relative_url %}
    {% else %}
      {% assign post_url = post.url | relative_url %}
    {% endif %}
    <div class="col mb-4">
      <a href="{{ post_url }}" class="blog-card-link">
        <div class="card h-100 hoverable">
          {% if post.thumbnail %}
            <img src="{{ post.thumbnail | relative_url }}" class="card-img-top" alt="{{ post.title }}">
          {% endif %}
          <div class="card-body">
            <p class="card-date">{{ post.date | date: '%B %d, %Y' }}</p>
            <h2 class="card-title">{{ post.title }}</h2>
            <p class="card-text">
              {% if post.description %}{{ post.description }}{% else %}{{ post.excerpt | strip_html | truncatewords: 30 }}{% endif %}
            </p>
            {% if post.tags.size > 0 %}
              <p class="card-tags">
                {% for tag in post.tags %}<span><i class="fa-solid fa-hashtag fa-sm"></i> {{ tag }}</span> {% endfor %}
              </p>
            {% endif %}
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

{% if site.posts.size == 0 %}
  <p>No posts yet.</p>
{% endif %}

<style>
  .blog-card-link, .blog-card-link:hover { text-decoration: none; color: inherit; }
  .blog-cards .card { border-radius: 8px; transition: transform .15s ease; }
  .blog-cards .card:hover { transform: translateY(-3px); }
  .blog-cards .card-title { font-size: 1.25rem; margin-bottom: .5rem; }
  .blog-cards .card-date { font-size: .8rem; color: var(--global-text-color-light); margin-bottom: .25rem; }
  .blog-cards .card-tags { font-size: .8rem; color: var(--global-theme-color); margin: 0; }
  .blog-cards .card-img-top { height: 160px; object-fit: cover; }
</style>
