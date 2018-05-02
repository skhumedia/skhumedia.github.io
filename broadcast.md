---
layout: broadcast
title: 방송국
description: 방송국 컨텐츠
permalink: /broadcast/
---

<center><h1><strong>방송국</strong></h1></center>

<main class="home" id="broadcast-post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div id="grid" class="row flex-grid">
    {% for broadcast-post in site.posts %}
        <article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
            <span class="category">
                <a href="{{ site.url }}{{ site.baseurl }}/categoria/{{ broadcast-post.category }}">
                    <span>{{ broadcast-post.category }}</span>
                </a>
            </span>
            <div class="box-body">
                {% if post.image %}
                    <div class="cover">
                        {% include new-post-tag.html date=broadcast-post.date %}
                        <a href="{{ broadcast-post.url | prepend: site.baseurl }}" {%if isnewpost %}class="new-post"{% endif %}>
                            <img src="assets/img/placeholder.png" data-url="{{ broadcast-post.image }}" class="preload">
                        </a>
                    </div>
                {% endif %}
                <div class="box-info">
                    <meta itemprop="datePublished" content="{{ broadcast-post.date | date_to_xmlschema }}">
                    <time itemprop="datePublished" datetime="{{ broadcast-post.date | date_to_xmlschema }}" class="date">
                        {% include date.html date=broadcast-post.date %}
                    </time>
                    <a class="post-link" href="{{ broadcast-post.url | prepend: site.baseurl }}">
                        <h2 class="broadcast-post-title" itemprop="name">
                            {{ broadcast-post.title }}
                        </h2>
                    </a>
                    <a class="post-link" href="{{ broadcast-post.url | prepend: site.baseurl }}">
                        <p class="description">{{ broadcast-post.introduction }}</p>
                    </a>
                    <div class="tags">
                        {% for tag in broadcast-post.tags %}
                            <a href="{{ site.baseurl}}/tags/#{{tag | slugify }}">{{ tag }}</a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </article>
    {% endfor %}
    </div>
</main>
