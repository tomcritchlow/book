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



</body>