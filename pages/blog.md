---
layout: default
title: Blog
description: "Articles, retours d'ateliers et éclairages sur les scénarios socio-énergétiques par l'association Scénario."
permalink: /blog
---

<div style="max-width:760px; margin:80px auto; padding:0 32px; font-family:'Inter',sans-serif; color:#111;">

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

  <!-- Emplacements vides -->
  <article style="border-bottom:1px solid #eee; padding:1.8rem 0; opacity:0.35;">
    <span style="font-size:0.82rem; color:#999; letter-spacing:0.05em;">À venir</span>
    <h2 style="font-size:1.2rem; font-weight:600; margin:0.4em 0 0.6em; color:#aaa;">Titre de l'article</h2>
    <p style="color:#bbb; font-size:0.97rem; line-height:1.7; margin:0;">Résumé de l'article à rédiger.</p>
  </article>

  <article style="border-bottom:1px solid #eee; padding:1.8rem 0; opacity:0.25;">
    <span style="font-size:0.82rem; color:#999; letter-spacing:0.05em;">À venir</span>
    <h2 style="font-size:1.2rem; font-weight:600; margin:0.4em 0 0.6em; color:#aaa;">Titre de l'article</h2>
    <p style="color:#bbb; font-size:0.97rem; line-height:1.7; margin:0;">Résumé de l'article à rédiger.</p>
  </article>

  <article style="padding:1.8rem 0; opacity:0.15;">
    <span style="font-size:0.82rem; color:#999; letter-spacing:0.05em;">À venir</span>
    <h2 style="font-size:1.2rem; font-weight:600; margin:0.4em 0 0.6em; color:#aaa;">Titre de l'article</h2>
    <p style="color:#bbb; font-size:0.97rem; line-height:1.7; margin:0;">Résumé de l'article à rédiger.</p>
  </article>

</div>
