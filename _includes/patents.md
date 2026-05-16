<h2 id="patents" style="margin: 2px 0px -15px;">Patents</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.pubscombined.main %}
{% if link.type contains "patent" %}

  <div class="col-sm-9" style="position: relative; padding-right: 15px; padding-left: 20px;">
    
    <div class="title">
      <b>{{ link.title }}</b> | {{ link.publication }} | {{ link.date }}
    </div>

    {% if link.authors %}
    <div class="author" style="position: relative; padding-left: 10px;">
      {{ link.authors }}
    </div>
    {% endif %}

    <div class="links">
      {% if link.doi %}
        <a href="{{ link.doi }}" target="_blank">Link</a>
      {% endif %}
      
      {% if link.notes %}
        <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
    </div>

  </div>

  <br>

{% endif %}
{% endfor %}

</ol>
</div>
