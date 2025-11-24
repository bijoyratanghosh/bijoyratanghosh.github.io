<h2 id="work-in-progress">Work in Progress</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.working_papers %}

<li style="margin-bottom: 30px;">
  <div class="pub-row" style="display: flex; flex-wrap: wrap; gap: 20px;">
    
    {% if link.image %} 
    <div class="pub-image" style="flex: 0 0 150px;">
      <img src="{{ link.image }}" class="teaser" style="width: 100%; border-radius: 5px; box-shadow: 0 2px 5px rgba(0,0,0,0.1);">
    </div>
    {% endif %}

    <div class="pub-content" style="flex: 1;">
      <div class="title" style="font-weight: bold; font-size: 1.1rem;">
        <a href="{{ link.pdf | default: '#' }}" style="text-decoration: none; color: #0056b3;">{{ link.title }}</a>
      </div>
      
      <div class="author" style="margin-top: 5px; font-style: italic;">{{ link.authors }}</div>
      
      {% if link.date %} 
      <div class="date" style="margin-top: 2px; font-size: 0.9rem; color: #666;">{{ link.date }}</div>
      {% endif %}

      {% if link.abstract %}
      <div class="abstract" style="margin-top: 10px; font-size: 0.95rem; color: #444; line-height: 1.5;">
        <strong>Abstract:</strong> {{ link.abstract }}
      </div>
      {% endif %}

      <div class="links" style="margin-top: 10px;">
        {% if link.pdf %} 
        <a href="{{ link.pdf }}" class="btn" role="button" target="_blank" style="font-size: 0.9rem; padding: 5px 10px; border: 1px solid #ccc; border-radius: 4px; text-decoration: none; color: #333; margin-right: 5px;">PDF</a>
        {% endif %}
        {% if link.code %} 
        <a href="{{ link.code }}" class="btn" role="button" target="_blank" style="font-size: 0.9rem; padding: 5px 10px; border: 1px solid #ccc; border-radius: 4px; text-decoration: none; color: #333;">Code</a>
        {% endif %}
      </div>
    </div>
  </div>
</li>

{% endfor %}

</ol>
</div>

