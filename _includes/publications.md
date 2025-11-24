<h2 id="work-in-progress" style="margin: 2px 0px -15px;">Work in Progress</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.working_papers %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.date %} 
    <abbr class="badge">{{ link.date }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf | default: '#' }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      {% if link.abstract %}
      <div class="abstract" style="margin-top: 5px; font-size: 0.9rem; color: #555;">
        <strong>Abstract:</strong> {{ link.abstract }}
      </div>
      {% endif %}
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>

