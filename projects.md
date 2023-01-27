---
layout: page
title: Projects
subtitle:
---

<table>
{% for proj in site.data.projs %}
  {% if proj.video_embed %}
    <tr>
      <td><a href="{{ proj.arxiv_url }}">{{ proj.title }}</a><br>
        <div class="projauthor">
          {{ proj.authors }}<br>
        </div>
        <div class="projjournal">
          {{ proj.venue }}
        </div>
        <div id="bib{{proj.short_id}}" style="display:none">
            <blockquote>
                <pre>
                    {{proj.bib}}
                </pre>
            </blockquote>
        </div>
        <div id="abs{{proj.short_id}}" style="display:none">
            <blockquote>
                {{proj.abs}}
            </blockquote>
        </div>
        <div style="font-size:small">
          {% if proj.site != null %}
              <a href="{{proj.site}}">[Github Page]</a>
          {% endif %}
          {% if proj.bib != null %}
              <a href="javascript:copy(div{{proj.short_id}}, bib{{proj.short_id}})">[Bibtex]</a>
          {% endif %}
          {% if proj.abs != null %}
              <a href="javascript:copy(div{{proj.short_id}}, abs{{proj.short_id}})">[Abstract]</a>
          {% endif %}
        </div>
        <div id="div{{ proj.short_id }}" class="projInfo"></div>
        <div class='video_embed'>
          {{ proj.video_embed }}
        </div>
      </td>
    </tr>
  {% endif %}
{% endfor %}
</table>
