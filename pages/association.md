---
layout: default
title: Présentation de l'asso
permalink: /association
---

<div id="hero-image-wrap" style="position:relative; width:100%; line-height:0;">
  <img id="hero-image" src="{{ site.baseurl }}/assets/img/top-image.jpg" alt="Scénario" style="width:100%; display:block; margin-top:0;">
  <div style="width:100%; background:#fff; padding:24px 10% 60px; box-sizing:border-box; font-family:'Inter',sans-serif; line-height:1.9;">
    <p style="font-size:1.15rem; margin-bottom:1.5rem; color:#111; max-width:860px;">
      Nucléaire ou renouvelables ? Sobriété ou souveraineté ? Coût ou climat ? Répondre à ces questions demande de raisonner en système : voir les arbitrages, les contraintes, les conséquences. C'est ce que permettent les scénarios de société.
    </p>
    <p style="font-size:1.15rem; margin:0; color:#111; max-width:860px;">
      Scénario propose des ateliers pour apprendre à construire et décrypter ces scénarios, afin que chacun puisse se forger sa propre opinion sur les choix énergétiques de demain.
    </p>
  </div>
</div>

<style>
  /* Cache le logo du header sur cette page */
  .site-logo { opacity: 0; transition: opacity 0.3s ease; }
  .site-logo.visible { opacity: 1; }
  /* Colle l'image directement sous le bandeau */
  .content-wrapper { padding-top: 0 !important; margin-top: 0 !important; }
</style>

<!-- Logo flottant — z-index SOUS le header pour disparaître derrière -->
<img id="floating-logo" src="{{ site.baseurl }}/assets/img/logo-scenario.png" alt="Scénario"
  style="position:fixed; pointer-events:none; z-index:50; transform-origin:top left; will-change:top,left,width;">

<script>
(function() {
  var floatingLogo = document.getElementById('floating-logo');
  var heroWrap     = document.getElementById('hero-image-wrap');
  var headerLogo   = document.querySelector('.site-logo');
  var header       = document.getElementById('site-header');

  function lerp(a, b, t) { return a + (b - a) * t; }
  function ease(t) { return t < 0.5 ? 2*t*t : -1+(4-2*t)*t; }

  var startW, startX, startY, endW, endX, endY, scrollDist, headerH;

  function init() {
    headerH  = header.offsetHeight;
    var heroRect = heroWrap.getBoundingClientRect();

    startW = 260;
    startX = heroRect.left + heroRect.width / 2 - startW / 2;
    startY = headerH + 20; // juste sous le bandeau

    // Destination : logo glisse vers le haut jusqu'à disparaître derrière le header
    // endY = -startW signifie que le logo est entièrement au-dessus du viewport
    endW = 86; // taille finale dans le header
    endX = 20; // aligné à gauche comme le logo header
    endY = headerH - startW; // le logo sort par le haut (derrière le bandeau)

    // scrollDist : nombre de pixels à scroller pour compléter l'animation
    scrollDist = startY - endY;

    floatingLogo.style.width = startW + 'px';
    floatingLogo.style.left  = startX + 'px';
    floatingLogo.style.top   = startY + 'px';
    floatingLogo.style.opacity = '1';
    update();
  }

  function update() {
    if (!scrollDist) return;
    var raw = Math.min(1, Math.max(0, window.scrollY) / scrollDist);
    var t   = ease(raw);

    var heroRect = heroWrap.getBoundingClientRect();
    var curStartX = heroRect.left + heroRect.width / 2 - startW / 2;

    var newTop = lerp(startY, endY, t);

    // Ne jamais descendre sous startY
    newTop = Math.min(newTop, startY);

    floatingLogo.style.width   = lerp(startW, endW, t) + 'px';
    floatingLogo.style.left    = lerp(curStartX, endX, t) + 'px';
    floatingLogo.style.top     = newTop + 'px';

    // Le logo est pleinement caché derrière le header quand newTop + currentW <= headerH
    var currentW = lerp(startW, endW, t);
    var fullyHidden = (newTop + currentW) <= headerH;

    if (fullyHidden) {
      headerLogo.classList.add('visible');
      floatingLogo.style.opacity = '0';
    } else {
      headerLogo.classList.remove('visible');
      floatingLogo.style.opacity = '1';
    }
  }

  window.addEventListener('scroll', update, { passive: true });
  window.addEventListener('resize', init,   { passive: true });

  var heroImg = document.getElementById('hero-image');
  if (heroImg.complete) { init(); } else { heroImg.addEventListener('load', init); }
})();
</script>


<div style="max-width:860px; margin:0 auto 80px; padding:0 32px; font-family:'Inter',sans-serif; color:#111;">

  <h2 style="font-size:1.6rem; font-weight:700; margin:0 0 2.5rem;">En quoi consiste l'atelier ?</h2>

  <!-- Partie 1 -->
  <div style="display:flex; gap:3rem; align-items:center; margin-bottom:4rem; flex-wrap:wrap;">
    <div style="flex:1; min-width:220px;">
      <img src="{{ site.baseurl }}/assets/images/environnement_mode_de_vie_1782397542481.png" alt="Mode de vie" style="width:100%; border-radius:6px; display:block;">
    </div>
    <div style="flex:2; min-width:260px;">
      <p style="font-size:0.8rem; font-weight:600; letter-spacing:0.1em; color:#999; text-transform:uppercase; margin-bottom:0.4em; margin-top:0;">Temps 1</p>
      <h2 style="font-size:1.4rem; font-weight:700; margin:0 0 0.8em;">Choisir son mode de vie</h2>
      <p style="font-size:1rem; line-height:1.75; color:#333;">
        Le joueur choisit un environnement (ville, campagne, mer…) puis construit son mode de vie : habitat, mobilité, alimentation. Ces choix définissent sa demande en énergie, le point de départ de tout.
      </p>
    </div>
  </div>

  <!-- Partie 2 -->
  <div style="display:flex; gap:3rem; align-items:center; margin-bottom:4rem; flex-wrap:wrap;">
    <div style="flex:2; min-width:260px; order:1;">
      <p style="font-size:0.8rem; font-weight:600; letter-spacing:0.1em; color:#999; text-transform:uppercase; margin-bottom:0.4em; margin-top:0;">Temps 2</p>
      <h2 style="font-size:1.4rem; font-weight:700; margin:0 0 0.8em;">Construire son mix énergétique</h2>
      <p style="font-size:1rem; line-height:1.75; color:#333;">
        Le joueur compose son mix de production (solaire, éolien, nucléaire, gaz…) pour couvrir la demande. Quatre indicateurs en temps réel : coût, CO₂, empreinte matières, souveraineté. Un mix instable oblige à des arbitrages douloureux.
      </p>
    </div>
    <div style="flex:1; min-width:220px; order:2;">
      <img src="{{ site.baseurl }}/assets/images/mix_energetique_1782397551726.png" alt="Mix énergétique" style="width:100%; border-radius:6px; display:block;">
    </div>
  </div>

  <!-- Partie 3 -->
  <div style="display:flex; gap:3rem; align-items:center; margin-bottom:4rem; flex-wrap:wrap;">
    <div style="flex:1; min-width:220px;">
      <img src="{{ site.baseurl }}/assets/images/international_ressources.jpeg" alt="Ressources mondiales" style="width:100%; border-radius:6px; display:block;">
    </div>
    <div style="flex:2; min-width:260px;">
      <p style="font-size:0.8rem; font-weight:600; letter-spacing:0.1em; color:#999; text-transform:uppercase; margin-bottom:0.4em; margin-top:0;">Temps 3</p>
      <h2 style="font-size:1.4rem; font-weight:700; margin:0 0 0.8em;">Confronter ses choix au monde réel</h2>
      <p style="font-size:1rem; line-height:1.75; color:#333;">
        Y a-t-il assez de lithium, de cuivre, de cobalt pour généraliser le modèle choisi à la planète entière ? Ce dernier temps ancre les décisions individuelles dans les tensions géopolitiques mondiales et ouvre le débat.
      </p>
    </div>
  </div>

  <hr style="border:none; border-top:1px solid #eee; margin-bottom:2.5rem;">
  <p style="font-size:0.95rem; color:#777; text-align:center;">
     L'atelier est actuellement en cours de test et de fabrication. Si le sujet vous intéresse, écrivez-nous :&nbsp;&nbsp;
    <a href="mailto:monscenarioenergetique@gmail.com" style="color:#111; font-weight:600; text-decoration:underline;">monscenarioenergetique@gmail.com</a>
  </p>

</div>

