---
layout: splash
header:
  overlay_color: "#000"
  overlay_filter: 0.35
  #overlay_image: /assets/cover.png
---

<style>
/***** Simple, responsive tile grid *****/
.tile-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:18px;margin:1.25rem 0 2rem}
.tile{display:flex;flex-direction:column;border:1px solid rgba(0,0,0,.06);border-radius:14px;padding:12px;text-decoration:none;background:#fff;transition:transform .15s ease, box-shadow .15s ease}
.tile:hover{transform:translateY(-2px);box-shadow:0 10px 24px rgba(0,0,0,.08)}
.tile img{width:100%;height:140px;object-fit:cover;border-radius:10px}
.tile-body{margin-top:.6rem}
.tile-title{margin:.25rem 0 .1rem;font-size:1.05rem}
.tile-desc{margin:0;color:rgba(0,0,0,.72);font-size:.92rem;line-height:1.35}
.tile-badge{display:inline-block;margin-top:.5rem;font-size:.75rem;padding:.15rem .5rem;border-radius:999px;background:#f2f2f2}
@media (min-width:1200px){.tile img{height:160px}}
</style>

<div class="tile-grid">
{% assign tools = site.data.tools.all %}
{% for t in tools %}
  <a class="tile" href="{{ t.url }}" target="_blank">
    {% if t.image %}<img src="{{ t.image | relative_url }}" alt="{{ t.title }}">{% endif %}
    <div class="tile-body">
      <h3 class="tile-title">{{ t.title }}</h3>
      <p class="tile-desc">{{ t.excerpt }}</p>
      {% if t.badge %}<span class="tile-badge">{{ t.badge }}</span>{% endif %}
    </div>
  </a>
{% endfor %}
</div>

<a id="about"></a>
## About
Hela Nomad Labs is the experimental wing of **Hela Nomad** — building digital tools at the intersection of culture, linguistics, and code.

<a id="updates"></a>
## Updates
- **Nov 2025** — *Indic Script Explorer:* Initial public release.
- **Soon** — *Pāli Transliterator* and *Font Visualizer*.

<a id="contact"></a>
## Contact
Find us on [GitHub](https://github.com/helanomad) or [YouTube](https://www.youtube.com/@HelaNomad).