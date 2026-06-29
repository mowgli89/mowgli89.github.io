---
layout: page
title: people
permalink: /people/
description: The Bose FABLE Lab team.
nav: true
nav_order: 3
---

## Principal Investigator

<div class="row align-items-center">
  <div class="col-sm-3 text-center">
    <img src="{{ '/assets/img/headshot_placeholder.png' | relative_url }}" alt="Sourav K. Bose" class="img-fluid rounded z-depth-1" style="max-width: 200px;">
    <p style="font-size: 0.8rem; opacity: 0.6; margin-top: 0.4rem;">Headshot placeholder</p>
  </div>
  <div class="col-sm-9">
    <h4 style="margin-bottom: 0.2rem;">Sourav K. Bose, MD, MBA, MSc</h4>
    <p style="opacity: 0.8; margin-top: 0;">Director, Bose FABLE Lab · Assistant Professor of Surgery, Baylor College of Medicine · Pediatric &amp; Fetal Surgeon, Texas Children's Hospital</p>
  </div>
</div>

<div markdown="1">

Dr. Bose is a pediatric and fetal surgeon and surgeon-scientist whose work bridges the operating room and the bench. His research program centers on the mechanobiology of fetal lung development and congenital diaphragmatic hernia (CDH), with a focus on how the developing lung senses mechanical force through the PIEZO1 pathway and how fetal interventions such as tracheal occlusion (FETO) can be understood and improved.

He completed general surgery training at Brigham and Women's Hospital (Harvard), a fetal research fellowship at the Children's Hospital of Philadelphia Center for Fetal Research, and pediatric surgery fellowship at Texas Children's Hospital. He earned his MD from the Perelman School of Medicine, an MBA from the Wharton School, and an MSc from the London School of Hygiene and Tropical Medicine.

<p style="font-size: 0.85rem; opacity: 0.7;">TODO: review and personalize this bio; replace the headshot placeholder with a photo at assets/img/headshot_placeholder.png. Verify degrees and training details before publishing.</p>

</div>

---

## Lab Members

<div class="row">
{% for m in site.data.members %}
  <div class="col-sm-4 mb-4 text-center">
    <img src="{{ '/assets/img/members/' | append: m.photo | relative_url }}" alt="{{ m.name }}" class="img-fluid rounded z-depth-1" style="max-width: 160px;">
    <h6 style="margin-bottom: 0.1rem; margin-top: 0.6rem;">
      {% if m.link and m.link != "" %}<a href="{{ m.link }}">{{ m.name }}</a>{% else %}{{ m.name }}{% endif %}
    </h6>
    <p style="font-size: 0.85rem; opacity: 0.75; margin: 0;">{{ m.role }}</p>
    {% if m.blurb and m.blurb != "" %}<p style="font-size: 0.8rem; opacity: 0.65; margin-top: 0.3rem;">{{ m.blurb }}</p>{% endif %}
  </div>
{% endfor %}
</div>

<p style="font-size: 0.9rem;">Interested in joining? See the <a href="{{ '/research/' | relative_url }}">research page</a> and <a href="{{ '/contact/' | relative_url }}">get in touch</a>.</p>
