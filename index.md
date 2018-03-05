---
layout: main
---
<link rel="stylesheet" href="assets/css/lightslider.css" />
    <style>
        ul{list-style: none outside none;padding-left: 0;margin: 0;}
        .demo .item{margin-bottom: 60px;}
        .content-slider li{background-color: #ed3020;text-align: center;color: #FFF;}
        .content-slider h3{margin: 0;padding: 70px 0;}
        .demo{width: 800px;}
    </style>
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js"></script>
    <script src="assets/js/lightslider.js"></script>
    <script>
        $(document).ready(function() {
			$("#content-slider").lightSlider({
                loop:true,
                keyPress:true
            });
            $('#image-gallery').lightSlider({
                gallery:true,
                item:1,
                thumbItem:9,
                slideMargin: 0,
                speed:500,
                auto:true,
                loop:true,
                onSliderLoad: function() {
                    $('#image-gallery').removeClass('cS-hidden');
                }  
            });
        });
    </script>
<main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
    <div class="demo">
        <div class="item">
            <div class="clearfix" style="max-width:474px;">
                <ul id="image-gallery" class="gallery list-unstyled cS-hidden">
                    <li data-thumb="assets/img/thumb/cS-1.jpg">
                    <li data-thumb="assets/img/thumb/cS-2.jpg">
                    <li data-thumb="assets/img/thumb/cS-3.jpg">
                    <li data-thumb="assets/img/thumb/cS-4.jpg">
                    <li data-thumb="assets/img/thumb/cS-5.jpg">
                </ul>
            </div>
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
