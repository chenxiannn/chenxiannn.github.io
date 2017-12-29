---
layout: default
---

<body>
  <div class="container">
        <div class="web-logo">
            <a href="/about.html"><img src="/images/Logo.png"/></a>
        </div>
        <div class="panel panel-default">
            <div class="panel-heading">博客</div>
            <!-- List group -->
            {% for post in site.categories.blog %}
                <li class="list-group">
                  <a href="{{ post.url }}" class="list-group-item title">{{ post.title }}</a>
                </li>
            {% endfor %}
        </div>
        <div align="center">
            <small>觅知圈@2018 无数科技</small>
            <small>京ICP备17043614号-3</small>
        </div>
    </div>
</body>
