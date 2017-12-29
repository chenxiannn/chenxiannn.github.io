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
        <div class="web-logo">
            <a href="/about.html"><img src="/images/Logo.png"/></a>
        </div>
        <div class="panel panel-default">
            <!-- List group -->
            <ul class="list-group">
            {% for cat in site.categories 
                for post in cat%}
                    <li class="list-group-item title"><a href="{{ post.url }}" target="_blank">{{ post.title }}</a></li>
                {% endfor 
            endfor %}
            </ul>
        </div>
        <div class="footer-info">
            觅知圈@2018 无数科技 京ICP备17043614号-3
        </div>
    </div>
</body>
