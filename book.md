---
---
<head>
    <link href="/css/print.css" rel="stylesheet" type="text/css" />
    
</head>

<body>

{% for section in site.data.structure %}
    {% for chapter in section %}
        
        {% assign post = site.chapters | where:"url", chapter.url  | first %}

        {{post.content}}

    {% endfor %}
{% endfor %}

<script src="https://unpkg.com/pagedjs/dist/paged.polyfill.js"></script>

<!-->
Seems relevant and useful: https://www.edrlab.org/public/slides/dps2019/DPS-s6-1-Blanc.pdf
<!-->


</body>