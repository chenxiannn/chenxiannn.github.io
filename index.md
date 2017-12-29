---
layout: default
---

<body>
  <div class="container">
        <div class="web-logo">
            <a href="/about.html"><img src="/images/Logo.png"/></a>
        </div>
        <div class="panel panel-default">
            <!-- List group -->
            {% for post in site.categories.blog %}
                <ul class="list-group">
                  <li class="list-group-item title"><a href="{{ post.url }}" target="_blank">{{ post.title }}</a></li>
                </ul>
            {% endfor %}
        </div>
        <div align="center">
            <small>觅知圈@2018 无数科技</small>
            <small>京ICP备17043614号-3</small>
        </div>
    </div>
</body>
