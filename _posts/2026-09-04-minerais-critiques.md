---
layout: default
title: "Minerais critiques : quelles sont les bonnes questions à se poser ?"
permalink: /minerais-critiques
body_class: post-page
bande_left: mine1.png
bande_right: mine2.png
---

<style>
  .post-hero {
    position: relative;
    border-bottom: 1px solid #e8e4dc;
    padding: 180px 32px 60px;
    text-align: center;
    overflow: hidden;
  }
  .post-hero-bg {
    position: absolute;
    inset: 0;
    background-image: url('{{ site.baseurl }}/assets/img/fond-article.png');
    background-size: cover;
    background-position: center;
    z-index: 0;
  }
  .post-hero > *:not(.post-hero-bg) {
    position: relative;
    z-index: 1;
  }
  .post-hero .post-tag {
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: #888;
    margin-bottom: 1.4rem;
  }
  .post-hero h1 {
    font-size: clamp(1.8rem, 4vw, 3rem);
    font-weight: 700;
    letter-spacing: -0.03em;
    line-height: 1.15;
    color: #111;
    max-width: 760px;
    margin: 0 auto 1.4rem;
  }
  .post-hero .post-subtitle {
    font-size: 1.05rem;
    color: #444;
    font-style: italic;
    max-width: 600px;
    margin: 0 auto 2rem;
    line-height: 1.7;
  }
  .post-meta {
    font-size: 0.75rem;
    color: #999;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .post-body {
    max-width: 720px;
    margin: 0 auto;
    padding: 64px 32px 100px;
    font-family: 'Inter', sans-serif;
    color: #222;
    line-height: 1.85;
    font-size: 1.02rem;
  }

  .post-body p {
    font-size: 1.02rem;
    color: #333;
    line-height: 1.85;
    margin-bottom: 1.4em;
  }

  .post-body h2 {
    font-size: 1.45rem;
    font-weight: 700;
    letter-spacing: -0.02em;
    color: #111;
    margin: 3.5rem 0 1rem;
    padding-top: 1rem;
    border-top: 2px solid #111;
  }

  .post-body h3 {
    font-size: 1.1rem;
    font-weight: 700;
    color: #111;
    margin: 2.5rem 0 0.8rem;
  }

  /* Bulle callout */
  .callout {
    border-left: 4px solid #111;
    background: #f7f5f0;
    margin: 2.5rem 0;
    padding: 1.4rem 2rem;
    border-radius: 0 8px 8px 0;
    position: relative;
  }
  .callout p {
    font-size: 1.05rem;
    font-style: italic;
    font-weight: 600;
    color: #111;
    margin: 0;
    line-height: 1.5;
  }
  .callout::before {
    content: '"';
    position: absolute;
    top: -10px;
    left: 16px;
    font-size: 4rem;
    color: #ddd;
    font-family: Georgia, serif;
    line-height: 1;
  }

  /* Placeholder image */
  .img-placeholder {
    width: 100%;
    background: #f0ede8;
    border: 2px dashed #ccc;
    border-radius: 8px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 2.5rem 0;
    padding: 40px 20px;
    color: #aaa;
    font-size: 0.82rem;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    text-align: center;
    gap: 10px;
  }
  .img-placeholder svg {
    opacity: 0.35;
  }
  .img-placeholder.tall { min-height: 300px; }
  .img-placeholder.medium { min-height: 220px; }

  /* Encadré stats */
  .stat-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 1px;
    background: #e5e5e5;
    border: 1px solid #e5e5e5;
    border-radius: 8px;
    overflow: hidden;
    margin: 2.5rem 0;
  }
  .stat-cell {
    background: #fff;
    padding: 1.4rem 1.2rem;
    text-align: center;
  }
  .stat-cell .stat-val {
    font-size: 2rem;
    font-weight: 700;
    color: #111;
    letter-spacing: -0.03em;
    display: block;
    margin-bottom: 0.3rem;
  }
  .stat-cell .stat-label {
    font-size: 0.75rem;
    color: #888;
    line-height: 1.4;
    text-transform: uppercase;
    letter-spacing: 0.06em;
  }

  /* Sources */
  .post-sources {
    margin-top: 4rem;
    padding-top: 2rem;
    border-top: 1px solid #eee;
  }
  .post-sources h2 {
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: #999;
    border: none;
    margin: 0 0 1rem;
    padding: 0;
    font-weight: 600;
  }
  .post-sources ul {
    padding-left: 0;
    list-style: none;
  }
  .post-sources li {
    font-size: 0.82rem;
    color: #888;
    line-height: 1.6;
    margin-bottom: 0.7em;
    padding-left: 1em;
    border-left: 2px solid #eee;
  }
  .post-sources a {
    color: #555;
    text-decoration: underline;
    text-underline-offset: 2px;
  }
  .post-sources a:hover { color: #111; }

  /* Retour blog */
  .post-back {
    text-align: center;
    padding: 2rem 0 0;
    border-top: 1px solid #eee;
    margin-top: 3rem;
  }
  .post-back a {
    font-size: 0.82rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: #999;
    text-decoration: none;
  }
  .post-back a:hover { color: #111; }

  @media (max-width: 768px) {
    .post-hero { padding: 60px 20px 40px; }
    .post-body { padding: 40px 20px 60px; }
    .stat-grid { grid-template-columns: 1fr 1fr; }
  }
</style>

<!-- En-tête de l'article -->
<div class="post-hero">
  <div class="post-hero-bg"></div>
  <h1>Minerais critiques : quelles sont les bonnes questions à se poser ?</h1>
  <p class="post-subtitle">Le cuivre de votre chargeur, le cobalt de votre batterie, le néodyme de l'éolienne au large des côtes. Ces métaux, personne ne les regardait. Depuis peu, on les compte comme des munitions.</p>
  <div class="post-meta">Par Scénario &nbsp;·&nbsp; 4 septembre 2026</div>
</div>

<div class="post-body">

  <p>En avril 2025, en représailles aux droits de douane américains, Pékin raye sept lignes d’une liste douanière : sept terres rares sont désormais soumises à restriction. Quelques mois plus tard, des chaînes de montage automobile tournent au ralenti à l’autre bout du monde.</p>
  
  <p>Les minerais critiques sont essentiels à l’électrification: voitures électriques, modernisation du réseau, énergies renouvelables etc. mais aussi, plus largement, à l’essor du numérique et à la défense. Ce sont, aujourd’hui, des sujets de sécurité nationale. Où en sont nos approvisionnements en ces minerais si précieux ?</p>

  <!-- Sommaire -->
  <nav style="background:#f7f5f0; border-radius:8px; padding:1.4rem 1.8rem; margin:2.5rem 0 3rem; font-size:0.88rem; line-height:2;">
    <p style="font-size:0.72rem; font-weight:700; letter-spacing:0.12em; text-transform:uppercase; color:#999; margin:0 0 0.8rem;">Sommaire</p>
    <ol style="margin:0; padding-left:1.2em; color:#444;">
      <li><a href="#materiaux" style="color:#333; text-decoration:none;">Qu’est-ce qu’un matériau critique ?</a></li>
      <li><a href="#essentiels" style="color:#333; text-decoration:none;">En quoi sont-ils si essentiels ?</a></li>
      <li><a href="#demande" style="color:#333; text-decoration:none;">La demande grimpe : la production suit-elle ?</a></li>
      <li><a href="#etats" style="color:#333; text-decoration:none;">Comment les États répondent-ils ?</a></li>
      <li><a href="#recyclage" style="color:#333; text-decoration:none;">Et le recyclage ?</a></li>
      <li><a href="#france" style="color:#333; text-decoration:none;">Investir en France : quels enjeux ?</a></li>
      <li><a href="#conclusion" style="color:#333; text-decoration:none;">Que dire, au final ?</a></li>
    </ol>
  </nav>

  <figure style="margin: 2.5rem 0;">
    <img src="{{ site.baseurl }}/assets/img/brgm-carte-productions.png" alt="Carte de répartition des productions minières mondiales — BRGM 2024" style="width:100%; border-radius:8px; display:block;">
    <figcaption style="font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.6rem; letter-spacing:0.04em;">BRGM - Carte de répartition des productions minières mondiales, 2024</figcaption>
  </figure>

  <h2 id="materiaux">Qu'est-ce qu'un matériau critique ?</h2>

  <div class="callout">
    <p> -> Sans substitut et un approvisionnement à risque.</p>
  </div>

  <p>On appelle matériau critique un minéral non substituable dont l'approvisionnement reste fragile, soit parce que sa concentration géographique en fait une arme géopolitique, soit parce que la demande explose plus vite que l'offre ne peut suivre.</p>

  <p>Cuivre, lithium, nickel, cobalt, graphite, terres rares : ce sont les figures de proue. À côté d'eux, des « minéraux mineurs stratégiques » : gallium, germanium, indium, antimoine, tungstène, pèsent peu en volume, mais conditionnent des pans entiers de l'industrie comme les semi-conducteurs, robotique, défense. L'Union européenne, dans son <a href="https://single-market-economy.ec.europa.eu/sectors/raw-materials/areas-specific-interest/critical-raw-materials/critical-raw-materials-act_en" target="_blank" rel="noopener">Critical Raw Materials Act</a>, recense 34 matières premières critiques, dont 17 jugées stratégiques (encore plus sensibles).</p>

  <h2 id="essentiels">En quoi sont-ils si essentiels ?</h2>

  <p>La transition énergétique et la révolution numérique ont un point commun : elles sont voraces en métaux. D'ici 2040 :</p>

  <div class="stat-grid">
    <div class="stat-cell"><span class="stat-val">×3</span><span class="stat-label">Demande de lithium</span></div>
    <div class="stat-cell"><span class="stat-val">×1,9</span><span class="stat-label">Demande de graphite</span></div>
    <div class="stat-cell"><span class="stat-val">×1,7</span><span class="stat-label">Demande de nickel</span></div>
    <div class="stat-cell"><span class="stat-val">×1,3</span><span class="stat-label">Demande de cuivre</span></div>
  </div>

  <p>D'ici 2040, l'AIE prévoit que la demande de lithium sera multipliée par plus de 3, tirée à 90 % par les usages bas-carbone : batteries de véhicules électriques, stockage d'énergie, électrolyseurs. Le nickel grimpe de 1,7 fois, le graphite de 1,9, les terres rares utilisées dans les aimants de 1,5, et le cuivre, présent dans tous les câbles et moteurs électriques, de 1,3.</p>


  <h2 id="demande">La demande grimpe : la production suit-elle ?</h2>

  <p>Le problème, c'est que les projets miniers et de raffinage n'avancent pas assez vite — notamment parce que les meilleurs gisements ont souvent été exploités en premier, rendant l'approvisionnement de plus en plus complexe. Un <strong>déficit d'offre important</strong> est attendu pour le cuivre et le lithium dans les prochaines décennies.</p>

  <div style="margin: 2.5rem 0;">
    <p style="font-size:0.78rem; font-weight:700; letter-spacing:0.1em; text-transform:uppercase; color:#999; margin-bottom:0.6rem;">Demande projetée vs mines annoncées: lithium &amp; cuivre</p>
    <p style="font-size:0.88rem; color:#666; margin-bottom:1rem; line-height:1.65;">
      Les barres indiquent la production issue des mines déjà en exploitation ou annoncées, comparée à la demande selon deux scénarios : <strong>STEPS</strong> (Stated Policies Scenario = politiques actuelles) et <strong>APS</strong> (Announced Pledges Scenario = engagements climatiques tenus).
    </p>
    <a href="https://www.iea.org/reports/copper-2" target="_blank" rel="noopener" style="display:grid; grid-template-columns:1fr 1fr; gap:12px; text-decoration:none;">
      <img src="{{ site.baseurl }}/assets/img/Li-miningrequirements.png" alt="Lithium — besoins miniers vs. mines annoncées (AIE)" style="width:100%; border-radius:6px; display:block; border:1px solid #eee;">
      <img src="{{ site.baseurl }}/assets/img/Cu-miningrequirements.png" alt="Cuivre — besoins miniers vs. mines annoncées (AIE)" style="width:100%; border-radius:6px; display:block; border:1px solid #eee;">
    </a>
    <p style="font-size:0.75rem; color:#bbb; text-align:center; margin-top:0.5rem; letter-spacing:0.03em;">AIE, Copper 2025 &amp; Lithium 2023 · Clique sur la photo pour accéder au rapport et voir les autres projections →</p>
    <div class="callout" style="margin-top:1.4rem;">
      <p>Dans les deux scénarios, les mines annoncées couvrent moins que la demande projetée d'ici 2035. Le déficit d'approvisionnement est donc un enjeu majeur.</p>
    </div>
  </div>

 <p> La situation s'est tout de même un peu améliorée grâce à de nouveaux projets en République démocratique du Congo et en Zambie. À l'inverse, un déficit inattendu vient d'apparaître pour le cobalt, provoqué par le nouveau quota à l'exportation décidé par la RDC, premier producteur mondial.</p>

  <p>C'est aussi une affaire de souveraineté. Il y a d'abord l'extraction, minée par des positions quasi monopolistiques. Et il y a le <strong>raffinage</strong>, cette étape souvent oubliée qui transforme le minerai brut en matériau utilisable, qui est encore plus concentré que le secteur minier lui-même. La Chine y détient aujourd'hui :</p>

  <div class="stat-grid">
    <div class="stat-cell"><span class="stat-val">50 %</span><span class="stat-label">Raffinage mondial du cuivre</span></div>
    <div class="stat-cell"><span class="stat-val">70 %</span><span class="stat-label">Raffinage du lithium</span></div>
    <div class="stat-cell"><span class="stat-val">85 %</span><span class="stat-label">Séparation des terres rares magnétiques</span></div>
    <div class="stat-cell"><span class="stat-val">&gt; 90 %</span><span class="stat-label">Graphite qualité batterie</span></div>
  </div>

<figure style="margin: 2.5rem 0;">
    <img src="{{ site.baseurl }}/assets/img/BRGM-raffinage.png" alt="Carte de répartition du raffinage — BRGM 2024" style="width:100%; border-radius:8px; display:block;">
    <figcaption style="font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.6rem; letter-spacing:0.04em;">BRGM - Carte de répartition des productions minières mondiales, 2024</figcaption>
  </figure>

  <p>En résumé, voici la repartition des mines et du raffinage en 2025:</p>

 <!-- Carrousel production par minerai -->
  <div style="margin: 2rem 0;">
    <p style="font-size:0.78rem; font-weight:700; letter-spacing:0.1em; text-transform:uppercase; color:#999; margin-bottom:0.8rem;">Production mondiale par minerai — cliquer pour le rapport AIE</p>
    <div style="display:flex; gap:16px; overflow-x:auto; padding-bottom:10px; scroll-snap-type:x mandatory; -webkit-overflow-scrolling:touch;">
      {% assign prod_imgs = "Li-prod,Cu-prod,Co-prod,Ni-prod,Rare-prod,C-prod" | split: "," %}
      {% assign prod_labels = "Lithium,Cuivre,Cobalt,Nickel,Terres rares,Graphite" | split: "," %}
      {% assign prod_urls = "https://www.iea.org/reports/lithium-2023,https://www.iea.org/reports/copper-2,https://www.iea.org/reports/cobalt,https://www.iea.org/reports/nickel,https://www.iea.org/reports/rare-earth-elements,https://www.iea.org/reports/graphite" | split: "," %}
      {% for img in prod_imgs %}
      <a href="{{ prod_urls[forloop.index0] }}" target="_blank" rel="noopener"
         style="flex:0 0 auto; width:460px; scroll-snap-align:start; text-decoration:none; display:block;">
        <img src="{{ site.baseurl }}/assets/img/{{ img }}.png"
             alt="{{ prod_labels[forloop.index0] }} — production mondiale (AIE)"
             style="width:460px; display:block; border-radius:8px; border:1px solid #eee;">
        <span style="display:block; font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.4rem; letter-spacing:0.04em;">{{ prod_labels[forloop.index0] }} →</span>
      </a>
      {% endfor %}
    </div>
    <p style="font-size:0.72rem; color:#ccc; margin-top:0.4rem; letter-spacing:0.03em;">Faire défiler · Sources : AIE</p>
  </div>


  <h3>Quand la concentration devient une arme</h3>

  <p>Rien d'accidentel dans cette domination : la Chine l'a construite patiemment, de la mine jusqu'au recyclage, en investissant sur toute la chaîne.</p>

  <p>Cette concentration s'est transformée en risque bien réel en 2025. En avril puis en octobre, la Chine a instauré des contrôles à l'exportation sur sept terres rares, forçant certains constructeurs automobiles à réduire leur production. Les mesures les plus larges ont été suspendues jusqu'en novembre 2026. Une rupture totale du commerce du graphite mettrait en péril plus de <strong>300 milliards de dollars</strong> de production annuelle hors de Chine.</p>

  <p>Résultat sur les prix : entre janvier 2025 et avril 2026, cuivre, aluminium et étain ont grimpé d'un tiers, le lithium a plus que doublé, le cobalt a bondi de 130 %, le tungstène a été multiplié par six.</p>

  <figure style="margin: 2.5rem 0;">
    <img src="{{ site.baseurl }}/assets/img/Cu_prix.jpg" alt="Évolution du prix du cuivre (AIE)" style="width:70%; max-width:480px; display:block; border-radius:8px; border:1px solid #eee; margin:0 auto;">
    <figcaption style="font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.6rem; letter-spacing:0.04em;">Prix du cuivre — AIE, Global Critical Minerals Outlook 2026</figcaption>
  </figure>

  
  <p>Mais la bonne nouvelle, c'est que ce surcoût se répercute assez peu sur le consommateur final : un triplement du prix des terres rares n'augmenterait le prix d'une voiture que de 0,1 %, ces métaux ne représentant qu'une infime part de la valeur du véhicule. La marge de manœuvre n'est pas la même partout : un triplement du prix des matériaux de batterie ferait grimper le prix final d'un véhicule électrique ou d'un système de stockage d'environ 5 %. <span style="font-size:0.82rem; color:#aaa;">(AIE, <em>Global Critical Minerals Outlook 2026</em>, p. 11)</span></p>

  <h2 id="etats">Comment les États répondent-ils ?</h2>

  <h3>La France : diplomatie du G7 et plan national</h3>

  <p>En 2026, la France a assuré la présidence du G7. Les dirigeants ont adopté en juin un objectif précis : ramener à moins de 60 % la dépendance à un seul fournisseur non membre du G7 pour les terres rares et les aimants permanents d'ici 2030.</p>

  <p>Le gouvernement français a présenté en mai 2026 un plan national de résilience « terres rares et aimants permanents ». Ses objectifs pour 2030 : couvrir 10 % de la demande mondiale de terres rares lourdes, 25 % des besoins européens en terres rares légères, et 50 % des besoins européens en aimants permanents néodyme-fer-bore, utilisés notamment dans les moteurs électriques et les éoliennes.</p>

  <h3>Les États-Unis : puissance publique et rapport de force commercial</h3>

  <p>Washington a élargi sa liste officielle de minéraux critiques de 50 à 60 entrées et lancé en février 2026 une réserve stratégique fédérale baptisée <em>Project Vault</em>, dotée de 12 milliards de dollars et consistant à établir un stock. En juillet 2025, le département de la Défense est devenu actionnaire principal de MP Materials, avec un prix plancher garanti pour l'oxyde de néodyme-praséodyme et des contrats d'achat sur dix ans.</p>

  <h3>Une carte du monde qui pourrait se redessiner</h3>
  <p>Cette crise ouvre une fenêtre pour de nouveaux acteurs. L'Amérique latine, qui produit déjà plus de 20 % de l'étain et du zinc mondiaux et environ 40 % du cuivre, ne raffine aujourd'hui qu'un cinquième de ce qu'elle extrait. Si la région développait davantage sa transformation locale, la valeur économique générée pourrait grimper de près de 50 % d'ici 2035 et permettrait de diversifier nos sources d'approvisionnement.</p>
  


  <h2 id="recyclage">Et le recyclage ?</h2>

  <p>Aujourd'hui, seuls environ 10 % des minéraux énergétiques utilisés proviennent du recyclage ; ce taux pourrait approcher 20 % d'ici 2040.</p>

  <p>On est capable de recycler une bonne partie de nos batteries jusqu'à 95 % de la matière utile, selon <a href="https://www.redwoodmaterials.com/resources/how-battery-recycling-works/">Redwood Materials</a>. Le goulot d'étranglement est ailleurs : la collecte, la réglementation, mais aussi le volume de batteries réellement en fin de vie.</p>

  <p>Mais une fois encore, le recyclage des batteries reste très concentré en Chine (75 % du prétraitement, 90 % de la récupération des matériaux).</p>

  <h2 id="france">Investir en France : quels enjeux ?</h2>

  <p>En 2023, le BRGM a actualisé le potentiel minier du sous-sol français. Certains matériaux y sont effectivement disponibles, tandis que d'autres sont absents ou très peu concentrés. Des recherches portent sur d'autres moyens de production, mais ils restent marginaux.</p>

   <figure style="margin: 2rem 0;">
    <a href="https://www.mineralinfo.fr/fr/potentiel-du-sous-sol-francais-exploration" target="_blank" rel="noopener">
      <img src="{{ site.baseurl }}/assets/img/potentiel-minier.jpg" alt="Potentiel minier du sous-sol français — BRGM 2023" style="width:100%; border-radius:8px; display:block; border:1px solid #eee;">
    </a>
    <figcaption style="font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.6rem; letter-spacing:0.04em;">Potentiel minier du sous-sol français — BRGM 2023 · Cliquer pour explorer →</figcaption>
  </figure>

  <p>« On aurait dû investir comme la Chine ! » Mais ce qu'on oublie de dire, c'est le prix social et environnemental des mines. Et c'est peut-être le point le plus important à retenir de cet article ! </p>

  <p>Le projet EMILI, porté par Imerys à Échassières (dans l'Allier), l'illustre bien : 34 000 tonnes d'hydroxyde de lithium visées chaque année, de quoi équiper environ 700 000 véhicules électriques, pour vingt-cinq ans d'exploitation. Un projet jugé stratégique par l'État, mais qui cristallise une opposition locale entre riverains inquiets pour l'eau et associations qui y voient un extractivisme déguisé en transition verte.</p>

  <p> Ouvrir de nouvelles mines, de nouvelles usines de raffinage ou même de recyclage, en France comme ailleurs, ce n'est jamais un geste neutre : l'extraction et la transformation sont des procédés gourmands en énergie, historiquement fossile, et pèsent sur la biodiversité, les sols, l'eau, sans compter les déchets miniers à gérer sur le long terme, le paysage et le travail humain souvent totalement inéthique. </p> 

  <figure style="margin: 2rem 0;">
    <a href="https://reporterre.net/Les-ravages-ignores-de-l-activite-miniere" target="_blank" rel="noopener">
      <img src="{{ site.baseurl }}/assets/img/mine-reporterre.png" alt="Les ravages ignorés de l'activité minière — Reporterre" style="width:100%; border-radius:8px; display:block; border:1px solid #eee;">
    </a>
    <figcaption style="font-size:0.75rem; color:#aaa; text-align:center; margin-top:0.6rem; letter-spacing:0.04em;"> La mine de cuivre de Palabora (Afrique du Sud) : à gauche, la représentation imagée de la quantité de cuivre métal produite par la mine jusqu’à environ 2007  ; à droite, l’emprise en surface des déchets miniers en vue satellitaire. © Dillon Marsh/Google 2021/Création SystExt/septembre 2021, Src: Reporterre · Cliquer pour lire →</figcaption>
  </figure>

  <div class="callout">
    <p>Reste une question, que nous vous laissons explorer : une mine peut-elle vraiment être durable et équitable ?</p>
  </div>


  <h2 id="conclusion">Que dire, au final ?</h2>

    <p>La transition énergétique et la révolution numérique nous rendent de plus en plus dépendants d'une poignée de métaux, extraits et transformés dans un nombre très restreint de pays. Cette dépendance s'est matérialisée en 2025 sous la forme de restrictions à l'export, puis en 2026 avec la crise du soufre après la fermeture du détroit d'Ormuz... Des stratégies émergent pour répondre à ces fragilités en chaîne : sécuriser des accords commerciaux, constituer des stocks, diversifier ses fournisseurs, mais aussi la low-tech, le recyclage ou l'efficacité énergétique.</p>

    <p>Il manque pourtant un pilier à ces stratégies, moins spectaculaire que les mines ou les réserves stratégiques, mais bien plus efficace : <strong>la sobriété</strong>. Puisqu'on ne peut pas tout électrifier avec un stock de métaux fini, la vraie question devient : de quoi accepterons-nous de nous passer ?</p>

    <p>Elle entraîne une autre question : où investir les ressources qui restent, et pour qui ? Prioriser l'accès à la voiture électrique en zone rurale et les transports en commun en ville ? Ce sont ces questions d'équité qui vont se jouer dans les années qui viennent, et ce sont aussi celles que pose le jeu Scenario.</p>

    <p><strong>Au final, savoir se restreindre n'est pas qu'un enjeu écologique : c'est aussi, peut-être, notre meilleure arme stratégique.<strong>

  <div class="post-sources">
    <h2>Sources</h2>
    <ul>
      <li><a href="https://www.iea.org/reports/global-critical-minerals-outlook-2026" target="_blank" rel="noopener">AIE — <em>Global Critical Minerals Outlook 2026</em></a> — rapport principal (projections de demande p. 110-115, raffinage chinois p. 121, recyclage p. 120-123, investissements p. 112-115, G7 p. 94, stratégies nationales p. 92-95) et résumé exécutif (déficits d'offre p. 6-7, prix p. 6, acide sulfurique p. 8, surcoût de diversification p. 10, impact consommateur p. 11, Amérique latine p. 12-13)</li>
      <li><a href="https://www.consilium.europa.eu/fr/infographics/critical-raw-materials-act/" target="_blank" rel="noopener">Conseil de l'Union européenne — Critical Raw Materials Act</a></li>
      <li><a href="https://www.entreprises.gouv.fr/fr/actualites/terres-rares-aimants-permanents" target="_blank" rel="noopener">Direction générale des Entreprises — Plan national terres rares et aimants permanents</a></li>
      <li><a href="https://www.mpmaterials.com" target="_blank" rel="noopener">MP Materials — Partenariat avec le département de la Défense américain</a></li>
      <li><a href="https://www.brgm.fr/fr/reference/inventaire-national-ressources-minerales-metalliques" target="_blank" rel="noopener">BRGM — Inventaire national des ressources minérales</a></li>
      <li><a href="https://www.mineralinfo.fr/fr/potentiel-du-sous-sol-francais-exploration" target="_blank" rel="noopener">MineralInfo — Potentiel du sous-sol français : exploration</a></li>
      <li><a href="https://emili.imerys.com" target="_blank" rel="noopener">Imerys — Projet EMILI (lithium, Allier)</a></li>
      <li><a href="https://www.fne.asso.fr/communiques/mine-de-lithium-dans-lallier-creusons-le-sujet" target="_blank" rel="noopener">France Nature Environnement — Mine de lithium dans l'Allier : creusons le sujet</a></li>
      <li><a href="https://reporterre.net/Les-ravages-ignores-de-l-activite-miniere" target="_blank" rel="noopener">Reporterre — Les ravages ignorés de l'activité minière</a></li>
      <li><a href="https://www.vie-publique.fr/en-bref/299667-minerais-et-metaux-critiques-mieux-securiser-les-approvisionnements" target="_blank" rel="noopener">Vie publique — Minerais et métaux critiques : mieux sécuriser les approvisionnements</a></li>
      <li><a href="https://news.un.org/fr/story/2026/03/1158514" target="_blank" rel="noopener">ONU Info — Minerais critiques et transition énergétique</a></li>
      <li><a href="https://www.consilium.europa.eu/fr/infographics/critical-raw-materials-explained/" target="_blank" rel="noopener">Conseil de l'UE — Les matières premières critiques expliquées</a></li>
      <li><a href="https://greenit.eco/nos-etudes-et-essais/etat-des-reserves-mondiales-de-metaux-2025/" target="_blank" rel="noopener">GreenIT — État des réserves mondiales de métaux 2025</a></li>
    </ul>
  </div>

  <div class="post-back">
    <a href="{{ site.baseurl }}/blog">← Retour au Blog</a>
  </div>

</div>
