---
---
<head>
    <link href="/css/print.css" rel="stylesheet" type="text/css" />
<script src="https://unpkg.com/pagedjs/dist/paged.js"></script>    
</head>

<body>

{% for section in site.data.structure %}
    {% for chapter in section %}
        
        {% assign post = site.chapters | where:"url", chapter.url  | first %}

        {{post.content}}

    {% endfor %}
{% endfor %}



<script>
let paged = new Previewer();
let flow = paged.preview(DOMContent, ["/css/print.css"], document.body).then((flow) => {
	console.log("Rendered", flow.total, "pages.");
})
</script>

<!-->
Seems relevant and useful: https://www.edrlab.org/public/slides/dps2019/DPS-s6-1-Blanc.pdf
<!-->


</body>