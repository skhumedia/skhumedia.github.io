---
layout: main
---
<div style="width: 100%;">
    <div class="content1" style="margin-left: 4%; float: left; width: 50%; height: auto; color: #fff;">
    <center><img src="/assets/img/scholarship/2018_3/사진기획1.jpg" width="100%" height="auto" style="border-radius:5%"></center>
    </div>
    <div class="content2" style="margin-right: 4%; float: right; width: 40%; height: auto; color: #fff; border: 2px solid #fff;">
        <table class="tr" style="font-size: 80%;">
            <tr><td><a href="" style="color:#fff; text-decoration:none;">학부방 4개, 새천년관 1층에 신설</a></td></tr>
            <tr><td><a href="" style="color:#fff; text-decoration:none;">오늘도 평화로에 갑니다.</a></td></tr>
            <tr><td><a href="" style="color:#fff; text-decoration:none;">노랑, 내가 만드는 행복의 공식-조재인</a></td></tr>
            <tr><td><a href="" style="color:#fff; text-decoration:none;">개발자들에게 직접 듣는 종합정보 시스템 이야기</a></td></tr>
            <tr><td><a href="" style="color:#fff; text-decoration:none;">가해자에게 느끼는 연민과 가해자 옹호</a></td></tr>
            <tr><td><a href="" style="color:#fff; text-decoration:none;">3월호 기고</a></td></tr>
        </table>
    </div>
</div>


<!-- 실제 꺼 -->
<!-- <main class="home" id="post" role="main" itemprop="mainContentOfPage" itemscope="itemscope" itemtype="http://schema.org/Blog">
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
</main> -->
