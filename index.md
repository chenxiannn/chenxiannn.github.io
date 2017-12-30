---
layout: default
---

<body>
    <script>
        if (/mobile/i.test(navigator.userAgent) || /android/i.test(navigator.userAgent))
        {
            document.body.classList.add('mobile');
        }
    </script>
  <div class="outer">
        {% include header.html %}
        <div class="panel panel-default">
            <!-- List group -->
            <ul class="list-group">
                {% for post in site.categories.blog %}
                <li class="list-group-item title"><a href="{{ post.url }}" target="_blank">{{ post.title }}</a></li>
                {% endfor %}
                {% for post in site.categories.the-little-heat-design %}
                <li class="list-group-item title"><a href="{{ post.url }}" target="_blank">{{ post.title }}</a></li>
                {% endfor %}
            </ul>
        </div>
        <div class="footer-info">
            觅知圈@2018 无数科技 京ICP备17043614号-3
        </div>
    </div>
</body>
