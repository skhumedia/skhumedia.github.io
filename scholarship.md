---
layout: scholarship
title: 학보사
description: 학보사 컨텐츠
permalink: /scholarship/
---
<center><h1><strong>학보사</strong></h1></center>
<center>
<h4><a href=""><strong>컨텐츠 1</strong></a></h4>
<h4><a href=""><strong>컨텐츠 2</strong></a></h4>
<h4><a href=""><strong>컨텐츠 3</strong></a></h4>
</center>
<hr/>
<div>
<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div id="grid" class="row flex-grid">
    {% for post in site.posts %}
        <article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
            <span class="category">
                <a href="{{ site.url }}{{ site.baseurl }}/categoria/{{ post.category }}">
                    <span>{{ post.category }}</span>
                </a>
            </span>
            <div class="box-body">
                {% if post.image %}
                    <div class="cover">
                        {% include new-post-tag.html date=post.date %}
                        <a href="{{ post.url | prepend: site.baseurl }}" {%if isnewpost %}class="new-post"{% endif %}>
                            <img src="assets/img/placeholder.png" data-url="{{ post.image }}" class="preload">
                        </a>
                    </div>
                {% endif %}
                <div class="box-info">
                    <meta itemprop="datePublished" content="{{ post.date | date_to_xmlschema }}">
                    <time itemprop="datePublished" datetime="{{ post.date | date_to_xmlschema }}" class="date">
                        {% include date.html date=post.date %}
                    </time>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <h2 class="post-title" itemprop="name">
                            {{ post.title }}
                        </h2>
                    </a>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <p class="description">{{ post.introduction }}</p>
                    </a>
                    <div class="tags">
                        {% for tag in post.tags %}
                            <a href="{{ site.baseurl}}/tags/#{{tag | slugify }}">{{ tag }}</a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </article>
    {% endfor %}
    </div>
</main>
</div>
<hr/>
<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div id="grid" class="row flex-grid">
    {% for post in site.posts %}
        <article class="box-item" itemscope="itemscope" itemtype="http://schema.org/BlogPosting" itemprop="blogPost">
            <span class="category">
                <a href="{{ site.url }}{{ site.baseurl }}/categoria/{{ post.category }}">
                    <span>{{ post.category }}</span>
                </a>
            </span>
            <div class="box-body">
                {% if post.image %}
                    <div class="cover">
                        {% include new-post-tag.html date=post.date %}
                        <a href="{{ post.url | prepend: site.baseurl }}" {%if isnewpost %}class="new-post"{% endif %}>
                            <img src="assets/img/placeholder.png" data-url="{{ post.image }}" class="preload">
                        </a>
                    </div>
                {% endif %}
                <div class="box-info">
                    <meta itemprop="datePublished" content="{{ post.date | date_to_xmlschema }}">
                    <time itemprop="datePublished" datetime="{{ post.date | date_to_xmlschema }}" class="date">
                        {% include date.html date=post.date %}
                    </time>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <h2 class="post-title" itemprop="name">
                            {{ post.title }}
                        </h2>
                    </a>
                    <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">
                        <p class="description">{{ post.introduction }}</p>
                    </a>
                    <div class="tags">
                        {% for tag in post.tags %}
                            <a href="{{ site.baseurl}}/tags/#{{tag | slugify }}">{{ tag }}</a>
                        {% endfor %}
                    </div>
                </div>
            </div>
        </article>
    {% endfor %}
    </div>
</main>