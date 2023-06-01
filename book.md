---
---
<head>
    <link href="/css/interface.css" rel="stylesheet" type="text/css" />
    <link href="/css/print.css" rel="stylesheet" type="text/css" />
    <script src="https://unpkg.com/pagedjs@0.4.1/dist/paged.polyfill.js"></script>

</head>

<body>

{% for section in site.data.structure %}
    {% for chapter in section %}
        
        {% assign post = site.chapters | where:"url", chapter.url  | first %}

        {{post.content}}

    {% endfor %}
{% endfor %}


<!-->
Seems relevant and useful: https://www.edrlab.org/public/slides/dps2019/DPS-s6-1-Blanc.pdf
<!-->


</body>