---
---
<head>
    <link href="/css/print.css" rel="stylesheet" type="text/css" />
    <script src="https://unpkg.com/pagedjs/dist/paged.polyfill.js"></script>
</head>

<body>

{% for section in site.data.structure %}
    {% for chapter in section %}

        {% assign post = site.chapters | where:"url", chapter.url  | first %}

        {{post.content}}

    {% endfor %}
{% endfor %}

<script>
class MyHandler extends Paged.Handler {
    beforeParsed(content) {
        // manipulate the DOM here
    }
}
Paged.registerHandlers(MyHandler);

window.onload = function() {
    var paged = new Paged.Preview();
}


</script>


</body>