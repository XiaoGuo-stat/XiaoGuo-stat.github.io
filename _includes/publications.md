<style>
    .publications ol.bibliography li {
        margin-bottom: 2px; /* 调整为需要的间距 */
        padding-bottom: 0; /* 去除多余的内部间距 */
    }
</style>

<h2 id="publications" style="margin: 2px 0px -15px;">Selected Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <!-- 删除图片相关的 col-sm-3 部分 -->
  <div class="col-sm-12" style="position: relative; padding-right: 15px; padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em></div>
      <div class="links">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Link</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
        {% endif %}
        {% if link.page %} 
        <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
        {% endif %}
        {% if link.bibtex %} 
        <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
        {% endif %}
        {% if link.notes %} 
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
        {% endif %}
        {% if link.others %} 
        {{ link.others }}
        {% endif %}
      </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>
