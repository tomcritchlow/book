---
---
<head>
    <script src="https://unpkg.com/pagedjs/dist/paged.polyfill.js"></script>
</head>

<body>

{% for section in site.data.structure %}
    {% for chapter in section %}

        {% assign post = site.chapters | where:"url", chapter.url  | first %}

        {{post.content}}

    {% endfor %}
{% endfor %}

</body>