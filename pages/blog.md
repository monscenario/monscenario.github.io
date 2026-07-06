---
layout: default
title: Blog
description: "Articles, retours d'ateliers et éclairages sur les scénarios socio-énergétiques par l'association Scénario."
permalink: /blog
---

<div style="max-width:760px; margin:150px auto 80px; padding:0 32px; font-family:'Inter',sans-serif; color:#111;">

  <h1 style="font-size:2.4rem; font-weight:700; letter-spacing:-0.02em; margin-bottom:0.3em;">Publications</h1>
  <p style="font-size:1.05rem; color:#555; margin-top:0; margin-bottom:3rem; border-bottom:1px solid #eee; padding-bottom:2rem;">
    Retours d'ateliers, éclairages scientifiques, actualités de l'association.
  </p>

  <!-- Articles existants -->
  {% for post in site.posts %}
  <article style="border-bottom:1px solid #eee; padding:1.8rem 0;">
    <span style="font-size:0.82rem; color:#999; letter-spacing:0.05em;">{{ post.date | date: "%d.%m.%Y" }}</span>
    <h2 style="font-size:1.2rem; font-weight:600; margin:0.4em 0 0.6em;">
      <a href="{{ site.baseurl }}{{ post.url }}" style="color:#111; text-decoration:none;">{{ post.title }}</a>
    </h2>
    {% if post.excerpt %}
    <p style="color:#555; font-size:0.97rem; line-height:1.7; margin:0;">{{ post.excerpt | strip_html | truncatewords:30 }}</p>
    {% endif %}
    <a href="{{ site.baseurl }}{{ post.url }}" style="display:inline-block; margin-top:0.8em; font-size:0.9rem; color:#111; text-decoration:underline;">Lire →</a>
  </article>
  {% endfor %}

  <!-- Ressources externes -->
  <h2 style="font-size:1.3rem; font-weight:700; margin:2.5rem 0 1.2em;">Ressources</h2>

  <a href="https://www.ademe.fr/les-futurs-en-transition/" target="_blank" rel="noopener" style="display:flex; gap:1.4rem; align-items:stretch; border:1px solid #eee; border-radius:10px; overflow:hidden; margin-bottom:1.6rem; text-decoration:none; color:inherit;">
    <img src="{{ site.baseurl }}/assets/img/ademe-preview.png" alt="Les Futurs en Transition — ADEME" style="width:180px; min-width:180px; height:130px; object-fit:cover; border-right:1px solid #eee;">
    <div style="padding:1rem 1.2rem 1rem 0; display:flex; flex-direction:column; justify-content:center;">
      <span style="font-size:0.75rem; color:#999; letter-spacing:0.08em; text-transform:uppercase;">ADEME</span>
      <h3 style="font-size:1.05rem; font-weight:600; margin:0.3em 0 0.4em; color:#111;">Les Futurs en Transition</h3>
      <p style="color:#555; font-size:0.92rem; line-height:1.6; margin:0;">Quatre scénarios prospectifs de l'ADEME pour atteindre la neutralité carbone de la France à l'horizon 2050.</p>
    </div>
  </a>

  <a href="https://rte-futursenergetiques2050.com" target="_blank" rel="noopener" style="display:flex; gap:1.4rem; align-items:stretch; border:1px solid #eee; border-radius:10px; overflow:hidden; margin-bottom:1.6rem; text-decoration:none; color:inherit;">
    <img src="{{ site.baseurl }}/assets/img/rte-preview.png" alt="Futurs énergétiques 2050 — RTE" style="width:180px; min-width:180px; height:130px; object-fit:cover; border-right:1px solid #eee;">
    <div style="padding:1rem 1.2rem 1rem 0; display:flex; flex-direction:column; justify-content:center;">
      <span style="font-size:0.75rem; color:#999; letter-spacing:0.08em; text-transform:uppercase;">RTE</span>
      <h3 style="font-size:1.05rem; font-weight:600; margin:0.3em 0 0.4em; color:#111;">Futurs énergétiques 2050</h3>
      <p style="color:#555; font-size:0.92rem; line-height:1.6; margin:0;">Six scénarios de RTE pour la neutralité carbone du système électrique français, avec ou sans relance du nucléaire.</p>
    </div>
  </a>

</div>
