<ol class="bibliography">
{% for publication in site.data.publications.main %}
  <li>
    <div class="pub-row{% unless publication.image %} no-image{% endunless %}">
      {% if publication.image %}<img class="pub-image" src="{{ publication.image }}" alt="{{ publication.title | escape }} 연구 그림" loading="lazy" width="116" height="84">{% endif %}
      <div>
        <h3 class="pub-title">{% if publication.pdf %}<a href="{{ publication.pdf }}" target="_blank" rel="noopener noreferrer">{{ publication.title }}</a>{% else %}{{ publication.title }}{% endif %}</h3>
        <p class="pub-author">{{ publication.authors }}</p>
        <p class="pub-venue">{{ publication.conference }}</p>
        {% if publication.notes %}<p class="pub-notes">{{ publication.notes }}</p>{% endif %}
        <div class="pub-links">
          {% if publication.pdf %}<a href="{{ publication.pdf }}" target="_blank" rel="noopener noreferrer">논문 보기</a>{% endif %}
          {% if publication.PPT %}<a href="{{ publication.PPT }}" target="_blank" rel="noopener noreferrer">발표자료</a>{% endif %}
          {% if publication.poster %}<a href="{{ publication.poster }}" target="_blank" rel="noopener noreferrer">포스터</a>{% endif %}
          {% if publication.code %}<a href="{{ publication.code }}" target="_blank" rel="noopener noreferrer">코드</a>{% endif %}
          {% if publication.page %}<a href="{{ publication.page }}" target="_blank" rel="noopener noreferrer">프로젝트 소개</a>{% endif %}
        </div>
      </div>
    </div>
  </li>
{% endfor %}
</ol>
