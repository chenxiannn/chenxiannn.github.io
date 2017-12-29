---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="index-content">
      <ul class="artical-list">
        {% for post in site.categories.blog %}
        <li>
          <a href="{{ post.url }}" class="title">{{ post.title }}</a>
          <div class="title-desc">{{ post.description }}</div>
        </li>
        {% endfor %}
      </ul>
    </div>
  </div>
  <div class="container">
        <div class="web-logo">
            <a href="/about.html"><img src="/images/Logo.png"/></a>
        </div>
        <div class="panel panel-default">
            <div class="panel-heading">博客</div>
            <!-- List group -->
             {% for post in site.categories.blog %}
                <li>
                  <a href="{{ post.url }}" class="title">{{ post.title }}</a>
                  <div class="title-desc">{{ post.description }}</div>
                </li>
            {% endfor %}
        </div>
        <div align="center">
            <small>觅知圈@2018 无数科技</small>
            <small>京ICP备17043614号-3</small>
        </div>
    </div>
</body>
