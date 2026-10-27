---
title: Sumário
---

# Sumário

Uma jornada em quatro partes. Os capítulos com link já têm rascunho; os outros ainda estão na estrada.

{% for parte in site.data.sumario %}
<section class="parte-sumario">
  <h2>Parte {{ parte.parte }}</h2>
  <ol>
  {% for c in parte.capitulos %}
    <li value="{{ c.numero }}">{% if c.arquivo %}<a href="{{ c.arquivo | replace: '.md', '.html' }}">{{ c.titulo }}</a>{% else %}<span class="por-vir">{{ c.titulo }}</span>{% endif %}</li>
  {% endfor %}
  </ol>
</section>
{% endfor %}
