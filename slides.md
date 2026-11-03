---
theme: ./slidev-theme-aalto-scicomp
themeConfig:
  palette: aalto-classic
  titles: aalto
  credit:
    text: Enrico Glerean · CC BY 4.0
    url: https://eglerean.github.io/
  download:
    url: /Glerean_2026_OpenClosed.pdf
    text: Download PDF
favicon: https://eglerean.github.io/favicon.svg
title: As open as possible, as closed as necessary
author: Enrico Glerean
info: |
  Slides by Enrico Glerean (https://eglerean.github.io/), CC BY 4.0.
  Research integrity, AI, privacy and cybersecurity through an open science lens.
  Source: https://github.com/eglerean/ajar
keywords: open science, research integrity, privacy, GDPR, cybersecurity, AI, Enrico Glerean, https://eglerean.github.io/
layout: cover
class: no-footer
hexText: "OPEN\nCLOSED"
hexSeed: 11
---

###### Open science · Research integrity

# As open as possible, as closed as necessary

Research integrity, AI, privacy and cybersecurity through an open science lens

::presenter::
**Enrico Glerean**, Staff Scientist, Aalto University, November 2026

<div class="license-line"><CcBy /> <a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a> · <a href="https://github.com/eglerean/ajar" class="gh-link" title="Slides on GitHub" aria-label="Slides on GitHub"><carbon-logo-github class="gh-icon" /></a></div>

<style>
h1 { font-size: 2.5rem !important; line-height: 1.1 !important; }
p { font-size: 0.95rem; }
.cover-presenter p { font-size: 0.85rem; }
.license-line { margin-top: 0.45rem; font-size: 0.75rem; white-space: nowrap; }
.gh-icon { vertical-align: -0.2em; width: 1.15em; height: 1.15em; }
.license-line a.gh-link { border-bottom: none; text-decoration: none; color: inherit; }
</style>

<!--
Thesis: "open" and "closed" are decisions per research object. Integrity decides what must stay checkable, privacy decides who could be harmed, cybersecurity decides whether "closed" holds, and AI moves all three lines.

Status date: legal and factual claims checked on 4 November 2026.
-->

---
layout: default
---

###### Part A · The principle

# Three ways to fail the same principle

<div class="grid-3">
  <div class="card">
    <svg class="door" viewBox="0 0 120 90" aria-label="A locked door, nobody holding the key">
      <rect x="35" y="8" width="50" height="78" rx="3" class="door-frame" />
      <rect x="40" y="13" width="40" height="73" class="door-leaf" />
      <rect x="66" y="44" width="12" height="10" rx="2" class="door-lock" />
      <path d="M68.5 44 v-4 a3.5 3.5 0 0 1 7 0 v4" class="door-shackle" />
    </svg>
    <h3>Closed by habit</h3>
    <p class="small">"Available on request": 1,792 authors asked, 123 shared data (6.8%). <span class="badge audit">Audit</span></p>
  </div>
  <div class="card">
    <svg class="door" viewBox="0 0 120 90" aria-label="A wide open door, nobody watching">
      <rect x="35" y="8" width="50" height="78" rx="3" class="door-frame" />
      <rect x="40" y="13" width="40" height="73" class="door-gap" />
      <polygon points="40,13 18,4 18,95 40,86" class="door-leaf" />
    </svg>
    <h3>Open by accident</h3>
    <p class="small">UK Biobank data in public code repositories, first detected in 2022; 80 takedown notices to GitHub in July–December 2025. UK Biobank's explanation: researchers published code, which journals often require. <span class="badge incident">Incident</span></p>
  </div>
  <div class="card">
    <svg class="door" viewBox="0 0 120 90" aria-label="A door with a do-not-enter sign and no lock">
      <rect x="35" y="8" width="50" height="78" rx="3" class="door-frame" />
      <rect x="40" y="13" width="40" height="73" class="door-leaf" />
      <circle cx="60" cy="36" r="11" class="door-sign" />
      <rect x="53" y="34" width="14" height="4" class="door-sign-bar" />
      <circle cx="74" cy="52" r="2.2" class="door-knob" />
    </svg>
    <h3>Closed on paper</h3>
    <p class="small">April 2026: data on about 500,000 participants listed for sale. No hack: breaches of access policy by approved institutions. <span class="badge incident">Incident</span></p>
  </div>
</div>

<div class="card dark">
Each failure has a different owner: <strong>integrity</strong>, <strong>privacy</strong>, <strong>security</strong>. Neither more openness nor more closure fixes all three.
</div>

<div class="ref-bottom"><a href="https://pubmed.ncbi.nlm.nih.gov/35654271">Gabelica 2022</a> · <a href="https://www.ukbiobank.ac.uk/?p=63092">UK Biobank statement 2026</a> · <a href="https://www.freevacy.com/news/the-guardian/confidential-uk-biobank-health-records-exposed-online/7214">Guardian via Freevacy 2026</a> · <a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UKB Oversight Committee 2026</a> · <a href="https://www.theregister.com/2026/04/23/500k_biobank_volunteers_data_listed/">The Register 2026</a></div>

<style>
.door { display: block; width: 110px; height: 82px; margin: 0 auto 0.4rem; }
.door-frame { fill: none; stroke: var(--asc-text); stroke-width: 2.5; }
.door-leaf { fill: var(--asc-sunken); stroke: var(--asc-text); stroke-width: 1.5; }
.door-gap { fill: var(--asc-night); }
.door-lock { fill: var(--aalto-darkyellow); stroke: var(--asc-text); stroke-width: 1.2; }
.door-shackle { fill: none; stroke: var(--asc-text); stroke-width: 1.8; }
.door-sign { fill: var(--aalto-red); }
.door-sign-bar { fill: #fff; }
.door-knob { fill: var(--asc-text); }
.card h3 { text-align: center; }
</style>

---
layout: default
---

###### Part A · The principle

# "Closed" needs a reason

<div class="grid-3-2">
  <div class="cascade">
    <div class="cs-step" style="--i: 0"><b>Ethics</b><span class="small">ALLEA 2023 §2.5: access "as open as possible, as closed as necessary", with transparent routes to access. §3.1: withholding data or results without justification is a <strong>violation</strong>.</span></div>
    <div class="cs-step" style="--i: 1"><b>EU law</b><span class="small">Open Data Directive Art 10: publicly funded research data "open by default". Horizon Europe: the DMP must explain any restriction.</span></div>
    <div class="cs-step" style="--i: 2"><b>Finland / Aalto</b><span class="small">National policy 2026–2030: same principle; where limits are justified, describe the resources as transparently as possible.</span></div>
    <div class="cs-step" style="--i: 3"><b>Researcher</b><span class="small">Every closure needs an object, a reason and an access route.</span></div>
  </div>
  <div class="stack">
    <div class="card">
      <h3>Valid reasons to close (ODD Art 10)</h3>
      <div class="chips">
        <span>personal data</span><span>confidentiality</span><span>IPR</span><span>security and dual use</span><span>legitimate commercial interests</span>
      </div>
    </div>
    <div class="card dark">
      <h3>Every closure: object · reason · access route</h3>
      <p>"On reasonable request" has none of the three.</p>
    </div>
  </div>
</div>

<div class="ref-bottom"><a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://eur-lex.europa.eu/eli/dir/2019/1024/oj">Open Data Directive</a> · <a href="https://rea.ec.europa.eu/open-science_en">Horizon Europe</a> · <a href="https://tsv.fi/fi/palvelut/linjauslouhi/index.php/Aineistot/en">FI policy 2026–2030</a> · <a href="https://eur-lex.europa.eu/eli/C/2024/3510/oj/eng/pdf">Council Rec. 2024 (research security)</a> · cascade from the <a href="https://scicomp.aalto.fi/scicomp/rcr-scicomp/">RCR page</a></div>

<style>
.cascade { display: flex; flex-direction: column; gap: 0.4rem; }
.cs-step { margin-left: calc(var(--i) * 1.6rem); padding: 0.3rem 0.7rem; border-left: 5px solid var(--aalto-blue); border-radius: var(--asc-radius-sm); background: var(--asc-surface); line-height: 1.2; }
.cs-step b { display: block; font-family: var(--asc-font-serif); }
.cs-step:last-child { border-left-color: var(--aalto-red); }
.chips { display: flex; flex-wrap: wrap; gap: 0.4rem; }
.chips span { padding: 0.15rem 0.7rem; border-radius: 999px; background: var(--aalto-yellow); color: #000; font-size: 0.85rem; }
</style>

<!--
"So every closure needs an object, a reason and an access route" is the take-away. Ask the room who has written "available on reasonable request".
-->

---
layout: default
---

###### Part A · The principle

# Four domains, six intersections, one question

<div class="grid-4 dq">
  <div class="card"><b>Research integrity</b><br>Can others check it and trust it?</div>
  <div class="card"><b>Privacy</b><br>Who could be harmed, and how?</div>
  <div class="card"><b>Cybersecurity</b><br>What can get in, get out or be altered?</div>
  <div class="card"><b>AI</b><br>What changes with a model in the loop?</div>
</div>

<DomainGrid full />

<div class="card dark os-note">
Open science is not a fifth domain. It is the question asked in every cell: <strong>what can be open here?</strong>
</div>

<style>
.dq { margin-bottom: 0.5rem; }
.dq .card { padding: 0.35rem 0.7rem; font-size: 0.78rem; line-height: 1.15; }
.dq b { font-family: var(--asc-font-serif); font-size: 0.95rem; }
.os-note { margin-top: 0.5rem; padding: 0.4rem 0.9rem; font-size: 0.9rem; }
</style>

<!--
This grid is also the agenda: each cell links to the slide where it comes up. The small grid in the top-right corner of later slides shows which cell we are in.
-->

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="int-cyb" /></div>

###### Part A · The principle

# One triad, three communities

<div class="grid-2-3">
<div>
<svg class="cia" viewBox="-40 0 440 290" role="img" aria-label="Triangle: Integrity at the top is fixed; the edge between Confidentiality and Availability is a slider of access tiers">
  <polygon points="180,40 40,230 320,230" class="cia-tri" />
  <!-- slider on the C–A edge -->
  <line x1="40" y1="230" x2="320" y2="230" class="cia-slider" />
  <g class="cia-ticks">
    <circle cx="40" cy="230" r="5" /><circle cx="110" cy="230" r="5" /><circle cx="180" cy="230" r="5" /><circle cx="250" cy="230" r="5" /><circle cx="320" cy="230" r="5" />
  </g>
  <circle cx="180" cy="230" r="11" class="cia-knob" />
  <text x="40" y="252" class="cia-tier">Not shared</text>
  <text x="110" y="268" class="cia-tier">Secure env.</text>
  <text x="180" y="252" class="cia-tier">Controlled</text>
  <text x="250" y="268" class="cia-tier">Registered</text>
  <text x="320" y="252" class="cia-tier">Public</text>
  <!-- vertices -->
  <circle cx="180" cy="40" r="20" class="cia-v cia-fixed" />
  <text x="180" y="41" class="cia-letter">I</text>
  <text x="180" y="10" class="cia-comm">research integrity · fixed</text>
  <circle cx="40" cy="200" r="20" class="cia-v" />
  <text x="40" y="201" class="cia-letter">C</text>
  <text x="40" y="168" class="cia-comm">privacy · security</text>
  <circle cx="320" cy="200" r="20" class="cia-v" />
  <text x="320" y="201" class="cia-letter">A</text>
  <text x="320" y="168" class="cia-comm">open science</text>
</svg>
</div>
<div>

- **Confidentiality:** participants, privacy, research security.
- **Integrity:** data, code and models unaltered and traceable. A precondition for research integrity, not the same thing.
- **Availability:** open science. Outputs that exist, can be found and can still be reached years later.
- GDPR already uses these terms: Art 5(1)(f) and Art 32(1)(b).

<div class="card dark">Access decisions trade C against A. <strong>I is the one you do not trade.</strong></div>

</div>
</div>

<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> Art 5(1)(f), 32(1)(b) · <a href="https://coderefinery.github.io/coding-with-ai/security/">CodeRefinery, Coding with AI: Security</a></div>

<style>
.cia { width: 100%; max-width: 380px; }
.cia-tri { fill: color-mix(in srgb, var(--aalto-blue) 12%, transparent); stroke: var(--asc-border); stroke-width: 2; }
.cia-slider { stroke: var(--aalto-blue); stroke-width: 6; stroke-linecap: round; }
.cia-ticks circle { fill: var(--asc-bg); stroke: var(--aalto-blue); stroke-width: 2; }
.cia-knob { fill: var(--aalto-yellow); stroke: var(--asc-text); stroke-width: 2; }
.cia-tier { font-size: 11px; text-anchor: middle; fill: var(--asc-muted); }
.cia-v { fill: var(--asc-night); }
.cia-fixed { fill: var(--aalto-red); }
.cia-letter { font-family: var(--asc-font-serif); font-weight: 700; font-size: 20px; text-anchor: middle; dominant-baseline: middle; fill: #fff; }
.cia-comm { font-size: 12px; font-weight: 600; text-anchor: middle; fill: var(--asc-text); }
</style>

---
layout: default
---

###### Part B · As open as possible

# A study is a bundle of objects, each with its own access level

<div class="grid-2-3">
<div>

- Transparency of **claims**, of **methods** and of **data** are three separate decisions.
- **Open by default:** question, protocol, data dictionary, code, container recipe, aggregate results (check small cells).
- **Gated by default:** participant-level data, linkage keys.
- **New rows:** prompts, logs, model weights, synthetic data (slides 14, 16).

<div class="running-case"><strong>Running case</strong> 80 interviews on workplace harassment (fictional). Filled in on the right.</div>

</div>
<div>
<table class="bp-matrix compact access-map">
  <thead>
    <tr><th>Object</th><th>Public</th><th>Registered users</th><th>Controlled access</th><th>Secure env. only</th><th>Not shared</th></tr>
  </thead>
  <tbody>
    <tr><td>Research question, protocol</td><td class="bp-green">●</td><td></td><td></td><td></td><td></td></tr>
    <tr><td>Data dictionary, interview guide</td><td class="bp-green">●</td><td></td><td></td><td></td><td></td></tr>
    <tr><td>Analysis code, container recipe</td><td class="bp-green">●</td><td></td><td></td><td></td><td></td></tr>
    <tr><td>Aggregate results <em>check small cells</em></td><td class="bp-green">●</td><td></td><td></td><td></td><td></td></tr>
    <tr><td>Sanitised AI workflow</td><td class="bp-green">●</td><td></td><td></td><td></td><td></td></tr>
    <tr><td>Synthetic excerpts for teaching</td><td></td><td class="bp-darkyellow">●</td><td></td><td></td><td></td></tr>
    <tr><td>Full prompt and session logs</td><td></td><td></td><td class="bp-orange">●</td><td></td><td></td></tr>
    <tr><td>Pseudonymised transcripts</td><td></td><td></td><td></td><td class="bp-red">●</td><td></td></tr>
    <tr><td>Audio, linkage key, consent forms</td><td></td><td></td><td></td><td></td><td class="bp-grey">●</td></tr>
  </tbody>
</table>
</div>
</div>

<div class="ref-bottom"><a href="https://doi.org/10.1016/j.xcrm.2025.102080">Lvovs 2025</a>, ethical data sharing and open science</div>

<style>
.access-map td:not(:first-child) { text-align: center; width: 13%; }
.access-map th { font-size: 0.65rem !important; text-align: center; }
.access-map em { display: inline !important; margin: 0 !important; font-size: 0.6rem; opacity: 0.75; }
</style>

<!--
The heatmap is a draft for the fictional case: revise the placements. The point is that one study has rows in every column.
-->

---
layout: default
---

###### Part B · As open as possible

# FAIR says how to reach data, not who gets it

<div class="grid-2-3">
<div class="fair-stack">
  <div class="fair-meta">
    <div class="fair-head"><b>Public metadata record</b><span class="fl">F</span><span class="fl">I</span><span class="fl">R</span><span class="fl">A2</span></div>
    <div class="small">DOI · title · description · variables · licence · <strong>access conditions</strong> · contact that outlives the project</div>
  </div>
  <div class="fair-door">
    <div class="fair-head"><b>The door</b><span class="fl">A1.2</span></div>
    <div class="small">Authentication and authorisation: data use agreement, ethics approval, named purpose</div>
  </div>
  <div class="fair-data">
    <div class="fair-head"><b>The dataset</b><span class="fl">A1</span></div>
    <div class="small">Retrievable by a standard protocol, once you are through the door</div>
  </div>
</div>
<div>

- FAIR **A1.2** allows authentication and authorisation where necessary. **A2** keeps metadata reachable after the data are gone.
- Behavioural datasets became more reusable while keeping access restrictions (two worked examples).
- FAIR is uneven. Feasibility varies with discipline, infrastructure and resources; 79.4% of data users report difficulty finding relevant data (n=643, LMIC focus). <span class="badge survey">Survey</span>
- Not every dataset earns the cost. **Appraise at the planning stage.**

</div>
</div>

<div class="ref-bottom"><a href="https://doi.org/10.1038/sdata.2016.18">Wilkinson 2016</a> · <a href="https://journals.sagepub.com/doi/10.1177/25152459251336130">van Ravenzwaaij 2025</a> · <a href="https://journals.sagepub.com/doi/10.1177/20539517251349157">Hellstrand 2025</a> · <a href="https://pubmed.ncbi.nlm.nih.gov/39565766/">Waithira 2024</a> · <a href="https://zenodo.org/records/18609058">Glerean 2026, Data Available on Unreasonable Request</a></div>

<style>
.fair-stack { display: flex; flex-direction: column; gap: 0; }
.fair-stack .fair-head { display: flex; align-items: center; gap: 0.3rem; margin-bottom: 0.2rem; }
.fair-stack .fair-head b { font-family: var(--asc-font-serif); margin-right: auto; }
.fl { display: inline-grid; place-items: center; min-width: 1.5rem; height: 1.5rem; padding: 0 0.25rem; border-radius: 999px; background: var(--aalto-blue); color: #000; font-weight: 700; font-size: 0.7rem; }
.fair-meta { padding: 0.6rem 0.8rem; border: 2px solid var(--aalto-blue); border-radius: var(--asc-radius-md) var(--asc-radius-md) 0 0; background: var(--asc-surface); }
.fair-door { padding: 0.6rem 0.8rem; background: var(--aalto-yellow); color: #000; border-left: 2px solid var(--aalto-yellow); border-right: 2px solid var(--aalto-yellow); }
.fair-data { padding: 0.6rem 0.8rem; background: var(--asc-night); color: var(--asc-paper); border-radius: 0 0 var(--asc-radius-md) var(--asc-radius-md); }
</style>

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="int-priv" /></div>

###### Part B · As open as possible

# Protecting participants protects validity

<div class="chain">
  <div class="flow">
    <div class="step weak"><b>Weak promise</b>"Anonymous", vague reuse, no named route</div>
    <div class="arrow">→</div>
    <div class="step weak"><b>Withheld or altered answers</b>plus non-response on sensitive items</div>
    <div class="arrow">→</div>
    <div class="step weak-end"><b>Biased estimate</b>and the loss is not random</div>
  </div>
  <div class="flow">
    <div class="step strong"><b>Credible promise</b>Who sees what, where, for how long</div>
    <div class="arrow">→</div>
    <div class="step strong"><b>Fuller answers</b>and fewer skipped measures</div>
    <div class="arrow">→</div>
    <div class="step strong-end"><b>Better estimate</b></div>
  </div>
  <div class="chain-label"><span class="schematic-label">Association, self-reported</span></div>
</div>

<div class="dense">

- 17,729 secondary school students: 46.0% had a privacy, confidentiality or data-use concern; 29.2% of those said it affected the accuracy of their answers. They skipped sensitive measures more often; gender-diverse adolescents reported more concerns. <span class="badge survey">Survey</span>
- Parkinson's patients favoured openness, but lower visit burden dominated their choices (randomised pilot, hypothetical trials).
- ALLEA §2.5: tell participants how data are used, reused, accessed, stored and deleted. Name the sharing route. **Do not promise "anonymous" for a small interview study.**
- Ethics consent is not GDPR consent. Consent as the legal basis keeps the link to the person, and non-random withdrawal biases the cohort.

</div>

<div class="ref-bottom"><a href="https://doi.org/10.1016/j.jadohealth.2025.03.004">Soneson 2025</a> · <a href="https://doi.org/10.1177/15562646251384573">Iskander 2025</a> · <a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://eglerean.github.io/posts/sciresgdpr">Glerean 2026, consent, anonymisation and open science</a></div>

<style>
.chain { display: flex; flex-direction: column; gap: 0.4rem; margin-bottom: 0.4rem; }
.chain .step.weak { border-color: var(--aalto-red); }
.chain .step.weak-end { background: var(--aalto-red); border-color: var(--aalto-red); color: #000; }
.chain .step.strong { border-color: var(--aalto-green); }
.chain .step.strong-end { background: var(--aalto-green); border-color: var(--aalto-green); color: #000; }
.chain-label { text-align: right; }
</style>

---
layout: default
---

###### Part C · As closed as necessary

# "Necessary" depends on who could identify whom, with what means

<div class="dense">

- **Four words, not synonyms:** de-identified (not a GDPR term), pseudonymised (Art 4(5)), anonymous (Recital 26), synthetic (a method, not a status).
- *EDPS v SRB* (C-413/23 P, 2025): identifiability depends on the means of the party concerned. The same data can be personal for one party and not for another. <span class="badge binding">Binding</span>
- EDPB draft Guidelines 02/2026: test record isolation, linkage and inference. Contracts supplement technical measures, they do not replace them. <span class="badge draft">Draft</span>
- Digital Omnibus: the Council mandate of 21 October 2026 keeps the Art 4(1) definition of personal data. <span class="badge proposal">Proposal</span>

</div>

<div class="grid-3 viewers">
  <div class="card dark"><div class="vw-who">Key holder</div><div class="vw-verdict">Personal data</div><div class="small">Holds the linkage key: pseudonymised data stay personal data.</div></div>
  <div class="card yellow"><div class="vw-who">Recipient without means</div><div class="vw-verdict">Assess</div><div class="small">No key, no realistic means: may not be personal data <em>for them</em>.</div></div>
  <div class="card red"><div class="vw-who">Public download</div><div class="vw-verdict">Assume anyone</div><div class="small">Any person, any tool, any auxiliary data, now and later.</div></div>
</div>

<div class="running-case"><strong>Running case</strong> The credible adversary is a colleague who recognises the story. Removing names does not stop that.</div>

<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> · <a href="https://www.fieldfisher.com/en-be/locations/belgium/insights/edps-v-srb-cjeu%e2%80%99s-contextual-approach-to-pseudonym">EDPS v SRB</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026 (draft)</a> · <a href="https://iapp.org/news/a/eu-member-states-finalize-digital-omnibus-negotiating-stance">Council mandate 2026</a></div>

<style>
.viewers { margin: 0.5rem 0; }
.viewers .card { padding: 0.55rem 0.8rem; }
.vw-who { font-size: 0.75rem; text-transform: uppercase; letter-spacing: 0.05em; opacity: 0.8; }
.vw-verdict { font-family: var(--asc-font-serif); font-weight: 700; font-size: 1.2rem; margin-bottom: 0.15rem; }
</style>

<!--
CHECK BEFORE PRESENTING
- Digital Omnibus is fast-moving: re-check the Council mandate and Parliament status.
- EDPB draft 02/2026 was read through summaries (Sidley, DLA Piper, GamingTechLaw): check against the primary text.
-->

---
layout: default
---

###### Part C · As closed as necessary

# Average risk hides the people at risk

- **70 clinical trial datasets** (31 open, 39 controlled): 7 labelled anonymised still held direct identifiers such as date of birth or initials. The scores measure structure; nobody was re-identified. <span class="badge audit">Audit</span>
- **"Anonymised" health data** kept measurable membership risk, depending on the privacy model and how records were changed. <span class="badge audit">Audit</span>
- **Medical AI, seven datasets:** aggregate attacks look close to chance, yet are near-perfect for some patients. Underrepresented groups face disproportionate success, and high-risk patients increase with model capacity. <span class="badge audit">Audit</span>

<div class="strip">
<svg viewBox="0 0 920 150" role="img" aria-label="Schematic strip plot of per-patient attack success: most points near chance, a long tail toward certain, and one subgroup shifted toward high risk. Schematic, not data.">
  <line x1="60" y1="115" x2="860" y2="115" class="sp-axis" />
  <line x1="460" y1="30" x2="460" y2="115" class="sp-chance" />
  <text x="460" y="135" class="sp-tick" text-anchor="middle">chance</text>
  <text x="60" y="135" class="sp-tick" text-anchor="start">attack always wrong</text>
  <text x="860" y="135" class="sp-tick" text-anchor="end">attack always right</text>
  <circle cx="461.1" cy="55.4" r="4" class="sp-dot" />
  <circle cx="473.0" cy="44.2" r="4" class="sp-dot" />
  <circle cx="447.1" cy="92.0" r="4" class="sp-dot" />
  <circle cx="469.9" cy="44.7" r="4" class="sp-dot" />
  <circle cx="485.9" cy="89.6" r="4" class="sp-dot" />
  <circle cx="471.5" cy="50.0" r="4" class="sp-dot" />
  <circle cx="503.7" cy="86.1" r="4" class="sp-dot" />
  <circle cx="435.2" cy="84.7" r="4" class="sp-dot" />
  <circle cx="461.9" cy="89.6" r="4" class="sp-dot" />
  <circle cx="440.3" cy="72.6" r="4" class="sp-dot" />
  <circle cx="438.1" cy="89.7" r="4" class="sp-dot" />
  <circle cx="454.9" cy="54.5" r="4" class="sp-dot" />
  <circle cx="466.2" cy="78.9" r="4" class="sp-dot" />
  <circle cx="471.7" cy="61.2" r="4" class="sp-dot" />
  <circle cx="474.2" cy="90.4" r="4" class="sp-dot" />
  <circle cx="522.5" cy="84.2" r="4" class="sp-dot" />
  <circle cx="484.2" cy="68.5" r="4" class="sp-dot" />
  <circle cx="415.4" cy="71.4" r="4" class="sp-dot" />
  <circle cx="465.7" cy="45.4" r="4" class="sp-dot" />
  <circle cx="442.6" cy="45.8" r="4" class="sp-dot" />
  <circle cx="445.6" cy="74.9" r="4" class="sp-dot" />
  <circle cx="496.6" cy="69.4" r="4" class="sp-dot" />
  <circle cx="453.8" cy="89.0" r="4" class="sp-dot" />
  <circle cx="405.4" cy="75.6" r="4" class="sp-dot" />
  <circle cx="468.7" cy="51.2" r="4" class="sp-dot" />
  <circle cx="451.8" cy="62.9" r="4" class="sp-dot" />
  <circle cx="427.1" cy="83.9" r="4" class="sp-dot" />
  <circle cx="434.2" cy="71.2" r="4" class="sp-dot" />
  <circle cx="442.5" cy="44.5" r="4" class="sp-dot" />
  <circle cx="459.3" cy="87.6" r="4" class="sp-dot" />
  <circle cx="448.1" cy="87.0" r="4" class="sp-dot" />
  <circle cx="462.0" cy="48.4" r="4" class="sp-dot" />
  <circle cx="511.4" cy="72.3" r="4" class="sp-dot" />
  <circle cx="437.6" cy="63.8" r="4" class="sp-dot" />
  <circle cx="437.4" cy="84.9" r="4" class="sp-dot" />
  <circle cx="453.0" cy="60.2" r="4" class="sp-dot" />
  <circle cx="490.7" cy="56.2" r="4" class="sp-dot" />
  <circle cx="440.2" cy="69.3" r="4" class="sp-dot" />
  <circle cx="500.2" cy="94.2" r="4" class="sp-dot" />
  <circle cx="423.4" cy="48.9" r="4" class="sp-dot" />
  <circle cx="431.1" cy="50.0" r="4" class="sp-dot" />
  <circle cx="458.5" cy="76.3" r="4" class="sp-dot" />
  <circle cx="435.8" cy="90.0" r="4" class="sp-dot" />
  <circle cx="442.7" cy="70.6" r="4" class="sp-dot" />
  <circle cx="472.6" cy="66.6" r="4" class="sp-dot" />
  <circle cx="480.3" cy="88.6" r="4" class="sp-dot" />
  <circle cx="463.2" cy="84.4" r="4" class="sp-dot" />
  <circle cx="452.3" cy="47.5" r="4" class="sp-dot" />
  <circle cx="497.6" cy="89.8" r="4" class="sp-dot" />
  <circle cx="471.3" cy="54.2" r="4" class="sp-dot" />
  <circle cx="453.4" cy="59.7" r="4" class="sp-dot" />
  <circle cx="494.0" cy="87.5" r="4" class="sp-dot" />
  <circle cx="434.8" cy="66.0" r="4" class="sp-dot" />
  <circle cx="464.6" cy="85.5" r="4" class="sp-dot" />
  <circle cx="478.5" cy="52.7" r="4" class="sp-dot" />
  <circle cx="459.7" cy="89.5" r="4" class="sp-dot" />
  <circle cx="443.9" cy="53.2" r="4" class="sp-dot" />
  <circle cx="469.8" cy="51.8" r="4" class="sp-dot" />
  <circle cx="444.9" cy="69.7" r="4" class="sp-dot" />
  <circle cx="443.3" cy="61.6" r="4" class="sp-dot" />
  <circle cx="431.4" cy="72.2" r="4" class="sp-dot" />
  <circle cx="496.5" cy="91.0" r="4" class="sp-dot" />
  <circle cx="444.6" cy="80.9" r="4" class="sp-dot" />
  <circle cx="492.3" cy="44.3" r="4" class="sp-dot" />
  <circle cx="470.7" cy="60.2" r="4" class="sp-dot" />
  <circle cx="452.7" cy="72.3" r="4" class="sp-dot" />
  <circle cx="478.7" cy="69.3" r="4" class="sp-dot" />
  <circle cx="467.6" cy="81.2" r="4" class="sp-dot" />
  <circle cx="463.7" cy="69.2" r="4" class="sp-dot" />
  <circle cx="421.5" cy="47.9" r="4" class="sp-dot" />
  <circle cx="462.0" cy="56.8" r="4" class="sp-dot" />
  <circle cx="485.0" cy="88.1" r="4" class="sp-dot" />
  <circle cx="473.6" cy="62.6" r="4" class="sp-dot" />
  <circle cx="487.9" cy="83.9" r="4" class="sp-dot" />
  <circle cx="501.7" cy="95.3" r="4" class="sp-dot" />
  <circle cx="471.5" cy="76.6" r="4" class="sp-dot" />
  <circle cx="515.3" cy="79.2" r="4" class="sp-dot" />
  <circle cx="417.6" cy="75.7" r="4" class="sp-dot" />
  <circle cx="453.3" cy="60.3" r="4" class="sp-dot" />
  <circle cx="389.3" cy="91.5" r="4" class="sp-dot" />
  <circle cx="483.0" cy="68.3" r="4" class="sp-dot" />
  <circle cx="462.6" cy="91.4" r="4" class="sp-dot" />
  <circle cx="507.3" cy="59.9" r="4" class="sp-dot" />
  <circle cx="449.7" cy="89.1" r="4" class="sp-dot" />
  <circle cx="403.3" cy="84.9" r="4" class="sp-dot" />
  <circle cx="495.8" cy="75.9" r="4" class="sp-dot" />
  <circle cx="422.4" cy="67.0" r="4" class="sp-dot" />
  <circle cx="424.5" cy="51.3" r="4" class="sp-dot" />
  <circle cx="455.1" cy="84.1" r="4" class="sp-dot" />
  <circle cx="477.6" cy="62.8" r="4" class="sp-dot" />
  <circle cx="445.8" cy="78.4" r="4" class="sp-dot" />
  <circle cx="465.2" cy="50.9" r="4" class="sp-dot" />
  <circle cx="407.3" cy="48.3" r="4" class="sp-dot" />
  <circle cx="508.4" cy="51.5" r="4" class="sp-dot" />
  <circle cx="458.1" cy="86.1" r="4" class="sp-dot" />
  <circle cx="463.4" cy="53.2" r="4" class="sp-dot" />
  <circle cx="476.4" cy="90.9" r="4" class="sp-dot" />
  <circle cx="464.7" cy="63.3" r="4" class="sp-dot" />
  <circle cx="465.6" cy="74.0" r="4" class="sp-dot" />
  <circle cx="434.0" cy="62.2" r="4" class="sp-dot" />
  <circle cx="456.8" cy="76.3" r="4" class="sp-dot" />
  <circle cx="472.3" cy="48.9" r="4" class="sp-dot" />
  <circle cx="489.2" cy="64.9" r="4" class="sp-dot" />
  <circle cx="456.6" cy="92.7" r="4" class="sp-dot" />
  <circle cx="462.6" cy="53.3" r="4" class="sp-dot" />
  <circle cx="469.5" cy="78.0" r="4" class="sp-dot" />
  <circle cx="476.0" cy="61.0" r="4" class="sp-dot" />
  <circle cx="465.8" cy="59.6" r="4" class="sp-dot" />
  <circle cx="452.9" cy="45.2" r="4" class="sp-dot" />
  <circle cx="445.7" cy="45.0" r="4" class="sp-dot" />
  <circle cx="491.5" cy="93.4" r="4" class="sp-dot" />
  <circle cx="468.3" cy="87.1" r="4" class="sp-dot" />
  <circle cx="460.6" cy="85.7" r="4" class="sp-dot" />
  <circle cx="557.4" cy="86.0" r="4" class="sp-dot" />
  <circle cx="484.7" cy="93.6" r="4" class="sp-dot" />
  <circle cx="483.9" cy="52.2" r="4" class="sp-dot" />
  <circle cx="464.3" cy="74.4" r="4" class="sp-dot" />
  <circle cx="431.6" cy="69.8" r="4" class="sp-dot" />
  <circle cx="491.8" cy="73.8" r="4" class="sp-dot" />
  <circle cx="457.5" cy="92.8" r="4" class="sp-dot" />
  <circle cx="461.5" cy="83.5" r="4" class="sp-dot" />
  <circle cx="488.8" cy="94.4" r="4" class="sp-dot" />
  <circle cx="488.5" cy="50.1" r="4" class="sp-dot" />
  <circle cx="466.7" cy="77.9" r="4" class="sp-dot" />
  <circle cx="460.5" cy="79.1" r="4" class="sp-dot" />
  <circle cx="518.7" cy="82.8" r="4" class="sp-dot" />
  <circle cx="476.0" cy="76.1" r="4" class="sp-dot" />
  <circle cx="431.3" cy="87.2" r="4" class="sp-dot" />
  <circle cx="481.0" cy="59.7" r="4" class="sp-dot" />
  <circle cx="464.2" cy="92.2" r="4" class="sp-dot" />
  <circle cx="460.9" cy="65.1" r="4" class="sp-dot" />
  <circle cx="479.1" cy="75.1" r="4" class="sp-dot" />
  <circle cx="466.6" cy="90.6" r="4" class="sp-dot" />
  <circle cx="516.1" cy="80.6" r="4" class="sp-dot" />
  <circle cx="465.7" cy="60.1" r="4" class="sp-dot" />
  <circle cx="467.1" cy="56.0" r="4" class="sp-dot" />
  <circle cx="492.5" cy="61.0" r="4" class="sp-dot" />
  <circle cx="444.2" cy="76.6" r="4" class="sp-dot" />
  <circle cx="488.4" cy="95.8" r="4" class="sp-dot" />
  <circle cx="458.3" cy="90.7" r="4" class="sp-dot" />
  <circle cx="493.1" cy="64.8" r="4" class="sp-dot" />
  <circle cx="436.2" cy="64.8" r="4" class="sp-dot" />
  <circle cx="471.7" cy="86.5" r="4" class="sp-dot" />
  <circle cx="415.2" cy="58.8" r="4" class="sp-dot" />
  <circle cx="447.6" cy="65.4" r="4" class="sp-dot" />
  <circle cx="460.4" cy="44.7" r="4" class="sp-dot" />
  <circle cx="473.8" cy="53.6" r="4" class="sp-dot" />
  <circle cx="515.3" cy="72.1" r="4" class="sp-dot" />
  <circle cx="511.4" cy="80.1" r="4" class="sp-dot" />
  <circle cx="422.5" cy="76.0" r="4" class="sp-dot" />
  <circle cx="547.4" cy="62.9" r="4" class="sp-dot" />
  <circle cx="610.7" cy="93.5" r="4" class="sp-dot" />
  <circle cx="662.3" cy="76.4" r="4" class="sp-dot" />
  <circle cx="606.7" cy="52.1" r="4" class="sp-dot" />
  <circle cx="669.9" cy="47.5" r="4" class="sp-dot" />
  <circle cx="580.1" cy="94.6" r="4" class="sp-dot" />
  <circle cx="610.1" cy="95.4" r="4" class="sp-dot" />
  <circle cx="619.2" cy="91.8" r="4" class="sp-dot" />
  <circle cx="538.0" cy="75.4" r="4" class="sp-dot" />
  <circle cx="753.9" cy="60.2" r="4" class="sp-dot" />
  <circle cx="808.5" cy="48.7" r="4" class="sp-dot" />
  <circle cx="515.4" cy="57.4" r="4" class="sp-dot" />
  <circle cx="844.0" cy="55.6" r="4" class="sp-dot" />
  <circle cx="821.4" cy="92.3" r="4" class="sp-dot" />
  <circle cx="591.0" cy="90.4" r="5" class="sp-sub" />
  <circle cx="580.9" cy="84.5" r="5" class="sp-sub" />
  <circle cx="641.0" cy="51.7" r="5" class="sp-sub" />
  <circle cx="576.7" cy="56.4" r="5" class="sp-sub" />
  <circle cx="732.0" cy="59.6" r="5" class="sp-sub" />
  <circle cx="578.4" cy="93.3" r="5" class="sp-sub" />
  <circle cx="653.4" cy="52.5" r="5" class="sp-sub" />
  <circle cx="623.8" cy="85.1" r="5" class="sp-sub" />
  <circle cx="528.6" cy="79.4" r="5" class="sp-sub" />
  <circle cx="518.2" cy="72.5" r="5" class="sp-sub" />
  <circle cx="599.6" cy="93.9" r="5" class="sp-sub" />
  <circle cx="420.0" cy="57.6" r="5" class="sp-sub" />
  <polygon points="487.5,30 480,18 495,18" class="sp-mean" />
  <text x="500" y="22" class="sp-lab sp-mean-lab" text-anchor="start">mean: "looks safe"</text>
  <text x="760" y="40" class="sp-lab sp-sub-lab">one subgroup</text>
</svg>
<div class="strip-label"><span class="schematic-label">Schematic, not data</span></div>
</div>

<div class="card dark">Report <strong>tails, subgroups and attack conditions</strong>, not one average.</div>

<div class="ref-bottom"><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12647387/">Rodriguez 2025</a> · <a href="https://pubmed.ncbi.nlm.nih.gov/40652760/">Meurers 2025</a> · <a href="https://doi.org/10.1038/s41586-026-10688-0">Knolle 2026</a> (<a href="https://www.tum.de/en/news-and-events/all-news/press-releases/details/study-reveals-privacy-risks-in-medical-ai">TUM release</a>)</div>

<style>
.strip { position: relative; margin: 0.2rem 0 0.4rem; }
.strip svg { width: 100%; height: 125px; }
.strip-label { position: absolute !important; top: 0; left: 0; }
.sp-axis { stroke: var(--asc-text); stroke-width: 1.5; }
.sp-chance { stroke: var(--asc-muted); stroke-width: 1.5; stroke-dasharray: 4 4; }
.sp-dot { fill: var(--aalto-blue); opacity: 0.55; }
.sp-sub { fill: var(--aalto-red); stroke: #000; stroke-width: 0.8; }
.sp-mean { fill: var(--asc-text); }
.sp-lab { font-size: 13px; fill: var(--asc-muted); text-anchor: middle; }
.sp-mean-lab { fill: var(--asc-text); font-weight: 600; }
.sp-sub-lab { fill: #c0302d; font-weight: 600; }
.sp-tick { font-size: 12px; fill: var(--asc-muted); }
</style>

<!--
The strip plot is schematic: the sources report no per-patient percentages, so none are shown.
Knolle 2026 was read through the abstract and the TUM press release (the Nature page would not load). Meurers 2025 was taken from the report, not opened.
-->

---
layout: default
---

###### Part C · As closed as necessary

# Privacy-enhancing technologies move risk, they do not remove it

<table class="bp-matrix pet compact">
  <thead>
    <tr><th>Technique</th><th>Gives you</th><th></th><th>Risk moves to</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Pseudonymisation</strong></td><td>No direct identifiers in working data</td><td class="pet-arrow">→</td><td class="bp-orange">Anyone who can link; narrative text still identifies</td></tr>
    <tr><td><strong>Synthetic data</strong></td><td>Teaching, software tests, previews</td><td class="pet-arrow">→</td><td class="bp-orange">Fidelity and disclosure; membership inference was the hardest criterion (Demuth 2025)</td></tr>
    <tr><td><strong>Differential privacy</strong></td><td>Formal bound on one record's influence</td><td class="pet-arrow">→</td><td class="bp-orange">Correlations and small groups (Adams 2025); the budget is a value judgement</td></tr>
    <tr><td><strong>Federated learning</strong></td><td>Raw data stay at each site</td><td class="pet-arrow">→</td><td class="bp-orange">Updates can leak; site differences cost accuracy</td></tr>
    <tr><td><strong>Secure environment</strong></td><td>Control of who, where and what leaves</td><td class="pet-arrow">→</td><td class="bp-orange">Cost, usability, reproducibility (slide 18)</td></tr>
  </tbody>
</table>

<div class="card dark">Use bundles. <strong>Report parameters, not labels.</strong></div>

<div class="ref-bottom"><a href="https://pubmed.ncbi.nlm.nih.gov/40343279/">Adams 2025</a> · <a href="https://pubmed.ncbi.nlm.nih.gov/41032725/">Demuth 2025</a> · <a href="https://www.sciencedirect.com/science/article/pii/S2773186325002257">Federated learning review 2025</a> · <a href="https://lumi-ai-factory.eu/articles/international-data-protection-day/">Honkela interview 2026</a> · <a href="https://www.edpb.europa.eu/our-work-tools/documents/public-consultations/2025/guidelines-012025-pseudonymisation_en">EDPB Guidelines 01/2025</a></div>

<style>
.pet { margin-bottom: 0.6rem; }
.slidev-layout .pet.compact td, .slidev-layout .pet.compact th { font-size: 0.85rem; padding: 0.35rem 0.6rem; }
.pet td:first-child { width: 22%; }
.pet .pet-arrow { width: 2.5rem; text-align: center; font-size: 1.3rem; color: var(--aalto-orange); }
</style>

---
layout: default
---

<div class="corner-icon"><DomainGrid mini :active="['int-cyb', 'priv-cyb']" /></div>

###### Part C · As closed as necessary

# "Closed" is only as real as the security behind it

<div class="timeline">
  <div class="tl-line"></div>
  <div class="tl-item">
    <div class="tl-year">2020</div>
    <div class="tl-card"><b>Vastaamo</b> <span class="cia-tag c">C</span><br>Psychotherapy records stolen, patients extorted one by one. <span class="badge incident">Incident</span><div class="tl-miss">Missing: database protection, encryption (to confirm)</div></div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2023</div>
    <div class="tl-card"><b>University of Manchester</b> <span class="cia-tag c">C</span><br>Research data on about 1.1 million NHS patients, including trauma and terror-attack victims. <span class="badge incident">Incident</span><div class="tl-miss">Missing: to confirm from incident report</div></div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2023</div>
    <div class="tl-card"><b>Microsoft AI research</b> <span class="cia-tag c">C</span> <span class="cia-tag i">I</span><br>A link in an open-model repo opened 38 TB with <strong>write</strong> access: the models could have been overwritten. <span class="badge incident">Incident</span><div class="tl-miss">Missing: scoped, expiring tokens</div></div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2026</div>
    <div class="tl-card"><b>UK Biobank</b> <span class="cia-tag c">C</span><br>No hack. Response: no participant-level downloads, a data airlock, confirmed deletion. <span class="badge incident">Incident</span><div class="tl-miss">Missing: export limits, enforcement</div></div>
  </div>
</div>

- **Contracts state rules, controls enforce them:** MFA, least privilege, logging, export limits, output checks.
- **Art 32 GDPR binds you now.** NIS2 and the Finnish Cybersecurity Act exclude universities from "research organisation", so do not assume a sector regime covers you.

<div class="ref-bottom"><a href="https://cyberscoop.com/finnish-psychotherapy-data-breach-vastaamo/">Vastaamo 2020</a> · <a href="https://www.govinfosecurity.com/trauma-terrorist-victim-data-breached-in-university-attack-a-22409">Manchester 2023</a> · <a href="https://wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers">Wiz 2023</a> · <a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UKB Oversight 2026</a> · <a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> · <a href="https://eur-lex.europa.eu/eli/dir/2022/2555/oj">NIS2</a> · <a href="https://kyberturvallisuuskeskus.fi/en/our-activities/regulation-and-supervision/public-administration-and-research-organisations">NCSC-FI</a> · <a href="https://www.finlex.fi/api/media/statute/535367/mainPdf/main.pdf">FI Cybersecurity Act 124/2025</a></div>

<style>
.timeline { position: relative; display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 0.6rem; margin-bottom: 0.6rem; }
.tl-line { position: absolute !important; left: 0; right: 0; top: 0.75rem; height: 3px; background: var(--asc-border); }
.tl-year { position: relative; display: inline-block; padding: 0.05rem 0.6rem; border-radius: 999px; background: var(--asc-night); color: var(--asc-paper); font-weight: 700; font-size: 0.8rem; margin-bottom: 0.35rem; }
.tl-card { padding: 0.45rem 0.6rem; border: 2px solid var(--asc-border); border-radius: var(--asc-radius-md); background: var(--asc-surface); font-size: 0.72rem; line-height: 1.25; }
.tl-card b { font-family: var(--asc-font-serif); font-size: 0.85rem; }
.tl-miss { margin-top: 0.3rem; padding-top: 0.25rem; border-top: 1px dashed var(--asc-border); color: var(--asc-muted); font-style: italic; }
.cia-tag { display: inline-grid; place-items: center; width: 1.1rem; height: 1.1rem; border-radius: 999px; font-size: 0.6rem; font-weight: 700; color: #fff; vertical-align: 0.1em; }
.cia-tag.c { background: var(--asc-night); }
.cia-tag.i { background: var(--aalto-red); }
.cia-tag.a { background: var(--aalto-blue); }
</style>

<!--
The "missing control" line under each incident is my reading of the public reports; revise wording.

CHECK BEFORE PRESENTING
- Confirm Aalto's actual NIS2 position with the CISO. A university could still be in scope through another role.
-->

---
layout: default
---

###### Part D · AI moves the line

# Ask which environment, not which chatbot

<div class="grid-2-3">
<div class="dense">

- **Two separate problems:** epistemic (is the output right?) and information governance (who receives the input?).
- **Uploading is disclosure** to a processing system. Assess roles, location, retention, training use and admin access per product and contract.
- **Keep the evidence straight.** "Everything you type becomes public" is not established. "Treat non-approved tools as public" is still sound policy.

<div class="running-case"><strong>Running case</strong> Pseudonymised transcripts do not go into a consumer chatbot.</div>

</div>
<div>
  <div class="ladder">
    <div class="ld-row" style="--c: var(--aalto-green)"><span class="ld-class">Public</span><span class="ld-arrow">→</span><span class="ld-tool">Any tool</span></div>
    <div class="ld-row" style="--c: var(--aalto-darkyellow)"><span class="ld-class">Internal</span><span class="ld-arrow">→</span><span class="ld-tool">Approved tools</span></div>
    <div class="ld-row" style="--c: var(--aalto-orange)"><span class="ld-class">Confidential</span><span class="ld-arrow">→</span><span class="ld-tool">Contractual guarantees or local models</span></div>
    <div class="ld-row" style="--c: var(--aalto-red)"><span class="ld-class">Secret</span><span class="ld-arrow">→</span><span class="ld-tool">Local tools inside a TRE</span></div>
  </div>
  <div class="ld-caption">Rule by data class, not by brand</div>
  <div class="risk-inset">
    <div class="ri blue"><b>Fundamental digital risks</b>confidentiality, security, non-approved tools</div>
    <div class="ri yellow"><b>AI-amplified risks</b>fabrication, falsification, irreproducibility</div>
    <div class="ri red"><b>AI-native risks</b>bias, opacity, deskilling, sycophancy</div>
  </div>
</div>
</div>

<div class="ref-bottom"><a href="https://www.aalto.fi/en/research-art/best-practices-for-ai-use-in-research-work">Aalto best practices</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Living Guidelines v4</a> · <a href="https://journals.sagepub.com/doi/10.1177/16094069251404329">Jones 2025</a> · <a href="https://eglerean.github.io/assets/docs/2026_05_06_AI_research_risks.pdf">Glerean 2026, AI risks</a></div>

<style>
.ladder { display: flex; flex-direction: column; gap: 0.35rem; }
.ld-row { display: grid; grid-template-columns: 8rem auto 1fr; align-items: center; gap: 0.6rem; padding: 0.45rem 0.8rem; border-left: 8px solid var(--c); border-radius: var(--asc-radius-sm); background: color-mix(in srgb, var(--c) 30%, transparent); }
.ld-class { font-family: var(--asc-font-serif); font-weight: 700; }
.ld-arrow { color: var(--asc-muted); }
.ld-caption { margin: 0.3rem 0 0.6rem; font-size: 0.7rem; color: var(--asc-muted); text-align: right; }
.risk-inset { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 0.4rem; }
.ri { padding: 0.35rem 0.5rem; border-radius: var(--asc-radius-sm); font-size: 0.6rem; line-height: 1.2; color: #000; }
.ri b { display: block; font-size: 0.68rem; }
.ri.blue { background: var(--aalto-blue); }
.ri.yellow { background: var(--aalto-yellow); }
.ri.red { background: var(--aalto-red); }
</style>

<!--
The small coloured cards are the "AI risks in research" framework from the previous deck (Glerean 2026).

CHECK BEFORE PRESENTING
- The four classes come from the public aalto.fi page; the adaptation of the Finnish classification model is still in progress.
-->

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="int-ai" /></div>

###### Part D · AI moves the line

# Disclosure is not documentation

<div class="grid-2-3">
<div class="dense">

- **"We used ChatGPT"** does not let anyone reconstruct the work: the same prompt can give different outputs.
- **Keep:** tool and version, task, input type, prompt logic, what was accepted or rejected, who verified it.
- **ALLEA §3.1:** hiding AI use is a violation. **EC Guidelines v4:** retain or share prompts, logs and versions when needed "to understand, reproduce or audit". **TENK 2026:** document AI like any other important method, including in metadata and the DMP.
- **Full prompt logs can leak source text.** Keep a restricted audit log and publish a sanitised workflow.

</div>
<div class="lanes">
  <div class="ln-session"><b>One AI session</b><span>prompts · uploaded excerpts · outputs · accept/reject decisions</span></div>
  <div class="ln-filter">▼ filter: remove source text, keep the method ▼</div>
  <div class="ln-split">
    <div class="ln-lane ln-restricted"><b>Restricted audit log</b><span>full prompts and outputs, with interview quotes</span><em>access: PI, auditors, ethics board</em></div>
    <div class="ln-lane ln-public"><b>Public supplement</b><span>tool, version, task, prompt templates, verification steps</span><em>with the paper</em></div>
  </div>
  <div class="running-case"><strong>Running case</strong> Interview quotes stay in the restricted lane.</div>
</div>
</div>

<div class="ref-bottom"><a href="https://doi.org/10.1186/s41073-026-00245-8">Cwik 2026</a> · <a href="https://journals.sagepub.com/doi/10.1177/16094069251404329">Jones 2025</a> · <a href="https://doi.org/10.48550/arXiv.2602.14349">Cui &amp; Alexander 2026</a> · <a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Guidelines v4</a> · <a href="https://tenk.fi/sites/default/files/2026-06/Artificial%20Intelligence%20in%20Research.%20TENK%27s%20Recommendation%202026.pdf">TENK 2026</a></div>

<style>
.lanes { display: flex; flex-direction: column; gap: 0.4rem; }
.lanes b { display: block; font-family: var(--asc-font-serif); }
.lanes span { display: block; font-size: 0.75rem; line-height: 1.2; }
.lanes em { display: block; margin-top: 0.25rem; font-size: 0.65rem; opacity: 0.8; }
.ln-session { padding: 0.5rem 0.8rem; border-radius: var(--asc-radius-md); background: var(--asc-night); color: var(--asc-paper); }
.ln-filter { text-align: center; font-size: 0.7rem; color: var(--asc-muted); }
.ln-split { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem; }
.ln-lane { padding: 0.5rem 0.7rem; border-radius: var(--asc-radius-md); border: 2px solid; }
.ln-restricted { border-color: var(--aalto-red); background: color-mix(in srgb, var(--aalto-red) 18%, transparent); }
.ln-public { border-color: var(--aalto-green); background: color-mix(in srgb, var(--aalto-green) 18%, transparent); }
</style>

<!--
Cwik 2026: only the bibliographic record was confirmed. Jones 2025 was taken from the report, not opened.
-->

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="priv-ai" /></div>

###### Part D · AI moves the line

# LLMs are cutting the cost of re-identification

<div class="flow reid">
  <div class="step"><b>Transcript</b>redacted, no names</div>
  <div class="arrow">→</div>
  <div class="step"><b>Attributes</b>role, project, affiliation, events<span class="tag">LLM</span></div>
  <div class="arrow">→</div>
  <div class="step"><b>Web search</b>papers, profiles, news<span class="tag">agent</span></div>
  <div class="arrow">→</div>
  <div class="step"><b>Candidates</b>shortlist of people</div>
  <div class="arrow">→</div>
  <div class="step reid-end"><b>Match + confidence</b><span class="tag">$0.50–4 · minutes</span></div>
</div>
<div class="reid-note"><span class="schematic-label">No names needed</span></div>

<div class="dense">

- **Published interviews:** of 24 public Anthropic Interviewer transcripts mentioning published work, 6 were linked to publications, at under $0.50 and about 4 minutes each. <span class="badge preprint">Preprint</span>
- **Pseudonymous profiles:** 226 of 338 Hacker News users identified at 90% precision, $1–4 each. <span class="badge preprint">Preprint</span>
- **Redaction:** after named-entity masking, at least one attacker still succeeded on 85.3% of a sample of synthetic test transcripts. The signal sits in role, project and affiliation. <span class="badge preprint">Preprint</span>
- **The legal test already expects this.** Recital 26 counts cost, time and technological developments. EDPB draft 02/2026: AI, especially agentic AI, lowers time and cost, so reassess periodically. <span class="badge draft">Draft</span>
- Demonstrated vulnerability, not documented harm: small samples, partly manual verification.

</div>

<div class="running-case"><strong>Running case</strong> This is why redacted transcripts still stay controlled.</div>

<div class="ref-bottom"><a href="https://arxiv.org/abs/2601.05918">Li 2026</a> · <a href="https://arxiv.org/abs/2602.16800">Lermen 2026</a> · <a href="https://arxiv.org/abs/2610.05586">Wen &amp; Li 2026</a> · <a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> Recital 26 · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026 (draft)</a> · <a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UKB Oversight 2026</a></div>

<style>
.slidev-layout .reid .step { font-size: 0.72rem; padding: 0.35rem 0.5rem; }
.slidev-layout .reid .step b { font-size: 0.82rem; }
.slidev-layout .reid .reid-end { background: var(--aalto-red); border-color: var(--aalto-red); color: #000; }
.reid-note { text-align: right; margin: 0.2rem 0 0.1rem; }
.running-case { margin-top: 0.3rem; }
</style>

<!--
CHECK BEFORE PRESENTING
- The four preprints are fast-moving: check for published versions and changed numbers.
- EDPB draft 02/2026 read through summaries only.
-->

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="priv-ai" /></div>

###### Part D · AI moves the line

# Sharing model weights can be sharing data

<div class="grid-3-2">
<div class="dense">

- **Two different attacks:** membership inference (was this person in training?) and extraction (what did the model memorise?). State which one, under which conditions.
- **EDPB Opinion 28/2024:** a model trained on personal data is not automatically anonymous. Draft 02/2026 treats inference through queries as in scope. <span class="badge draft">Draft</span>
- Knolle 2026 recommends patient-level audits before release, access control and differential privacy.
- **Weights cannot be recalled**, and unlearning is largely theoretical without special training.
- **Minimising vs measuring:** AI Act Art 4a allows special-category data only where strictly necessary for bias detection and correction, under safeguards. It is not a training licence. <span class="badge binding">Binding</span>

</div>
<div class="release">
  <div class="rl-step rl-top" style="--n: 3"><b>Public weights</b><span>no recall possible</span></div>
  <div class="rl-gate">privacy audit gate</div>
  <div class="rl-step" style="--n: 2"><b>Gated weights</b><span>registered users, access control, query logging</span></div>
  <div class="rl-gate">privacy audit gate</div>
  <div class="rl-step" style="--n: 1"><b>Code</b><span>training and evaluation pipeline</span></div>
  <div class="rl-gate">privacy audit gate</div>
  <div class="rl-step" style="--n: 0"><b>Paper</b><span>methods, aggregate results</span></div>
  <div class="rl-note small">Imaging example: qualified verifiers rerun the workflow inside secure environments instead of downloading weights.</div>
</div>
</div>

<div class="ref-bottom"><a href="https://www.edpb.europa.eu/our-work-tools/our-documents/opinion-board-art-64/opinion-282024-certain-data-protection-aspects_en">EDPB Opinion 28/2024</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026 (draft)</a> · <a href="https://doi.org/10.1038/s41586-026-10688-0">Knolle 2026</a> · <a href="https://lumi-ai-factory.eu/articles/international-data-protection-day/">Honkela interview 2026</a> · <a href="https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng">AI Omnibus, Reg. (EU) 2026/1744</a></div>

<style>
.release { display: flex; flex-direction: column; gap: 0.15rem; }
.rl-step { margin-left: calc(var(--n) * 1.2rem); padding: 0.35rem 0.7rem; border-radius: var(--asc-radius-sm); background: color-mix(in srgb, var(--aalto-blue) calc(20% + var(--n) * 20%), transparent); line-height: 1.15; }
.rl-step b { font-family: var(--asc-font-serif); margin-right: 0.4rem; }
.rl-step span { font-size: 0.7rem; }
.rl-top { background: var(--aalto-red); color: #000; }
.rl-gate { align-self: center; font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.05em; color: var(--asc-muted); border-top: 2px dashed var(--aalto-orange); border-bottom: 2px dashed var(--aalto-orange); padding: 0.05rem 0.6rem; }
.rl-note { margin-top: 0.5rem; color: var(--asc-muted); }
</style>

<!--
CHECK BEFORE PRESENTING
- Final text of Reg. (EU) 2026/1744 (Art 4a) was read through summaries only; check against the primary text.
- Knolle 2026 read through abstract and press release.
-->

---
layout: default
---

<div class="corner-icon"><DomainGrid mini active="cyb-ai" /></div>

###### Part D · AI moves the line

# Agents turn untrusted text into actions

<div class="grid-2-3">
<div>
<svg class="trifecta" viewBox="-50 0 440 295" role="img" aria-label="Lethal trifecta: private data, untrusted content and exfiltration, with the exfiltration leg cut">
  <line x1="170" y1="45" x2="45" y2="235" class="tf-leg" />
  <line x1="170" y1="45" x2="295" y2="235" class="tf-leg" />
  <line x1="45" y1="235" x2="295" y2="235" class="tf-leg tf-cut" />
  <text x="170" y="236" class="tf-scissors">✂</text>
  <circle cx="170" cy="45" r="14" class="tf-node" />
  <circle cx="45" cy="235" r="14" class="tf-node" />
  <circle cx="295" cy="235" r="14" class="tf-node" />
  <text x="170" y="14" class="tf-lab">Private data</text>
  <text x="192" y="50" class="tf-ex" text-anchor="start">participant data</text>
  <text x="45" y="266" class="tf-lab">Untrusted content</text>
  <text x="45" y="283" class="tf-ex">PDFs, web pages</text>
  <text x="295" y="266" class="tf-lab">A way out</text>
  <text x="295" y="283" class="tf-ex">network access</text>
</svg>
</div>
<div class="dense">

- **Lethal trifecta:** private data, untrusted content and a way to send data out.
- **Prompt injection has reached peer review.** Authors hid "positive review" prompts; ICML 2026 used hidden prompts to flag 506 reviewers and desk-rejected 497 papers. EC Guidelines v4 now names hidden prompts. <span class="badge incident">Incident</span>
- **Open inputs need checks too.** Pickle model files run code on load; non-existent packages reached at least 5.2% for commercial models and 21.7% for open-source models. <span class="badge audit">Audit</span>
- **Validate, minimize, contain:** cut one leg of the trifecta. No network, read-only data, disposable containers, pinned hashes, human check points.
- EC Guidelines v4: agents are never "a delegation of control or responsibility".

</div>
</div>

<div class="ref-bottom"><a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">Willison 2025</a> · <a href="https://asia.nikkei.com/business/technology/artificial-intelligence/positive-review-only-researchers-hide-ai-prompts-in-papers">Nikkei 2025</a> · <a href="https://blog.icml.cc/2026/03/18/on-violations-of-llm-review-policies/">ICML 2026</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Guidelines v4</a> · <a href="https://thehackernews.com/2025/02/malicious-ml-models-found-on-hugging.html">nullifAI 2025</a> · <a href="https://arxiv.org/abs/2406.10279">Spracklen 2025</a> · <a href="https://coderefinery.github.io/coding-with-ai/security/">CodeRefinery security page</a></div>

<style>
.trifecta { width: 100%; max-width: 360px; }
.tf-leg { stroke: var(--asc-text); stroke-width: 4; }
.tf-cut { stroke: var(--aalto-red); stroke-dasharray: 10 8; }
.tf-scissors { font-size: 30px; text-anchor: middle; dominant-baseline: middle; fill: var(--aalto-red); paint-order: stroke; stroke: var(--asc-bg); stroke-width: 6px; }
.tf-node { fill: var(--aalto-blue); stroke: var(--asc-text); stroke-width: 2; }
.tf-lab { font-family: var(--asc-font-serif); font-weight: 700; font-size: 15px; text-anchor: middle; fill: var(--asc-text); }
.tf-ex { font-size: 12px; text-anchor: middle; fill: var(--asc-muted); }
</style>

<!--
The previous deck's risk-domains figure (CodeRefinery) is in public/risk-domains.png if you want to show it here.
-->

---
layout: default
---

###### Part E · Closed, but verifiable

# Secure environments are a reproducibility variable

<div class="verify">
  <div class="flow">
    <div class="step v-pub"><b>Public code + container</b>versioned, pinned</div>
    <div class="arrow">→</div>
    <div class="step v-sec"><b>Secure environment</b>versioned dataset</div>
    <div class="arrow">→</div>
    <div class="step v-sec"><b>Run</b>machine-executable workflow</div>
    <div class="arrow">→</div>
    <div class="step v-check"><b>Output check</b>predictable rules</div>
    <div class="arrow">→</div>
    <div class="step v-pub"><b>Public result</b>with public metadata</div>
  </div>
  <div class="v-second"><span>↳ second path: a <strong>qualified verifier</strong> gets the same container and dataset version inside the environment and reruns it</span></div>
</div>

<div class="dense">

- Same R scripts, two English secure settings: data preparation was the obstacle. *"Even with perfect code sharing, data reproducibility remains a challenge."*
- **Closure has a price.** Controlled trial datasets took 270 days on average to access, open ones 8. Two UK TREs differed on approval, accreditation, cost and linkage. Lower-resource institutions report more difficulty.
- **EU direction:** EHDS permits and secure processing environments; only non-personal outputs leave; results public within 18 months (Art 61). <span class="badge phasing">Phasing in</span>
- **Finland:** since 1 May 2026 Findata can allow another environment for a special reason, with the recipient as independent controller. <span class="badge binding">Binding</span>
- **Build for verification:** approved containers, stable dataset versions, machine-executable workflows, public metadata, predictable output checks.

</div>

<div class="ref-bottom"><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12273930/">Williams 2025</a> · <a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12647387/">Rodriguez 2025</a> · <a href="https://ijpds.org/article/view/3243">IJPDS, barriers across TREs</a> · <a href="https://pubmed.ncbi.nlm.nih.gov/39565766/">Waithira 2024</a> · <a href="https://eur-lex.europa.eu/eli/reg/2025/327/oj">EHDS</a> (<a href="https://streamlex.eu/articles/ehds-en-art-61/">Art 61</a>) · <a href="https://findata.fi/en/permits/data-permits/">Findata</a></div>

<style>
.verify { margin-bottom: 0.4rem; }
.slidev-layout .verify .step { font-size: 0.72rem; }
.slidev-layout .verify .step b { font-size: 0.82rem; }
.slidev-layout .verify .v-pub { border-color: var(--aalto-green); }
.slidev-layout .verify .v-sec { background: var(--asc-night); border-color: var(--asc-night); color: var(--asc-paper); }
.slidev-layout .verify .v-check { border-color: var(--aalto-orange); background: color-mix(in srgb, var(--aalto-orange) 25%, transparent); }
.v-second { margin: 0.3rem 0 0 15%; font-size: 0.75rem; color: var(--asc-muted); }
</style>

---
layout: default
---

###### Part E · Closed, but verifiable

# Check the status before you cite the rule

<div class="grid-2-3 status">
<div>
<svg class="swim" viewBox="0 0 430 210" role="img" aria-label="Swimlane timeline 2018 to 2031 for privacy, AI, health and cyber rules, with a you-are-here marker at November 2026">
  <!-- x = 70 + (years since Jan 2018) * 25 -->
  <g class="sw-lanes">
    <text x="0" y="42">Privacy</text><line x1="70" y1="38" x2="420" y2="38" />
    <text x="0" y="82">AI</text><line x1="70" y1="78" x2="420" y2="78" />
    <text x="0" y="122">Health</text><line x1="70" y1="118" x2="420" y2="118" />
    <text x="0" y="162">Cyber</text><line x1="70" y1="158" x2="420" y2="158" />
  </g>
  <g class="sw-years">
    <text x="70" y="192">2018</text><text x="145" y="192">2021</text><text x="220" y="192">2024</text><text x="295" y="192">2027</text><text x="370" y="192">2030</text>
  </g>
  <!-- Privacy: GDPR applies May 2018 -->
  <circle cx="78" cy="38" r="6" class="sw-bind" /><text x="88" y="30" class="sw-ev">GDPR</text>
  <!-- AI: prohibitions Feb 2025, GPAI Aug 2025, AI Omnibus Jul 2026 (binding); high-risk Annex III Dec 2027, Annex I Aug 2028 -->
  <circle cx="247" cy="78" r="6" class="sw-bind" /><circle cx="260" cy="78" r="6" class="sw-bind" /><circle cx="282" cy="78" r="6" class="sw-bind" />
  <text x="243" y="70" class="sw-ev" text-anchor="end">AI Act</text>
  <circle cx="318" cy="78" r="6" class="sw-phase" /><circle cx="335" cy="78" r="6" class="sw-phase" />
  <text x="345" y="70" class="sw-ev">high-risk</text>
  <!-- Health: EHDS Mar 2027, Mar 2029, Mar 2031 -->
  <circle cx="299" cy="118" r="6" class="sw-phase" /><circle cx="349" cy="118" r="6" class="sw-phase" /><circle cx="399" cy="118" r="6" class="sw-phase" />
  <text x="349" y="108" class="sw-ev" text-anchor="middle">EHDS</text>
  <!-- Cyber: NIS2 Oct 2024; CRA reporting Sep 2026, full Dec 2027 -->
  <circle cx="239" cy="158" r="6" class="sw-bind" /><text x="229" y="150" class="sw-ev" text-anchor="end">NIS2</text>
  <circle cx="287" cy="158" r="6" class="sw-phase" /><circle cx="318" cy="158" r="6" class="sw-phase" /><text x="328" y="150" class="sw-ev">CRA</text>
  <!-- you are here: Nov 2026 -->
  <line x1="291" y1="18" x2="291" y2="172" class="sw-now" />
  <text x="291" y="12" class="sw-now-lab">you are here · Nov 2026</text>
</svg>
<div class="sw-key small"><span class="k-bind"></span> binding <span class="k-phase"></span> phasing in</div>
</div>
<div class="dense">
<strong>Scope traps</strong>

- **AI Act Art 2(6), 2(8)** exclude research-only systems and pre-market research. Deployment and real-world testing are not excluded.
- **CRA:** free, non-commercial open source is outside; public funding alone does not make it commercial (Commission guidance).
- **NIS2:** see slide 12.

</div>
</div>

<table class="bp-matrix compact rulebook">
  <thead>
    <tr><th>Binding now <span class="badge binding">Binding</span></th><th>Phasing in <span class="badge phasing">Phasing in</span></th><th>Not law <span class="badge draft">Draft</span> <span class="badge proposal">Proposal</span></th></tr>
  </thead>
  <tbody>
    <tr>
      <td><ul>
        <li>GDPR</li>
        <li>Open Data Directive, through national law</li>
        <li>AI Act: prohibitions, GPAI, Art 50</li>
        <li>Digital Omnibus on AI, Reg. (EU) 2026/1744, in force 27 Jul 2026 (Art 4 softened, Art 4a added)</li>
        <li>Finnish Secondary Use Act</li>
      </ul></td>
      <td><ul>
        <li>CRA: reporting since 11 Sep 2026, full 11 Dec 2027</li>
        <li>AI Act high-risk: Annex III 2 Dec 2027, Annex I 2 Aug 2028</li>
        <li>EHDS: 26 Mar 2027; secondary use 26 Mar 2029; more categories 26 Mar 2031</li>
      </ul></td>
      <td><ul>
        <li>EDPB draft Guidelines 1/2026 (scientific research)</li>
        <li>EDPB draft Guidelines 02/2026 (anonymisation)</li>
        <li>Digital Omnibus COM(2025)837: Council mandate 21 Oct 2026, Parliament committee vote expected early 2027</li>
      </ul></td>
    </tr>
  </tbody>
</table>

<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng">AI Act</a> · <a href="https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng">AI Omnibus</a> · <a href="https://eur-lex.europa.eu/eli/reg/2025/327/oj">EHDS</a> · <a href="https://eur-lex.europa.eu/eli/reg/2024/2847/oj">CRA</a> · <a href="https://www.opensourceforu.com/2026/07/eu-clarifies-cra-rules-for-non-commercial-open-source/">CRA guidance 2026</a> · <a href="https://www.edpb.europa.eu/system/files/2026-04/edpb_guidelines_202601_scientificresearch_en.pdf">EDPB 1/2026</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026</a> · <a href="https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52025PC0837">COM(2025)837</a> · <a href="https://iapp.org/news/a/eu-member-states-finalize-digital-omnibus-negotiating-stance">Council mandate</a> · <a href="https://www.nicfab.eu/en/posts/digital-omnibus-council/">NicFab 2026</a></div>

<style>
.status { margin-bottom: 0.3rem; }
.swim { width: 100%; height: 140px; }
.rulebook td { width: 33%; }
.slidev-layout .rulebook ul { margin: 0; padding-left: 0.9rem; }
.slidev-layout .rulebook li { font-size: 0.7rem; line-height: 1.2; margin: 0.1rem 0; }
.slidev-layout .rulebook li::before { left: -0.75rem; }
.sw-lanes text { font-size: 12px; font-weight: 600; fill: var(--asc-text); }
.sw-lanes line { stroke: var(--asc-border); stroke-width: 2; }
.sw-years text { font-size: 10px; text-anchor: middle; fill: var(--asc-muted); }
.sw-ev { font-size: 10px; fill: var(--asc-text); }
.sw-bind { fill: var(--asc-night); }
.sw-phase { fill: var(--aalto-blue); stroke: var(--asc-text); stroke-width: 1; }
.sw-now { stroke: var(--aalto-red); stroke-width: 2.5; stroke-dasharray: 5 3; }
.sw-now-lab { font-size: 10px; font-weight: 700; text-anchor: middle; fill: #c0302d; }
.sw-key span { display: inline-block; width: 0.7rem; height: 0.7rem; border-radius: 999px; vertical-align: -0.05em; margin-left: 0.6rem; }
.sw-key .k-bind { background: var(--asc-night); }
.sw-key .k-phase { background: var(--aalto-blue); }
.status th .badge { font-size: 0.5rem; }
</style>

<!--
EU rulebook, November 2026.

CHECK BEFORE PRESENTING
- Digital Omnibus (COM(2025)837) is fast-moving.
- Final text of Reg. (EU) 2026/1744 and EDPB draft 02/2026 read through summaries only: check against the primary texts.
- Swimlane dates are placed by hand from the table; check positions after any date change.
-->

---
layout: end
---

# Five questions before you open, close or upload

<div class="hexq">
  <div class="hx"><span class="hx-n">1</span>Which object is this?</div>
  <div class="hx"><span class="hx-n">2</span>Who could be harmed, by whom, with what means today?</div>
  <div class="hx"><span class="hx-n">3</span>What must stay checkable, and by whom?</div>
  <div class="hx"><span class="hx-n">4</span>Where does it run, and who else can see it?</div>
  <div class="hx"><span class="hx-n">5</span>Is the closure written down and technically enforced?</div>
</div>

Not "how do we stop risky research?" but **"what infrastructure lets people do ambitious work safely and reproducibly?"**

<div class="ai-disclosure">AI use: generative AI tools were used substantially for the literature review behind this deck (substantial use under EC Guidelines v4) and for drafting the slide code. Legal and factual claims were checked on 4 November 2026; claims read only through summaries are listed in the source plan.</div>

<style>
.slidev-layout.end h1 { font-size: 2.3rem !important; margin-bottom: 0.3rem; }
.hexq { display: flex; justify-content: center; gap: 0.35rem; margin: 0.4rem 0 0.6rem; }
.hx { display: flex; flex-direction: column; align-items: center; justify-content: center; width: 138px; height: 152px; padding: 1.3rem 0.9rem; clip-path: polygon(50% 0, 100% 25%, 100% 75%, 50% 100%, 0 75%, 0 25%); background: var(--aalto-blue); color: #000; font-size: 0.78rem; line-height: 1.2; text-align: center; }
.hx:nth-child(even) { background: var(--aalto-yellow); margin-top: 2.2rem; }
.hx-n { font-family: var(--asc-font-serif); font-weight: 700; font-size: 1.3rem; margin-bottom: 0.2rem; }
.slidev-layout.end strong { color: var(--asc-text); }
.ai-disclosure { margin-top: 0.5rem; font-size: 0.6rem; color: var(--asc-muted); max-width: 46rem; margin-left: auto; margin-right: auto; }
</style>

<!--
Discussion prompts:
1. Which parts of your work must be open for real scrutiny?
2. Should approved, secure generative AI be treated as research infrastructure?
3. Who decides when privacy protection reduces accuracy for a small subgroup?

The AI-use disclosure wording is a draft: adjust it to what was actually done.
-->
