---
layout: default
title: "Blog"
description: "Technical articles on industrial welding, mining fabrication, and professional journey. Written by a CWB and AWS certified welder working in Canada."
image: /images/og/wallid-guergour.webp
image_alt: "Wallid Guergour Blog — Industrial Welding & Fabrication"
og_type: website
permalink: /blog/
breadcrumb_name: "Blog"
schema_type: BreadcrumbList
body_class: page
---

<div class="section started section-title" id="section-started">
  <div class="video-bg jarallax" style="background-image: url(/images/bg/hero.webp);">
    <div class="video-bg-mask"></div>
    <div class="video-bg-texture" id="grained_container"></div>
  </div>
  <div class="centrize full-width">
    <div class="vertical-center">
      <div class="started-content">
        <h1 class="h-title">Blog</h1>
        <div class="h-subtitles">
          <div class="h-subtitle">
            <p>Welding · Fabrication · Industry · Journey</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>


{% assign categories = "welding,fabrication,industry,journey" | split: "," %}

{% for cat in categories %}
  {% assign cat_posts = site.posts | where: "category", cat %}
  {% if cat_posts.size > 0 %}

<div class="section about blog-category" id="section-{{ cat }}">
  <div class="title">
    <div class="title_inner">
      <h2>{{ cat | capitalize }}</h2>
    </div>
  </div>

  <div class="blog-grid">
    {% for post in cat_posts %}
    <article class="blog-card">
      <a href="{{ post.url }}" class="blog-card-link">

        <!-- Image -->
        <div class="blog-card-image">
          <img src="{{ post.image | default: '/images/og/wallid-guergour.webp' }}"
               alt="{{ post.image_alt | default: post.title }}"
               loading="lazy">
          <div class="blog-card-label">{{ post.category | upcase }}</div>
        </div>

        <!-- Contenu -->
        <div class="blog-card-content">
          <h3 class="blog-card-title">{{ post.title }}</h3>
          <p class="blog-card-desc">{{ post.description | truncate: 120 }}</p>
          <div class="blog-card-meta">
            <span class="blog-card-date">{{ post.date | date: "%B %d, %Y" }}</span>
            {% if post.read_time %}
            <span class="blog-card-sep">·</span>
            <span class="blog-card-read">{{ post.read_time }} min read</span>
            {% endif %}
          </div>
          <div class="blog-card-cta">
            Read the article <span class="blog-card-arrow">→</span>
          </div>
        </div>

      </a>
    </article>
    {% endfor %}
  </div>
</div>

  {% endif %}
{% endfor %}
