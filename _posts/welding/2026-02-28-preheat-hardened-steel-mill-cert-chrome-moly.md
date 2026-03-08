---
layout: article
title: "Preheat on Hardened Steel: What the Mill Cert Tells You and What Happens When You Skip It"
description: "Real-shop preheat practice on 4041 chrome-moly pins and wear plate hardfacing. CE calculation, temperature control with heat crayons, and what one wrong wire choice cost us."
date: 2026-02-28
category: welding
permalink: /blog/welding/preheat-hardened-steel-mill-cert-chrome-moly/
image: /images/blog/preheat-chromoly-pin-shop.webp
image_alt: "Heat crayon melting on a 4041 chrome-moly pin at 400°F before FCAW welding"
image_caption: "Heat crayon verification on a 4041 chrome-moly pin before welding. When it melts, you weld. Not before."
read_time: 9

tags:
  - Preheat
  - Chrome-Moly
  - 4041
  - Hardfacing
  - FCAW
  - Mill Certificate
  - Mining Equipment

faq:
  - q: "What preheat temperature is required for 4041 chrome-moly steel?"
    a: "For a quenched and tempered 4041 pin or shaft, 400°F (204°C) is a commonly used minimum preheat. The exact value should always be calculated from the mill cert using the CE(IIW) formula per AWS D1.1 Annex I, since the chemistry can vary between heats. The preheat zone should extend at least 3 inches on each side of the weld."
  - q: "Why is an infrared thermometer unreliable for preheat verification on steel?"
    a: "IR guns calculate temperature by measuring infrared radiation and applying an emissivity factor. On mill-scale or oxidized steel surfaces, the emissivity varies significantly and the reading angle matters. Errors of 30 to 50°C are common. Heat crayons give a direct, reliable go/no-go indication at a specific temperature and are far more trustworthy for preheat verification in shop or field conditions."
  - q: "What happens if you use the wrong filler wire on a hardfacing job?"
    a: "If the tensile classification of the wire is too low for the application, the deposit will be softer and weaker than designed. On a high-strength base metal without adequate preheat, you also create a steep hardness gradient at the fusion line that generates stress concentrations. The result is cracking, sometimes fine enough to miss without good lighting, but always a problem that requires repair or scrapping the part."
  - q: "Should I preheat the entire part or just the weld zone?"
    a: "You need to bring the full weld zone to temperature, a minimum of 3 inches on each side of the joint. You also need the surrounding mass warm enough that it does not pull the temperature back down as soon as you stop torching. On a heavy pin or shaft, preheating only the immediate area creates a temperature gradient that can crack the base metal away from the weld during or after welding."
  - q: "What is the best way to slow-cool a welded chrome-moly part?"
    a: "Burying the part in a closed container filled with dry sand or gravel is an effective and practical method for shop work. The thermal mass of the sand insulates the part and forces a very slow, even cool-down. A properly buried pin can still be warm to the touch the following morning, which is exactly what you want. Ceramic fiber blankets are an alternative on larger or awkwardly shaped parts."

howto:
  name: "How to Preheat and Post-Cool a Chrome-Moly Pin or Shaft Repair"
  description: "Practical procedure for preheating a 4041 chrome-moly pin before welding and controlling the cool-down, based on shop practice with hardfacing and structural repair."
  steps:
    - name: "Pull the mill cert and calculate the CE"
      text: "Get the actual heat chemistry for the steel you are welding. Apply the CE(IIW) formula: CE = C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15. For a 4041-class chrome-moly steel, expect a CE in the range of 0.55 to 0.70. This confirms that preheating is required and gives you the basis for determining the minimum temperature."
    - name: "Select the right filler metal"
      text: "Match the wire or electrode to the base metal strength and the application. For a structural or build-up repair on a 4041 pin, you need a wire classified to the appropriate tensile strength, typically 110 ksi (760 MPa) minimum, such as Lincoln Electric Metalshield MC-110 (E110C-K4 H4). Never grab a general-purpose wire off the shelf without checking the classification against the WPS or the engineer specification."
    - name: "Apply heat to the full preheat zone"
      text: "Use a propane rosebud or oxy-acetylene torch to heat the weld zone plus a minimum of 3 inches on each side. Move the torch continuously to heat evenly. On a heavy pin, this takes time. Rushing it produces a hot surface with a cold core, which is worse than no preheat."
    - name: "Verify temperature with heat crayons"
      text: "Use a Tempilstik rated at your target temperature. Mark the steel at least 75mm from the weld centerline. When the crayon mark goes wet and shiny, you are at temperature. Do not use an infrared gun as your primary check. Emissivity errors on mill-scale steel make it unreliable."
    - name: "Weld and maintain interpass temperature"
      text: "Strike the arc once temperature is confirmed. Between passes, recheck with the crayon before every pass. Do not let the part drop below minimum preheat at any point during the repair. On a chrome-moly pin in a cool shop, heat loss is faster than you expect."
    - name: "Slow-cool in sand or gravel"
      text: "Once the final pass is complete, bury the part in a closed bin packed with dry sand or gravel. Pack the sand around the full part, close the lid, and leave it until the following day. The part should still be warm to the touch in the morning. This ensures hydrogen has time to diffuse and the cooling rate stays low enough to avoid martensite formation in the HAZ."
---

I work a lot with hardened and tempered steels. Pins, shafts, structural components on forestry conveyors and heavy mining equipment. These parts come in quenched and tempered, and they need to go back into service with their mechanical properties intact. That means the welding procedure has to be right, and it starts well before you strike an arc.

The most important document on a job like this is the mill cert. Not the material designation on the drawing, not what the supplier told you over the phone, but the actual cert for that heat of steel. I pull it every time, without exception. The reason is simple. A designation like 4041 or 4140 is a family, not a fixed chemistry. Two bars with the same name from different heats can have different carbon, manganese, and chromium content, and those differences move the carbon equivalent in ways that matter.

The CE(IIW) formula is what I use: CE = C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15. You plug in the weight percentages directly from the cert. For a typical 4041 chrome-moly shaft, you'll land somewhere between 0.55 and 0.70. Anything above 0.45 means preheat is mandatory. At 0.60 and above, you're dealing with a steel that will crack if you don't take the procedure seriously.

<!-- Visualisation 1 : Calculateur CE(IIW) interactif -->
<!-- Entrez les valeurs de votre mill cert et le calculateur affiche le CE et la zone de risque -->
<!-- ============================================================
     Visualisation : Calculateur Carbone Équivalent CE(IIW) — v2
     Article : "Preheat on Hardened Steel — What the Mill Cert Tells You"
     Blog : wallid-guergour.com | Jekyll / GitHub Pages
     Dépendance : D3.js v7 via CDN (utilisé pour la sélection DOM uniquement)
     Correctif v2 : remplacement D3.arc par SVG path manuel (coordonnées
                    trigonométriques standard) pour aligner zones et labels.
     ============================================================ -->

<div id="viz-ce-iiw" style="width:100%; max-width:720px; margin:32px auto;"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js"></script>
<script>
(function() {

  // ── Charte graphique ──────────────────────────────────────────
  const C = {
    bg:              '#0B0F14',
    bgCard:          '#111820',
    bgInput:         '#0d1319',
    accent:          '#F2DBC2',
    white:           '#FFFFFF',
    textSub:         'rgba(255,255,255,0.55)',
    border:          'rgba(255,255,255,0.08)',
    zoneOk:          '#3d6e4e',
    zoneWarn:        '#8c6a2a',
    zoneDanger:      '#7a2a2a',
    zoneOkBright:    '#6db88a',
    zoneWarnBright:  '#e8b84b',
    zoneDangerBright:'#d45f5f',
  };

  // ── Valeurs par défaut (mill cert typique 4041) ──────────────
  const defaults = { C: 0.38, Mn: 0.80, Cr: 0.95, Mo: 0.20, V: 0.00, Ni: 0.00, Cu: 0.00 };

  // ── Formule CE(IIW) — AWS D1.1 Annex I ──────────────────────
  function calcCE(v) {
    return v.C + v.Mn/6 + (v.Cr + v.Mo + v.V)/5 + (v.Ni + v.Cu)/15;
  }

  // ── Zones de risque ──────────────────────────────────────────
  function getZone(ce) {
    if (ce < 0.45) return {
      label: 'Low Risk',
      sub:   'Preheat generally not required for most thicknesses. Verify per WPS.',
      color: C.zoneOkBright,
      bg:    'rgba(61,110,78,0.15)',
    };
    if (ce < 0.60) return {
      label: 'Preheat Required',
      sub:   'Minimum preheat mandatory. Temperature depends on thickness and heat input. Check WPS.',
      color: C.zoneWarnBright,
      bg:    'rgba(140,106,42,0.15)',
    };
    return {
      label: 'Critical — High Crack Risk',
      sub:   'High preheat (200°C +) and post-weld treatment required. Do not improvise.',
      color: C.zoneDangerBright,
      bg:    'rgba(122,42,42,0.18)',
    };
  }

  // ── Système de coordonnées de la jauge ───────────────────────
  // Jauge = demi-cercle du côté, de gauche (9h) à droite (3h) en passant par le haut.
  // CE=0 → angle π (gauche), CE=1 → angle 0 (droite)
  // Coordonnées SVG : x = cx + r·cos(θ), y = cy − r·sin(θ)
  const ceMin = 0, ceMax = 1.0;
  const gaugeW = 260, gaugeH = 148;
  const cx = gaugeW / 2;
  const cy = gaugeH - 10;   // pivot en bas du SVG
  const rOuter = 100, rInner = 62;

  function ceToAngle(ce) {
    // CE 0 → angle π (gauche), CE 1 → angle 0 (droite)
    const frac = Math.max(0, Math.min(1, (ce - ceMin) / (ceMax - ceMin)));
    return Math.PI * (1 - frac);
  }

  function angleToSVG(theta, r) {
    // Angle trigonométrique → coordonnées SVG (y inversé)
    return { x: cx + r * Math.cos(theta), y: cy - r * Math.sin(theta) };
  }

  // Dessine un arc de donut (anneau) entre deux valeurs CE
  function makeDonutPath(ce1, ce2) {
    const a1 = ceToAngle(ce1);  // angle pour ce1 (côté gauche du segment)
    const a2 = ceToAngle(ce2);  // angle pour ce2 (côté droit, a2 < a1)
    const o1 = angleToSVG(a1, rOuter);
    const o2 = angleToSVG(a2, rOuter);
    const i1 = angleToSVG(a1, rInner);
    const i2 = angleToSVG(a2, rInner);
    // Arc de plus de 180° ?
    const large = (a1 - a2) > Math.PI ? 1 : 0;
    // SVG : sweep-flag=1 = sens horaire sur écran
    return [
      `M ${o1.x.toFixed(2)} ${o1.y.toFixed(2)}`,
      `A ${rOuter} ${rOuter} 0 ${large} 1 ${o2.x.toFixed(2)} ${o2.y.toFixed(2)}`,
      `L ${i2.x.toFixed(2)} ${i2.y.toFixed(2)}`,
      `A ${rInner} ${rInner} 0 ${large} 0 ${i1.x.toFixed(2)} ${i1.y.toFixed(2)}`,
      'Z'
    ].join(' ');
  }

  // Rotation SVG de l'aiguille (part de la position "vers le haut")
  function ceToNeedleRotation(ce) {
    const theta = ceToAngle(ce) * 180 / Math.PI;  // en degrés
    return -(theta - 90);   // CW en SVG, 0° = pointe vers le haut
  }

  // ── Construction du DOM ──────────────────────────────────────
  const container = document.getElementById('viz-ce-iiw');
  container.style.cssText = `
    font-family: Arial, sans-serif;
    background: ${C.bgCard};
    border: 1px solid ${C.border};
    border-radius: 4px;
    overflow: hidden;
    box-sizing: border-box;
  `;

  // En-tête
  const header = document.createElement('div');
  header.style.cssText = `
    padding: 18px 24px 14px;
    border-bottom: 1px solid ${C.border};
    display: flex;
    align-items: baseline;
    gap: 12px;
    flex-wrap: wrap;
  `;
  header.innerHTML = `
    <span style="font-size:11px; letter-spacing:0.12em; text-transform:uppercase;
                 color:${C.accent}; font-weight:600;">CE(IIW) Calculator</span>
    <span style="font-size:11px; color:${C.textSub}; font-family:'Courier New',monospace;">
      C + Mn/6 + (Cr+Mo+V)/5 + (Ni+Cu)/15
    </span>
  `;
  container.appendChild(header);

  // Corps
  const body = document.createElement('div');
  body.style.cssText = 'display:flex; flex-wrap:wrap;';
  container.appendChild(body);

  // ── Panneau gauche : inputs ──────────────────────────────────
  const leftPanel = document.createElement('div');
  leftPanel.style.cssText = `
    flex: 1 1 280px;
    padding: 20px 24px;
    border-right: 1px solid ${C.border};
    box-sizing: border-box;
  `;
  body.appendChild(leftPanel);

  const inputLabel = document.createElement('p');
  inputLabel.style.cssText = `margin:0 0 14px; font-size:10px; letter-spacing:0.1em;
                               text-transform:uppercase; color:${C.textSub};`;
  inputLabel.textContent = 'Mill Cert Values (wt%)';
  leftPanel.appendChild(inputLabel);

  const fields = [
    { key:'C',  label:'C',  name:'Carbon',     hint:'0.35–0.43', weight:'× 1'  },
    { key:'Mn', label:'Mn', name:'Manganese',  hint:'0.60–1.00', weight:'÷ 6'  },
    { key:'Cr', label:'Cr', name:'Chromium',   hint:'0.80–1.10', weight:'÷ 5'  },
    { key:'Mo', label:'Mo', name:'Molybdenum', hint:'0.15–0.25', weight:'÷ 5'  },
    { key:'V',  label:'V',  name:'Vanadium',   hint:'0.00–0.05', weight:'÷ 5'  },
    { key:'Ni', label:'Ni', name:'Nickel',     hint:'0.00–0.25', weight:'÷ 15' },
    { key:'Cu', label:'Cu', name:'Copper',     hint:'0.00–0.35', weight:'÷ 15' },
  ];

  const values = { ...defaults };
  const inputRefs = {};

  fields.forEach(f => {
    const row = document.createElement('div');
    row.style.cssText = 'display:flex; align-items:center; margin-bottom:8px; gap:8px;';

    const badge = document.createElement('span');
    badge.style.cssText = `display:inline-block; width:26px; text-align:center;
                            font-size:12px; font-weight:700; color:${C.accent}; flex-shrink:0;`;
    badge.textContent = f.label;

    const name = document.createElement('span');
    name.style.cssText = `font-size:11px; color:${C.textSub}; flex:1; min-width:70px;`;
    name.textContent = f.name;

    // type="text" pour éviter le bug de locale (virgule vs point)
    const inp = document.createElement('input');
    inp.type  = 'text';
    inp.inputMode = 'decimal';
    inp.value = defaults[f.key].toFixed(2);
    inp.style.cssText = `
      width: 68px;
      background: ${C.bgInput};
      border: 1px solid ${C.border};
      color: ${C.white};
      font-size: 12px;
      font-family: 'Courier New', monospace;
      padding: 5px 8px;
      text-align: right;
      border-radius: 2px;
      outline: none;
      box-sizing: border-box;
      flex-shrink: 0;
    `;
    inp.addEventListener('focus', () => { inp.style.borderColor = C.accent; });
    inp.addEventListener('blur',  () => { inp.style.borderColor = C.border; });
    inp.addEventListener('input', () => {
      // Accepte virgule (locale FR) ou point comme séparateur décimal
      const raw = inp.value.replace(',', '.');
      const val = parseFloat(raw);
      values[f.key] = isNaN(val) ? 0 : Math.max(0, val);
      update();
    });

    const wt = document.createElement('span');
    wt.style.cssText = `font-size:10px; color:rgba(255,255,255,0.28); width:28px;
                         text-align:right; flex-shrink:0; font-family:'Courier New',monospace;`;
    wt.textContent = f.weight;

    row.appendChild(badge); row.appendChild(name);
    row.appendChild(inp);   row.appendChild(wt);
    leftPanel.appendChild(row);
    inputRefs[f.key] = inp;
  });

  const note = document.createElement('p');
  note.style.cssText = `margin:16px 0 0; font-size:10px; color:rgba(255,255,255,0.28); line-height:1.5;`;
  note.innerHTML = 'Enter values from your actual heat cert.<br>CE(IIW) per AWS D1.1 Annex I.';
  leftPanel.appendChild(note);

  // ── Panneau droit : jauge SVG + résultat ─────────────────────
  const rightPanel = document.createElement('div');
  rightPanel.style.cssText = `
    flex: 1 1 260px;
    padding: 20px 16px 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;
  `;
  body.appendChild(rightPanel);

  // Conteneur SVG
  const gaugeDiv = document.createElement('div');
  gaugeDiv.style.cssText = 'width:100%; max-width:260px;';
  rightPanel.appendChild(gaugeDiv);

  // ── Construction SVG de la jauge ─────────────────────────────
  const svg = d3.select(gaugeDiv)
    .append('svg')
    .attr('viewBox', `0 0 ${gaugeW} ${gaugeH}`)
    .attr('width', '100%')
    .attr('preserveAspectRatio', 'xMidYMid meet')
    .style('overflow', 'visible');

  // Segments de zone (SVG path manuel — coordonnées trig standard)
  const zones = [
    { ce1: 0,    ce2: 0.45, color: C.zoneOk     },
    { ce1: 0.45, ce2: 0.60, color: C.zoneWarn   },
    { ce1: 0.60, ce2: 1.0,  color: C.zoneDanger },
  ];

  zones.forEach(z => {
    svg.append('path')
      .attr('d', makeDonutPath(z.ce1, z.ce2))
      .attr('fill', z.color)
      .attr('opacity', 0.88);
  });

  // Séparateurs de seuil (traits radiaux à 0.45 et 0.60)
  [0.45, 0.60].forEach(thresh => {
    const a  = ceToAngle(thresh);
    const p1 = angleToSVG(a, rInner - 2);
    const p2 = angleToSVG(a, rOuter + 2);
    svg.append('line')
      .attr('x1', p1.x).attr('y1', p1.y)
      .attr('x2', p2.x).attr('y2', p2.y)
      .attr('stroke', C.bgCard)
      .attr('stroke-width', 2.5);
  });

  // Labels de zone centrés sur chaque arc
  const zoneMids = [
    { ce: 0.22, text: 'Low Risk',  color: C.zoneOkBright    },
    { ce: 0.52, text: 'Preheat',   color: C.zoneWarnBright  },
    { ce: 0.80, text: 'Critical',  color: C.zoneDangerBright },
  ];
  const rLabel = (rInner + rOuter) / 2;
  zoneMids.forEach(l => {
    const pos = angleToSVG(ceToAngle(l.ce), rLabel);
    svg.append('text')
      .attr('x', pos.x).attr('y', pos.y)
      .attr('text-anchor', 'middle')
      .attr('dominant-baseline', 'middle')
      .attr('fill', l.color)
      .attr('font-size', '7.5')
      .attr('font-weight', '700')
      .attr('font-family', 'Arial, sans-serif')
      .attr('letter-spacing', '0.04em')
      .text(l.text);
  });

  // Labels de seuil numériques (0.45, 0.60)
  [0.45, 0.60].forEach(thresh => {
    const pos = angleToSVG(ceToAngle(thresh), rOuter + 13);
    svg.append('text')
      .attr('x', pos.x).attr('y', pos.y)
      .attr('text-anchor', 'middle')
      .attr('dominant-baseline', 'middle')
      .attr('fill', C.textSub)
      .attr('font-size', '9')
      .attr('font-family', 'Courier New, monospace')
      .text(thresh.toFixed(2));
  });

  // Labels extrémités (0.0 et 1.0)
  [
    { ce: 0,   anchor: 'end'   },
    { ce: 1.0, anchor: 'start' },
  ].forEach(l => {
    const pos = angleToSVG(ceToAngle(l.ce), rOuter + 12);
    const dx = l.anchor === 'end' ? -4 : 4;
    svg.append('text')
      .attr('x', pos.x + dx).attr('y', pos.y)
      .attr('text-anchor', l.anchor)
      .attr('dominant-baseline', 'middle')
      .attr('fill', C.textSub)
      .attr('font-size', '9')
      .attr('font-family', 'Courier New, monospace')
      .text(l.ce.toFixed(1));
  });

  // Aiguille : groupe transformé par rotation
  const needleGroup = svg.append('g')
    .attr('transform', `translate(${cx},${cy}) rotate(0)`);

  needleGroup.append('line')
    .attr('x1', 0).attr('y1', 4)
    .attr('x2', 0).attr('y2', -(rOuter - 8))
    .attr('stroke', C.accent)
    .attr('stroke-width', 2.5)
    .attr('stroke-linecap', 'round');

  // Hub central
  svg.append('circle')
    .attr('cx', cx).attr('cy', cy)
    .attr('r', 6)
    .attr('fill', C.accent);

  // ── Affichage valeur CE ──────────────────────────────────────
  const ceDisplay = document.createElement('div');
  ceDisplay.style.cssText = 'text-align:center; margin-top:-4px;';
  ceDisplay.innerHTML = `
    <div id="ce-value" style="
      font-size:40px; font-weight:700;
      font-family:'Courier New',monospace;
      color:${C.accent}; line-height:1; letter-spacing:-1px;">0.000</div>
    <div style="font-size:10px; text-transform:uppercase; letter-spacing:0.1em;
                color:${C.textSub}; margin-top:4px;">Carbon Equivalent</div>
  `;
  rightPanel.appendChild(ceDisplay);

  // Bloc recommandation
  const recBox = document.createElement('div');
  recBox.id = 'ce-rec';
  recBox.style.cssText = `
    margin-top: 14px;
    padding: 11px 14px;
    border-radius: 3px;
    width: 100%;
    box-sizing: border-box;
    text-align: center;
    transition: background 0.25s, border-color 0.25s;
  `;
  rightPanel.appendChild(recBox);

  // ── Mise à jour ──────────────────────────────────────────────
  function update() {
    const ce = calcCE(values);
    const zone = getZone(ce);
    const rotation = ceToNeedleRotation(Math.max(ceMin, Math.min(ceMax, ce)));

    // Rotation aiguille
    needleGroup.attr('transform', `translate(${cx},${cy}) rotate(${rotation.toFixed(2)})`);

    // Valeur CE
    document.getElementById('ce-value').textContent = ce.toFixed(3);
    document.getElementById('ce-value').style.color = zone.color;

    // Bloc recommandation
    recBox.style.background   = zone.bg;
    recBox.style.border       = `1px solid ${zone.color}33`;
    recBox.innerHTML = `
      <div style="font-size:12px; font-weight:700; color:${zone.color};
                  letter-spacing:0.06em; text-transform:uppercase; margin-bottom:6px;">${zone.label}</div>
      <div style="font-size:11px; color:${C.textSub}; line-height:1.5;">${zone.sub}</div>
    `;
  }

  update();
})();
</script>

## What 400°F actually means in practice

On pins for heavy equipment, the target I work to is 400°F, which is around 204°C, and that temperature has to be reached and held across the full preheat zone. A minimum of three inches on each side of the weld, six inches total. I've seen guys heat a small area right at the joint and call it good. That's not preheat. That's a hot surface on a cold mass, and the thermal gradient you create that way can crack the base metal away from the weld before you even finish the first pass.

The torch work matters too. You move the rosebud continuously, covering the whole zone, letting the heat soak in rather than concentrating it on one spot. On a heavy pin, this takes longer than most people expect. Rushing it gets you a hot skin and a cold core, which is about the worst situation you can have going into a weld on chrome-moly.

<!-- Visualisation 2 : Diffusion thermique radiale — Rush vs Correct -->
<!-- Simulation physique de la pénétration de chaleur dans un pin Ø150mm -->
<!-- Rush = surface à 400°F en 90 secondes (mauvaise pratique) -->
<!-- Correct = trempage lent en 10 minutes (bonne pratique) -->
<!-- ============================================================
     Visualisation : Diffusion thermique radiale — Rush vs Correct
     Article : "Preheat on Hardened Steel — What the Mill Cert Tells You"
     Blog : wallid-guergour.com | Jekyll / GitHub Pages
     Dépendance : P5.js 1.9.0 via CDN Cloudflare (mode instance)

     Physique : équation de chaleur en coordonnées cylindriques
       ∂T/∂t = α · [∂²T/∂r² + (1/r)·∂T/∂r]
     Schéma explicite — différences finies, pas radial dr = R/N
     ============================================================ -->

<div id="viz-thermal" style="width:100%; max-width:720px; margin:32px auto; line-height:0;"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.0/p5.min.js"></script>
<script>
new p5(function(p) {

  // ── Paramètres physiques ──────────────────────────────────────
  // Modifiez ces valeurs pour correspondre à votre pièce réelle
  const T_AMB    = 20;    // °C — température ambiante
  const T_TARG   = 204;   // °C = 400°F — cible de préchauffage
  const N        = 65;    // points radiaux (résolution de la grille)
  const R_MM     = 75;    // rayon réel du pin en mm (axe Ø150mm)
  const ALPHA    = 5.3;   // diffusivité thermique 4140 acier Cr-Mo (mm²/s)

  const dr       = R_MM / (N - 1);
  // Limite de stabilité du schéma explicite (critère CFL)
  const DT_MAX   = 0.9 * dr * dr / (2 * ALPHA);  // secondes

  // Accélération temporelle : 1 seconde animation = TSCALE secondes réelles
  const TSCALE = 90;

  // Durée réelle (secondes) pour que la surface atteigne T_TARG
  const RAMP_RUSH    =  90;   // 1 min 30 → chauffage agressif
  const RAMP_CORRECT = 600;   // 10 min  → trempage lent

  // ── État de la simulation ─────────────────────────────────────
  let T_R, T_C;   // tableaux de température (Rush, Correct)
  let t_sim;      // temps réel écoulé (secondes)
  let paused;

  // ── Mise en page ──────────────────────────────────────────────
  let W, H, R_PX;
  let lcx, lcy, rcx, rcy;
  let btnReset, btnPause;
  let timerStr = '0m 00s';

  function resetSim() {
    T_R    = new Array(N).fill(T_AMB);
    T_C    = new Array(N).fill(T_AMB);
    t_sim  = 0;
    paused = false;
  }

  // ── Température → couleur ─────────────────────────────────────
  // Palette : bleu nuit (froid) → rouille sombre → orange chaud
  function tCol(T_val) {
    const f = p.constrain((T_val - T_AMB) / (T_TARG - T_AMB), 0, 1);
    let r, g, b;
    if (f < 0.35) {
      const t = f / 0.35;
      r = p.lerp(8,   52, t);
      g = p.lerp(18,  28, t);
      b = p.lerp(48,  12, t);
    } else if (f < 0.72) {
      const t = (f - 0.35) / 0.37;
      r = p.lerp(52,  172, t);
      g = p.lerp(28,   72, t);
      b = p.lerp(12,   18, t);
    } else {
      const t = (f - 0.72) / 0.28;
      r = p.lerp(172, 234, t);
      g = p.lerp(72,  138, t);
      b = p.lerp(18,   52, t);
    }
    return p.color(r, g, b);
  }

  // ── Température de surface (rampe linéaire) ───────────────────
  function Tsurf(t, ramp) {
    return T_AMB + (T_TARG - T_AMB) * Math.min(1, t / ramp);
  }

  // ── Pas de différences finies (schéma explicite) ─────────────
  function stepFD(T, dt, Ts) {
    const Tn = T.slice();
    // Condition aux limites : surface à température imposée
    Tn[N - 1] = Ts;
    // Centre (symétrie → limite de L'Hôpital : ∂²T/∂r²|r=0 = 2·∂²T/∂r²)
    Tn[0] = T[0] + ALPHA * dt * 2 * (T[1] - T[0]) / (dr * dr);
    // Nœuds intérieurs
    for (let i = 1; i < N - 1; i++) {
      const ri = i * dr;
      const d2 = (T[i + 1] - 2 * T[i] + T[i - 1]) / (dr * dr);
      const d1 = (T[i + 1] - T[i - 1]) / (2 * dr * ri);
      Tn[i] = T[i] + ALPHA * dt * (d2 + d1);
    }
    Tn[N - 1] = Ts;
    return Tn;
  }

  // ── Dessin du pin (cercles concentriques) ─────────────────────
  function drawPin(cx, cy, T_arr) {
    p.noStroke();
    for (let i = N - 1; i >= 0; i--) {
      const rDraw = (i / (N - 1)) * R_PX;
      p.fill(tCol(T_arr[i]));
      p.ellipse(cx, cy, rDraw * 2, rDraw * 2);
    }
    // Cerclage acier
    p.noFill();
    p.stroke(95, 108, 120);
    p.strokeWeight(2);
    p.ellipse(cx, cy, R_PX * 2 + 3, R_PX * 2 + 3);
    p.noStroke();
  }

  // ── Readout de température (boîtes Surface / Core) ────────────
  function drawReadout(cx, T_arr) {
    const cToF  = c => Math.round(c * 9 / 5 + 32);
    const surf_F = cToF(T_arr[N - 1]);
    const core_F = cToF(T_arr[0]);

    const boxW  = 62, boxH = 36, gap = 7;
    const yR    = lcy + R_PX + 20;
    const bx1   = cx - boxW - gap / 2;   // boîte Surface
    const bx2   = cx + gap / 2;          // boîte Core

    function miniBox(bx, label, valF, T_val) {
      const c = tCol(T_val);
      const cr = p.red(c), cg = p.green(c), cb = p.blue(c);
      // Fond teinté
      p.fill(cr * 0.25, cg * 0.25, cb * 0.25, 200);
      p.stroke(cr, cg, cb, 70);
      p.strokeWeight(1);
      p.rect(bx, yR, boxW, boxH, 2);
      p.noStroke();
      // Libellé
      p.fill(255, 255, 255, 90);
      p.textSize(7.5);
      p.textStyle(p.NORMAL);
      p.textAlign(p.CENTER, p.TOP);
      p.text(label, bx + boxW / 2, yR + 5);
      // Valeur
      p.fill(Math.min(cr + 45, 255), Math.min(cg + 35, 255), Math.min(cb + 35, 255));
      p.textSize(12);
      p.textStyle(p.BOLD);
      p.text(valF + '°F', bx + boxW / 2, yR + 17);
    }

    miniBox(bx1, 'SURFACE', surf_F, T_arr[N - 1]);
    miniBox(bx2, 'CORE',    core_F, T_arr[0]);
  }

  // ── Hit test et dessin boutons ────────────────────────────────
  function hitBtn(btn) {
    return p.mouseX >= btn.x && p.mouseX <= btn.x + btn.w
        && p.mouseY >= btn.y && p.mouseY <= btn.y + btn.h;
  }

  function drawBtn(btn) {
    const h = hitBtn(btn);
    p.fill(h ? 52 : 20, h ? 64 : 28, h ? 78 : 36);
    p.stroke(242, 219, 194, h ? 160 : 70);
    p.strokeWeight(1);
    p.rect(btn.x, btn.y, btn.w, btn.h, 3);
    p.noStroke();
    p.fill(242, 219, 194, h ? 255 : 180);
    p.textAlign(p.CENTER, p.CENTER);
    p.textSize(10);
    p.textStyle(p.NORMAL);
    p.text(btn.label, btn.x + btn.w / 2, btn.y + btn.h / 2);
  }

  // ── Setup ─────────────────────────────────────────────────────
  p.setup = function() {
    const el = document.getElementById('viz-thermal');
    W    = Math.min(Math.max(el.offsetWidth || 660, 320), 660);
    H    = 420;
    R_PX = Math.round(Math.min(102, W * 0.148));

    lcx  = Math.round(W * 0.255);
    rcx  = Math.round(W * 0.745);
    lcy  = rcy = Math.round(H * 0.415);   // remonté pour dégager le bas

    const cnv = p.createCanvas(W, H);
    cnv.parent('viz-thermal');
    cnv.elt.style.display = 'block';

    const bw = 92, bh = 28;
    btnReset = { x: W / 2 - bw - 7, y: H - 38, w: bw, h: bh, label: 'Reset'   };
    btnPause = { x: W / 2 + 7,       y: H - 38, w: bw, h: bh, label: 'Pause ‖' };

    resetSim();
    p.frameRate(30);
  };

  // ── Draw ──────────────────────────────────────────────────────
  p.draw = function() {

    // ── Avance la simulation ───────────────────────────────────
    if (!paused) {
      const dtAnim  = Math.min(p.deltaTime / 1000, 0.05); // cap pour éviter les sauts
      const dtReal  = dtAnim * TSCALE;
      const Ts_R    = Tsurf(t_sim, RAMP_RUSH);
      const Ts_C    = Tsurf(t_sim, RAMP_CORRECT);

      let rem = dtReal;
      while (rem > 0) {
        const dt = Math.min(DT_MAX, rem);
        T_R = stepFD(T_R, dt, Ts_R);
        T_C = stepFD(T_C, dt, Ts_C);
        rem -= dt;
      }
      t_sim += dtReal;
    }

    // ── Fond ──────────────────────────────────────────────────
    p.background(11, 15, 20);

    // ── En-tête ───────────────────────────────────────────────
    p.textFont('Arial');
    p.textAlign(p.LEFT, p.TOP);
    p.textStyle(p.BOLD);
    p.textSize(9.5);
    p.fill(242, 219, 194);
    p.text('THERMAL PENETRATION  ·  RADIAL CROSS-SECTION', 16, 12);

    p.textStyle(p.NORMAL);
    p.textSize(9);
    p.fill(255, 255, 255, 85);
    p.text('4041 Cr-Mo pin  ·  Ø150 mm  ·  Target 400°F (204°C)  ·  Same torch energy input', 16, 27);

    // Timer — affiché dans l'en-tête, à droite
    const mins   = Math.floor(t_sim / 60);
    const secs   = Math.floor(t_sim % 60);
    const padded = secs < 10 ? '0' + secs : '' + secs;
    timerStr     = mins + 'm ' + padded + 's';
    p.textAlign(p.RIGHT, p.TOP);
    p.fill(242, 219, 194, 130);
    p.textSize(9);
    p.text('⏱ ' + timerStr, W - 14, 12);

    // ── Séparateur central ────────────────────────────────────
    p.stroke(255, 255, 255, 13);
    p.strokeWeight(1);
    p.line(W / 2, 42, W / 2, lcy + R_PX + 14);
    p.noStroke();

    // ── Labels de colonne ─────────────────────────────────────
    p.textAlign(p.CENTER, p.TOP);

    // Rush
    p.textStyle(p.BOLD);
    p.textSize(10.5);
    p.fill(200, 82, 82);
    p.text('RUSH HEATING', lcx, 44);
    p.textStyle(p.NORMAL);
    p.textSize(8.5);
    p.fill(255, 255, 255, 72);
    p.text('Surface to 400°F in 90 sec', lcx, 59);

    // Correct
    p.textStyle(p.BOLD);
    p.textSize(10.5);
    p.fill(109, 185, 138);
    p.text('CORRECT HEATING', rcx, 44);
    p.textStyle(p.NORMAL);
    p.textSize(8.5);
    p.fill(255, 255, 255, 72);
    p.text('Slow soak to 400°F in 10 min', rcx, 59);

    // ── Pins ──────────────────────────────────────────────────
    drawPin(lcx, lcy, T_R);
    drawPin(rcx, lcy, T_C);

    // ── Annotations Surface / Core ────────────────────────────
    function annotate(cx, cy) {
      // Flèche "Surface"
      const sx = cx + R_PX + 8;
      const sy = cy - R_PX * 0.45;
      p.stroke(255, 255, 255, 28);
      p.strokeWeight(1);
      p.line(cx + R_PX + 1, cy - 6, sx, sy + 3);
      p.noStroke();
      p.fill(255, 255, 255, 52);
      p.textSize(8);
      p.textAlign(p.LEFT, p.CENTER);
      p.textStyle(p.NORMAL);
      p.text('Surface', sx, sy);

      // Label "Core" au centre
      p.fill(255, 255, 255, 42);
      p.textAlign(p.CENTER, p.CENTER);
      p.textSize(8);
      p.text('Core', cx, cy + 1);
    }
    annotate(lcx, lcy);
    annotate(rcx, lcy);

    // ── Readouts température ──────────────────────────────────
    drawReadout(lcx, T_R);
    drawReadout(rcx, T_C);

    // ── Échelle de couleur ────────────────────────────────────
    const barW  = Math.round(Math.min(280, W * 0.44));
    const barH  = 10;
    const barX  = (W - barW) / 2;
    const barY  = H - 68;

    p.noStroke();
    for (let i = 0; i < barW; i++) {
      const T_val = T_AMB + (i / barW) * (T_TARG - T_AMB);
      p.fill(tCol(T_val));
      p.rect(barX + i, barY, 1, barH);
    }
    p.noFill();
    p.stroke(255, 255, 255, 22);
    p.strokeWeight(1);
    p.rect(barX, barY, barW, barH);
    p.noStroke();

    // Étiquettes de l'échelle
    p.fill(255, 255, 255, 75);
    p.textSize(8);
    p.textStyle(p.NORMAL);
    p.textAlign(p.LEFT,   p.TOP);
    p.text('68°F',  barX,           barY + barH + 3);
    p.textAlign(p.CENTER, p.TOP);
    p.text('200°F', barX + barW / 2, barY + barH + 3);
    p.textAlign(p.RIGHT,  p.TOP);
    p.text('400°F', barX + barW,    barY + barH + 3);
    p.textAlign(p.CENTER, p.BOTTOM);
    p.fill(255, 255, 255, 40);
    p.textSize(7.5);
    p.text('Temperature scale', barX + barW / 2, barY - 2);

    // ── Boutons ───────────────────────────────────────────────
    btnPause.label = paused ? 'Play  ▶' : 'Pause ‖';
    drawBtn(btnReset);
    drawBtn(btnPause);
  };

  // ── Interaction ───────────────────────────────────────────────
  p.mousePressed = function() {
    if (hitBtn(btnReset)) resetSim();
    if (hitBtn(btnPause)) paused = !paused;
  };

}, 'viz-thermal');
</script>

For verification, I use heat crayons. You mark the steel at 75mm from the weld centerline, and when that mark goes wet and shiny, you're at temperature. It's direct, fast, and it doesn't lie. I have much less use for infrared thermometers on this kind of work. The readings depend on the emissivity of the surface, and mill-scale steel is inconsistent enough that you can easily be 30 or 40 degrees off without knowing it. The angle of the gun matters too. I've seen people get confident readings on an IR gun and then wonder why they had cracking. The heat crayon is old technology, but it's honest.

## After the last pass

Once the weld is done, the cool-down is just as important as the heat-up. What you're trying to avoid is rapid cooling that traps hydrogen in the hardened heat-affected zone and builds up enough stress to crack. My method in the shop is straightforward. I bury the pins in a large closed bin packed with dry sand and gravel. The thermal mass of the sand slows the cooling rate dramatically, and when I come in the next morning, the parts are still warm to the touch. That's what a proper slow cool looks like. It's low-tech, it costs nothing, and it works consistently.

<!-- ============================================================
     Visualisation : Courbe de refroidissement — deux phases
     Phase 1 : Refroidissement HAZ à l'air (800°C → 204°C)
     Phase 2 : Enfouissement dans le gravier (204°C → lendemain matin)
     Article : "Preheat on Hardened Steel — What the Mill Cert Tells You"
     Blog : wallid-guergour.com | Jekyll / GitHub Pages
     Dépendance : D3.js v7 via CDN Cloudflare

     Physique : loi de Newton T(t) = T_amb + (T0 − T_amb) · exp(−k · t)
     Phase 1 k_air    calibrée : HAZ retombe à 204°C en ~45 min (pièce massive préchauffée)
     Phase 2 k_gravel calibrée : encore tiède (~35°C) après 22h dans le gravier (mesure atelier)
     ============================================================ -->

<div id="viz-cooling" style="width:100%; max-width:720px; margin:32px auto;"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js"></script>
<script>
(function () {

  // ── Paramètres physiques ──────────────────────────────────────
  const T_HAZ    = 800;    // °C — température HAZ fin du dernier passage
  const T_BURIAL = 204;    // °C = 400°F — température d'enfouissement (= preheat maintenu)
  const T_AMB    = 20;     // °C — température ambiante atelier

  // Phase 1 : refroidissement à l'air jusqu'à T_BURIAL
  // Pour une pièce massive préchauffée à 204°C, la HAZ revient à 204°C en ~45 min
  const T_BURIAL_MIN = 360;        // minutes avant enfouissement
  const K_AIR  = -Math.log((T_BURIAL - T_AMB) / (T_HAZ - T_AMB)) / (T_BURIAL_MIN * 60);

  // Phase 2 : enfouissement dans le gravier
  // Calibré sur mesure atelier : encore tiède (~35°C) après 22h
  const T_NEXT_MORNING = 35;      // °C — mesure atelier lendemain matin
  const T_NEXT_MORNING_H = 22;    // heures après enfouissement
  const K_GRAVEL = -Math.log((T_NEXT_MORNING - T_AMB) / (T_BURIAL - T_AMB))
                   / (T_NEXT_MORNING_H * 3600);

  // Seuils métallurgiques 4041 Cr-Mo
  const MS = 350;   // °C — Martensite Start
  const MF = 180;   // °C — Martensite Finish (approx)

  // ── Génération de la courbe combinée ─────────────────────────
  // t_global en minutes, T en °C
  const T_BURIAL_S = T_BURIAL_MIN * 60;  // secondes
  const T_TOTAL_H  = T_BURIAL_MIN / 60 + T_NEXT_MORNING_H + 2; // heures totales
  const STEP_S     = 60; // 1 point par minute

  const data = [];
  const T_TOTAL_S = T_TOTAL_H * 3600;

  for (let t = 0; t <= T_TOTAL_S; t += STEP_S) {
    let T;
    if (t <= T_BURIAL_S) {
      // Phase 1 : air
      T = T_AMB + (T_HAZ - T_AMB) * Math.exp(-K_AIR * t);
    } else {
      // Phase 2 : gravier (repart de T_BURIAL à t=T_BURIAL_S)
      const dt = t - T_BURIAL_S;
      T = T_AMB + (T_BURIAL - T_AMB) * Math.exp(-K_GRAVEL * dt);
    }
    data.push({ tH: t / 3600, T }); // tH en heures pour l'axe X
  }

  // Heure à laquelle la courbe traverse un seuil
  function timeAtTemp(Ttarget) {
    for (let i = 0; i < data.length - 1; i++) {
      if (data[i].T >= Ttarget && data[i + 1].T < Ttarget) {
        const frac = (data[i].T - Ttarget) / (data[i].T - data[i + 1].T);
        return data[i].tH + frac * (STEP_S / 3600);
      }
    }
    return null;
  }

  // ── Charte graphique ──────────────────────────────────────────
  const C = {
    bg:         '#0B0F14',
    bgCard:     '#111820',
    accent:     '#F2DBC2',
    white:      '#FFFFFF',
    textSub:    'rgba(255,255,255,0.52)',
    border:     'rgba(255,255,255,0.08)',
    grid:       'rgba(255,255,255,0.06)',
    gravel:     '#e8b84b',
    air:        '#d45f5f',
    martensite: 'rgba(210,80,80,0.12)',
    msLine:     'rgba(210,80,80,0.55)',
    mfLine:     'rgba(210,80,80,0.32)',
    phase1Bg:   'rgba(212,95,95,0.05)',
    phase2Bg:   'rgba(232,184,75,0.04)',
    burial:     'rgba(242,219,194,0.18)',
  };

  // ── Layout ────────────────────────────────────────────────────
  const container = document.getElementById('viz-cooling');
  const totalW    = Math.min(container.offsetWidth || 720, 720);
  const margin    = { top: 58, right: 24, bottom: 56, left: 56 };
  const innerW    = totalW - margin.left - margin.right;
  const innerH    = 290;
  const totalH    = innerH + margin.top + margin.bottom;

  container.style.cssText = `
    background: ${C.bgCard};
    border: 1px solid ${C.border};
    border-radius: 4px;
    overflow: hidden;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
  `;

  const svg = d3.select('#viz-cooling')
    .append('svg')
    .attr('width', '100%')
    .attr('viewBox', `0 0 ${totalW} ${totalH}`)
    .attr('preserveAspectRatio', 'xMidYMid meet');

  // En-tête
  svg.append('text')
    .attr('x', 16).attr('y', 18)
    .attr('fill', C.accent)
    .attr('font-size', 10).attr('font-weight', '700')
    .attr('letter-spacing', '0.1em')
    .attr('font-family', 'Arial, sans-serif')
    .text('COOLING PROFILE  ·  HAZ END OF LAST PASS → NEXT MORNING IN GRAVEL');

  svg.append('text')
    .attr('x', 16).attr('y', 34)
    .attr('fill', C.textSub)
    .attr('font-size', 9).attr('font-family', 'Arial, sans-serif')
    .text('4041 Cr-Mo  ·  Preheated to 400°F  ·  Phase 2 calibrated: ~35°C after 22h in gravel (shop measurement)');

  const g = svg.append('g')
    .attr('transform', `translate(${margin.left},${margin.top})`);

  // ── Échelles ──────────────────────────────────────────────────
  const xScale = d3.scaleLinear()
    .domain([0, T_TOTAL_H])
    .range([0, innerW]);

  const yScale = d3.scaleLinear()
    .domain([T_AMB, T_HAZ + 30])
    .range([innerH, 0]);

  const xBurial = xScale(T_BURIAL_MIN / 60); // position X du point d'enfouissement

  // ── Fonds de phase ────────────────────────────────────────────
  // Phase 1 : fond rouge très léger
  g.append('rect')
    .attr('x', 0).attr('width', xBurial)
    .attr('y', 0).attr('height', innerH)
    .attr('fill', C.phase1Bg);

  // Phase 2 : fond ambre très léger
  g.append('rect')
    .attr('x', xBurial).attr('width', innerW - xBurial)
    .attr('y', 0).attr('height', innerH)
    .attr('fill', C.phase2Bg);

  // ── Grille ────────────────────────────────────────────────────
  [100, 200, 300, 400, 500, 600, 700].forEach(tick => {
    g.append('line')
      .attr('x1', 0).attr('x2', innerW)
      .attr('y1', yScale(tick)).attr('y2', yScale(tick))
      .attr('stroke', C.grid).attr('stroke-width', 1);
  });

  const xTicksH = [1, 2, 4, 6, 8, 10, 14, 18, 22];
  xTicksH.forEach(h => {
    g.append('line')
      .attr('x1', xScale(h)).attr('x2', xScale(h))
      .attr('y1', 0).attr('y2', innerH)
      .attr('stroke', C.grid).attr('stroke-width', 1);
  });

  // ── Zone martensite ───────────────────────────────────────────
  g.append('rect')
    .attr('x', 0).attr('width', innerW)
    .attr('y', yScale(MS))
    .attr('height', yScale(MF) - yScale(MS))
    .attr('fill', C.martensite);

  // Lignes Ms / Mf
  g.append('line')
    .attr('x1', 0).attr('x2', innerW)
    .attr('y1', yScale(MS)).attr('y2', yScale(MS))
    .attr('stroke', C.msLine).attr('stroke-width', 1)
    .attr('stroke-dasharray', '5,4');

  g.append('line')
    .attr('x1', 0).attr('x2', innerW)
    .attr('y1', yScale(MF)).attr('y2', yScale(MF))
    .attr('stroke', C.mfLine).attr('stroke-width', 1)
    .attr('stroke-dasharray', '4,5');

  // Labels Ms / Mf
  g.append('text')
    .attr('x', innerW - 4).attr('y', yScale(MS) - 4)
    .attr('text-anchor', 'end')
    .attr('fill', C.msLine).attr('font-size', 8.5)
    .attr('font-family', 'Arial, sans-serif')
    .text('Ms ≈ 350°C — Martensite Start');

  g.append('text')
    .attr('x', innerW - 4).attr('y', yScale(MF) - 4)
    .attr('text-anchor', 'end')
    .attr('fill', C.mfLine).attr('font-size', 8.5)
    .attr('font-family', 'Arial, sans-serif')
    .text('Mf ≈ 180°C — Martensite Finish');

  g.append('text')
    .attr('x', 5).attr('y', yScale((MS + MF) / 2) + 4)
    .attr('fill', 'rgba(220,80,80,0.45)')
    .attr('font-size', 7.5).attr('font-style', 'italic')
    .attr('font-family', 'Arial, sans-serif')
    .text('Martensitic transformation window');

  // ── Ligne de transition d'enfouissement ──────────────────────
  g.append('line')
    .attr('x1', xBurial).attr('x2', xBurial)
    .attr('y1', 0).attr('y2', innerH)
    .attr('stroke', C.burial).attr('stroke-width', 1.5)
    .attr('stroke-dasharray', '4,3');

  // Label enfouissement
  g.append('text')
    .attr('x', xBurial + 5).attr('y', yScale(T_BURIAL) - 10)
    .attr('fill', C.accent).attr('font-size', 8.5)
    .attr('font-weight', '700').attr('font-family', 'Arial, sans-serif')
    .text('Buried in gravel');

  g.append('text')
    .attr('x', xBurial + 5).attr('y', yScale(T_BURIAL) + 2)
    .attr('fill', 'rgba(242,219,194,0.55)').attr('font-size', 8)
    .attr('font-family', 'Arial, sans-serif')
    .text('400°F / ' + T_BURIAL_MIN + ' min after last pass');

  // Point de transition
  g.append('circle')
    .attr('cx', xBurial).attr('cy', yScale(T_BURIAL))
    .attr('r', 5).attr('fill', C.accent).attr('opacity', 0.9);

  // Annotation "Next morning"
  const xNextMorning = xScale(T_BURIAL_MIN / 60 + T_NEXT_MORNING_H);
  g.append('line')
    .attr('x1', xNextMorning).attr('x2', xNextMorning)
    .attr('y1', 0).attr('y2', innerH)
    .attr('stroke', 'rgba(242,219,194,0.12)').attr('stroke-width', 1)
    .attr('stroke-dasharray', '3,4');
  g.append('text')
    .attr('x', xNextMorning - 4).attr('y', 10)
    .attr('text-anchor', 'end')
    .attr('fill', 'rgba(242,219,194,0.35)').attr('font-size', 7.5)
    .attr('font-family', 'Arial, sans-serif')
    .text('Next morning (' + T_NEXT_MORNING_H + 'h after burial)');

  // Point "lendemain matin" calibration
  g.append('circle')
    .attr('cx', xNextMorning).attr('cy', yScale(T_NEXT_MORNING))
    .attr('r', 4).attr('fill', C.gravel).attr('opacity', 0.7);
  g.append('text')
    .attr('x', xNextMorning - 6).attr('y', yScale(T_NEXT_MORNING) - 8)
    .attr('text-anchor', 'end')
    .attr('fill', 'rgba(232,184,75,0.65)').attr('font-size', 7.5)
    .attr('font-family', 'Arial, sans-serif')
    .text('~35°C — shop measurement');

  // ── Annotation traversée de la fenêtre Ms ────────────────────
  const t_ms = timeAtTemp(MS);
  if (t_ms) {
    const x = xScale(t_ms);
    g.append('line')
      .attr('x1', x).attr('x2', x)
      .attr('y1', 0).attr('y2', yScale(MS))
      .attr('stroke', C.msLine).attr('stroke-width', 1)
      .attr('stroke-dasharray', '3,3').attr('opacity', 0.6);
    g.append('circle')
      .attr('cx', x).attr('cy', yScale(MS))
      .attr('r', 4).attr('fill', C.air).attr('opacity', 0.9);

    const tLabel = t_ms < 1
      ? Math.round(t_ms * 60) + ' min'
      : Math.floor(t_ms) + 'h ' + Math.round((t_ms % 1) * 60) + 'm';
    g.append('text')
      .attr('x', x + 5).attr('y', yScale(MS) - 8)
      .attr('fill', C.msLine).attr('font-size', 8)
      .attr('font-weight', '700').attr('font-family', 'Arial, sans-serif')
      .text('Enters Ms at ' + tLabel);
  }

  // ── Labels de phase ───────────────────────────────────────────
  g.append('text')
    .attr('x', xBurial / 2).attr('y', 14)
    .attr('text-anchor', 'middle')
    .attr('fill', 'rgba(212,95,95,0.6)').attr('font-size', 8.5)
    .attr('font-weight', '700').attr('font-family', 'Arial, sans-serif')
    .attr('letter-spacing', '0.06em')
    .text('PHASE 1 — AIR');

  g.append('text')
    .attr('x', xBurial + (innerW - xBurial) / 2).attr('y', 14)
    .attr('text-anchor', 'middle')
    .attr('fill', 'rgba(232,184,75,0.6)').attr('font-size', 8.5)
    .attr('font-weight', '700').attr('font-family', 'Arial, sans-serif')
    .attr('letter-spacing', '0.06em')
    .text('PHASE 2 — GRAVEL BURIAL');

  // ── Courbe principale ─────────────────────────────────────────
  // Segment Phase 1 (air) — rouge
  const dataP1 = data.filter(d => d.tH <= T_BURIAL_MIN / 60 + 0.01);
  const dataP2 = data.filter(d => d.tH >= T_BURIAL_MIN / 60 - 0.01);

  const line = d3.line()
    .x(d => xScale(d.tH))
    .y(d => yScale(d.T))
    .curve(d3.curveCatmullRom.alpha(0.5));

  g.append('path')
    .datum(dataP1)
    .attr('fill', 'none')
    .attr('stroke', C.air)
    .attr('stroke-width', 2.5)
    .attr('d', line);

  g.append('path')
    .datum(dataP2)
    .attr('fill', 'none')
    .attr('stroke', C.gravel)
    .attr('stroke-width', 2.5)
    .attr('d', line);

  // ── Axes ──────────────────────────────────────────────────────
  const xAxis = d3.axisBottom(xScale)
    .tickValues([0, 0.25, 0.5, 0.75, 1, 2, 4, 6, 8, 10, 14, 18, 22])
    .tickFormat(d => {
      if (d === 0)    return '0';
      if (d < 1)      return Math.round(d * 60) + 'm';
      return d + 'h';
    })
    .tickSize(4);

  const xG = g.append('g')
    .attr('transform', `translate(0,${innerH})`)
    .call(xAxis);
  xG.select('.domain').attr('stroke', C.border);
  xG.selectAll('text')
    .attr('fill', C.textSub).attr('font-size', 8).attr('font-family', 'Arial, sans-serif');
  xG.selectAll('.tick line').attr('stroke', C.border);

  g.append('text')
    .attr('x', innerW / 2).attr('y', innerH + 44)
    .attr('text-anchor', 'middle')
    .attr('fill', C.textSub).attr('font-size', 9)
    .attr('font-family', 'Arial, sans-serif')
    .text('Time after last weld pass');

  const yAxis = d3.axisLeft(yScale)
    .tickValues([20, 100, 180, 204, 350, 400, 500, 600, 700, 800])
    .tickFormat(d => d + '°C')
    .tickSize(4);

  const yG = g.append('g').call(yAxis);
  yG.select('.domain').attr('stroke', C.border);
  yG.selectAll('text')
    .attr('fill', C.textSub).attr('font-size', 8).attr('font-family', 'Arial, sans-serif');
  yG.selectAll('.tick line').attr('stroke', C.border);

  g.append('text')
    .attr('transform', 'rotate(-90)')
    .attr('x', -innerH / 2).attr('y', -44)
    .attr('text-anchor', 'middle')
    .attr('fill', C.textSub).attr('font-size', 9)
    .attr('font-family', 'Arial, sans-serif')
    .text('Temperature (°C)');

  // ── Légende ───────────────────────────────────────────────────
  const legEntries = [
    { color: C.air,    label: 'Phase 1 — Air cool (HAZ → 400°F)' },
    { color: C.gravel, label: 'Phase 2 — Gravel burial (calibrated)'  },
  ];

  const legX = innerW - 272, legY = 22;
  g.append('rect')
    .attr('x', legX - 8).attr('y', legY - 8)
    .attr('width', 280).attr('height', legEntries.length * 20 + 14)
    .attr('fill', 'rgba(11,15,20,0.75)')
    .attr('stroke', C.border).attr('stroke-width', 1).attr('rx', 3);

  legEntries.forEach((d, i) => {
    const ly = legY + i * 20 + 4;
    g.append('line')
      .attr('x1', legX).attr('x2', legX + 22)
      .attr('y1', ly + 5).attr('y2', ly + 5)
      .attr('stroke', d.color).attr('stroke-width', 2.5);
    g.append('text')
      .attr('x', legX + 28).attr('y', ly + 9)
      .attr('fill', C.white).attr('font-size', 9)
      .attr('font-family', 'Arial, sans-serif')
      .text(d.label);
  });

  // ── Tooltip ───────────────────────────────────────────────────
  const tooltip  = svg.append('g').attr('opacity', 0);
  const ttBg     = tooltip.append('rect').attr('rx', 3)
    .attr('fill', 'rgba(11,15,20,0.92)').attr('stroke', C.border).attr('stroke-width', 1);
  const ttTime   = tooltip.append('text').attr('fill', C.accent)
    .attr('font-size', 9).attr('font-weight', '700').attr('font-family', 'Arial, sans-serif');
  const ttTemp   = tooltip.append('text').attr('fill', C.white)
    .attr('font-size', 9).attr('font-family', 'Arial, sans-serif');
  const ttPhase  = tooltip.append('text').attr('fill', C.textSub)
    .attr('font-size', 8).attr('font-family', 'Arial, sans-serif');

  const cursorLine = g.append('line').attr('y1', 0).attr('y2', innerH)
    .attr('stroke', 'rgba(255,255,255,0.18)').attr('stroke-width', 1).attr('opacity', 0);
  const dot = g.append('circle').attr('r', 4).attr('opacity', 0);

  svg.on('mousemove', function(event) {
    const [mx, my] = d3.pointer(event);
    const xInner = mx - margin.left;
    if (xInner < 0 || xInner > innerW) {
      tooltip.attr('opacity', 0);
      cursorLine.attr('opacity', 0);
      dot.attr('opacity', 0);
      return;
    }

    const tH = xScale.invert(xInner);
    const tS = tH * 3600;
    const tBurial_S = T_BURIAL_MIN * 60;
    let T_val, phase, col;

    if (tS <= tBurial_S) {
      T_val = T_AMB + (T_HAZ - T_AMB) * Math.exp(-K_AIR * tS);
      phase = 'Phase 1 — Air';
      col   = C.air;
    } else {
      const dt = tS - tBurial_S;
      T_val = T_AMB + (T_BURIAL - T_AMB) * Math.exp(-K_GRAVEL * dt);
      phase = 'Phase 2 — Gravel';
      col   = C.gravel;
    }

    const cToF = c => Math.round(c * 9 / 5 + 32);
    const tLabel = tH < 1
      ? Math.round(tH * 60) + ' min'
      : Math.floor(tH) + 'h ' + Math.round((tH % 1) * 60).toString().padStart(2, '0') + 'm';

    cursorLine.attr('x1', xInner).attr('x2', xInner).attr('opacity', 1);
    dot.attr('cx', xInner).attr('cy', yScale(T_val))
      .attr('fill', col).attr('opacity', 0.9);

    const ttW = 170, ttH = 56;
    let ttX = mx + 12, ttY = my - 36;
    if (ttX + ttW > totalW - 6) ttX = mx - ttW - 12;
    if (ttY < 4)                 ttY = 4;
    if (ttY + ttH > totalH - 4) ttY = totalH - ttH - 4;

    ttBg.attr('x', ttX).attr('y', ttY).attr('width', ttW).attr('height', ttH);
    ttTime.attr('x', ttX + 9).attr('y', ttY + 14).text('⏱  ' + tLabel);
    ttTemp.attr('x', ttX + 9).attr('y', ttY + 30)
      .text(Math.round(T_val) + '°C  (' + cToF(T_val) + '°F)');
    ttPhase.attr('x', ttX + 9).attr('y', ttY + 44).text(phase);

    tooltip.attr('opacity', 1);
  });

  svg.on('mouseleave', function() {
    tooltip.attr('opacity', 0);
    cursorLine.attr('opacity', 0);
    dot.attr('opacity', 0);
  });

})();
</script>

## When someone grabs the wrong wire

I was working on a hardfacing job, rechargement on a large plate. I had specified the wire: Lincoln Electric Metalshield MC-110, classified E110C-K4 H4, rated at 110 ksi tensile strength (760 MPa). It's a low-alloy metal-cored wire with good low-temperature impact properties and a low hydrogen classification, which is exactly what you need on high-strength base metal.

A helper who was setting up while I was on another part of the job grabbed a different wire off the shelf. A standard structural wire, something in the 70 ksi range, the kind you'd use on mild steel. Not classified for this application, and he started welding without verifying preheat either.

The deposit was softer and weaker than specified. The mismatch between the deposit and the hardened base metal created stress concentrations at the fusion line, and the missing preheat meant the HAZ cooled too fast. When I came back and looked at the plate under a good light, the cracks were there. Fine and tight, the kind you can miss in bad lighting, but clearly visible once you slow down and look properly. The plate had also come in wrong by about 3/16 of an inch, so it already needed rework. The cracking made it significantly worse and delayed the delivery.

Both problems came from the same place: assumptions made without checking. The mill cert was there. The WPS was there. The right wire was in the shop. None of it was consulted before starting. That's where most welding failures actually begin, not in the arc itself but in the few minutes before it.

Chrome-moly steels are not forgiving of improvisation. They reward the person who does the calculation, pulls the cert, and checks the temperature before every pass. That's not excessive caution. It's just how the metallurgy works, and the cracks will always tell you when you ignored it.
