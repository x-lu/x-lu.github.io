<h2 id="publications" style="margin: 2px 0 -15px;">Publications</h2>

<div class="publications">
  <ol class="bibliography">
    {% for publication in site.data.publications.main %}
      <li>
        <div class="title">
          {% if publication.conference_short %}
            <abbr class="badge publication-badge">{{ publication.conference_short }}</abbr>
          {% endif %}
          <a href="{{ publication.pdf }}" target="_blank" rel="noopener">{{ publication.title }}</a>
        </div>
        <div class="author">{{ publication.authors }}</div>
        <div class="periodical"><em>{{ publication.conference }}</em></div>
        <div class="links">
          {% if publication.pdf %}
            <a href="{{ publication.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">PDF</a>
          {% endif %}
          {% if publication.slides %}
            <a href="{{ publication.slides }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Slides</a>
          {% endif %}
          {% if publication.code %}
            <a href="{{ publication.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Code</a>
          {% endif %}
          {% if publication.notes %}
            <strong class="publication-note"><i>{{ publication.notes }}</i></strong>
          {% endif %}
        </div>
      </li>
    {% endfor %}
  </ol>
</div>
