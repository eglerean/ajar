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
  Open science with personal data: what researchers can do.
  Source: https://github.com/eglerean/ajar
keywords: open science, research integrity, privacy, GDPR, cybersecurity, AI, Enrico Glerean, https://eglerean.github.io/
layout: cover
class: no-footer
hexText: "OPEN\nCLOSED"
hexSeed: 11
---

###### Open science · Personal data · AI

# As open as possible, as closed as necessary ... in the age of AI

Open science with personal data plus the opportunities and risks that AI can bring: what researchers and support personnel can do

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
Message: integrity pulls research towards open. Privacy pulls it towards closed. AI adds risk on the first side and cybersecurity on the second. You resolve the tension with four moves, made object by object.

About 20 minutes. Audience: non-technical researchers who work with personal data and publish articles.
Status date: legal and factual claims checked on 4 November 2026.
-->

---
layout: image-right
image: /book-secure-ai-personal-data.png
class: fit-image
---

###### About me

# Enrico Glerean, DSc.

**Staff scientist and Data Agent** at Aalto University (background in neuroimaging). I train and support researchers with **handling personal data** (anonymization, secure computing), medical images, clinical trials, **research ethics and research integrity** (AI and new technologies), statistics, and **open science**. I coordinate **LUMI AI Factory trainings** at Aalto University.

**Other affiliations / COI**

- [CodeRefinery](https://coderefinery.org/): Nordic network to teach computational reproducibility
- [Finnish Reproducibility Network](https://www.finnish-rn.org/): national network to raise awareness of reproducibility
- [Support Pool of Experts](https://www.edpb.europa.eu/support-pool-of-experts-spe-programme_en) at the European Data Protection Board: open training materials on personal data, AI and cybersecurity
- Member of the [EU AI Act Advisory Forum](https://digital-strategy.ec.europa.eu/en/policies/ai-advisory-forum)
- Teacher in the [Data Steward training programme](https://www.tuni.fi/en/study-with-us/data-steward), Tampere University

<div class="bio-refs">
<strong>References</strong>
<ol>
<li>Book: <a href="https://www.edpb.europa.eu/documents/support-pool-of-experts/fundamentals-of-secure-ai-systems-with-personal-data_en">Fundamentals of Secure AI Systems with Personal Data</a> (EDPB, 2025)</li>
<li>Slides: <a href="https://github.com/eglerean/genAI_researchintegrity">Generative AI tools and research integrity</a></li>
<li>Slides: <a href="https://eglerean.github.io/posts/nordic-data-stewardship-seminar-2026/">Responsible AI in research: ethics, integrity, compliance</a> (Nordic Data Stewardship Network, 2026)</li>
<li>Slides: <a href="https://zenodo.org/records/18609058">Data available on unreasonable request</a> (Zenodo, 2026)</li>
<li>Slides: <a href="https://eglerean.github.io/posts/fpf-talk/">Talk at the Future of Privacy Forum</a></li>
</ol>
</div>

<style>
.slidev-layout h1 { font-size: 1.8rem !important; margin-bottom: 0.5rem !important; }
.slidev-layout p, .slidev-layout li { font-size: 0.74rem !important; line-height: 1.35 !important; }
.slidev-layout p { margin: 0.4rem 0 !important; }
.slidev-layout ul { margin-top: 0.1rem !important; }
.slidev-layout li { margin: 0.05rem 0 !important; }
.slidev-layout .bio-refs { margin-top: 0.5rem; font-size: 0.64rem; line-height: 1.3; }
.slidev-layout .bio-refs ol { margin: 0.1rem 0 0 1.1rem !important; padding: 0 !important; list-style: decimal; }
.slidev-layout .bio-refs li { font-size: 0.64rem !important; line-height: 1.3 !important; margin: 0 !important; }
</style>

---
layout: default
---

###### The tension

# One tension, two added risks

<div class="tow-wrap"><TugOfWar /></div>

<div class="grid-2">
<div class="card blue">
<h3>Integrity: the ALLEA principles</h3>

- **Reliability** in the design, method, analysis and use of resources
- **Honesty** in developing, reviewing, reporting and communicating research
- **Respect** for colleagues, participants, research subjects, society, ecosystems and the environment
- **Accountability** for research from idea to publication

</div>
<div class="card red">
<h3>Privacy: the 7 principles of privacy by design</h3>

1. Proactive, not reactive
2. Privacy as the default setting
3. Privacy embedded into design
4. Full functionality: positive-sum, not zero-sum
5. End-to-end security across the data life cycle
6. Visibility and transparency
7. Respect for user privacy

</div>
</div>

<div class="ref-bottom"><a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://iapp.org/media/pdf/resource_center/pbd_implement_7found_principles.pdf">Cavoukian 2009</a> · <a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR Art. 25</a>: data protection by design and by default</div>

<style>
.tow-wrap { max-width: 620px; margin: -0.6rem auto 0.6rem; }
.slidev-layout .grid-2 { display: grid; grid-template-columns: minmax(0, 1fr) minmax(0, 1fr); gap: 1rem; }
.slidev-layout .grid-2 .card { padding: 0.6rem 0.9rem; }
.slidev-layout .grid-2 h3 { font-size: 0.95rem !important; margin: 0 0 0.3rem !important; }
.slidev-layout .grid-2 li { font-size: 0.76rem !important; line-height: 1.35 !important; margin: 0.05rem 0 !important; }
.slidev-layout .grid-2 ol { margin: 0 0 0 1.1rem !important; padding: 0 !important; list-style: decimal; }
.slidev-layout .grid-2 ol li::marker { color: #000; font-weight: 700; }
</style>

<!--
This picture returns as the small icon in the top-right corner, with the part we are talking about highlighted.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini :active="['ai', 'integrity']" /></div>

###### The added risks

# AI makes research harder to check

<div class="grid-3-2">
<div>

- **Errors get cheaper.** Papers citing references that do not exist: 1 in 2,828 in 2023, 1 in 277 in early 2026.
- **The same prompt can give different outputs**, so "we used ChatGPT" does not let anyone reconstruct the work.
- **Hiding AI use is an integrity violation** (ALLEA 2023 §3.1).
- **Peer review is exposed too:** authors have hidden instructions in manuscripts to steer AI reviewers.
- **The catch:** prompts and logs make AI use checkable, but they can contain confidential text. That is the tension again.

</div>
<div>
  <div class="flow ai-flow">
    <div class="step"><b>Input</b>your text, data, question</div>
    <div class="arrow">→</div>
    <div class="step ai-tool"><b>AI tool</b><span class="qm">?</span></div>
    <div class="arrow">→</div>
    <div class="step"><b>Output</b>plausible, not checked</div>
  </div>
  <div class="ai-log"><span class="warn">⚠</span><div><b>The log</b>makes the work checkable, but can contain confidential text</div></div>
  <div class="card yellow misconduct"><strong>Generative AI: the ideal misconduct machine?</strong> It always produces text and leaves quality control to the user. More cases in <a href="https://github.com/eglerean/genAI_researchintegrity">AI tools, Research Integrity and Ethics</a>.</div>
</div>
</div>

<div class="ref-bottom"><a href="https://retractionwatch.com/2026/05/07/one-in-277-pubmed-indexed-papers-in-2026-shows-fabricated-references-says-analysis/">Topaz 2026</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Guidelines v4</a> · <a href="https://doi.org/10.48550/arXiv.2602.14349">Cui &amp; Alexander 2026</a> · <a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://asia.nikkei.com/business/technology/artificial-intelligence/positive-review-only-researchers-hide-ai-prompts-in-papers">Nikkei 2025</a></div>

<style>
.slidev-layout .ai-flow .step { text-align: center; font-size: 0.72rem; }
.slidev-layout .ai-flow .ai-tool { background: var(--asc-night); border-color: var(--asc-night); color: var(--asc-paper); }
.ai-flow .qm { display: block; font-family: var(--asc-font-serif); font-size: 1.8rem; font-weight: 700; line-height: 1; color: var(--aalto-yellow); }
.ai-log { display: flex; gap: 0.5rem; align-items: center; margin: 0.4rem 20% 0.8rem; padding: 0.35rem 0.6rem; border: 2px dashed var(--aalto-orange); border-radius: var(--asc-radius-md); font-size: 0.72rem; line-height: 1.2; }
.ai-log b { display: block; font-family: var(--asc-font-serif); font-size: 0.82rem; }
.ai-log .warn { font-size: 1.4rem; color: var(--aalto-orange); }
.misconduct { font-size: 0.72rem; line-height: 1.25; }
</style>

<!--
CHECK BEFORE PRESENTING
- Topaz counts references to papers that do not exist. It does not prove AI caused each one, and 91% of affected papers had only one or two.

The yellow card reuses "Generative AI: the ideal misconduct machine?" from the genAI_researchintegrity deck.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini :active="['cyber', 'privacy']" /></div>

###### The added risks

# Closed data is only as safe as its security

<div class="timeline">
  <div class="tl-line"></div>
  <div class="tl-item">
    <div class="tl-year">2020</div>
    <div class="tl-card"><span class="kind attack">Attack</span><b>Vastaamo</b><br>Therapy records stolen, patients blackmailed.</div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2023</div>
    <div class="tl-card"><span class="kind attack">Attack</span><b>University of Manchester</b><br>Research data on about 1.1 million NHS patients affected.</div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2023</div>
    <div class="tl-card"><span class="kind mistake">Mistake</span><b>Microsoft AI research</b><br>A link for sharing AI models also opened 38 TB of other data.</div>
  </div>
  <div class="tl-item">
    <div class="tl-year">2026</div>
    <div class="tl-card"><span class="kind misuse">Misuse</span><b>UK Biobank</b><br>No hack: approved institutions broke the rules.</div>
  </div>
</div>

<div class="grid-3-2">
  <div class="card">
    <h3>AI helps the attacker</h3>
    <p>6 of 24 public interview transcripts were linked to publications, at under $0.50 each. Participants had agreed to release, so this shows a capability, not documented harm. <span class="badge preprint">Preprint</span></p>
  </div>
  <div class="card dark rules">
    <p>A contract states the rule. <strong>Only a technical control enforces it.</strong></p>
  </div>
</div>

<div class="ref-bottom"><a href="https://cyberscoop.com/finnish-psychotherapy-data-breach-vastaamo/">Vastaamo 2020</a> · <a href="https://www.govinfosecurity.com/trauma-terrorist-victim-data-breached-in-university-attack-a-22409">Manchester 2023</a> · <a href="https://wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers">Wiz 2023</a> · <a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UKB Oversight 2026</a> · <a href="https://arxiv.org/abs/2601.05918">Li 2026</a></div>

<style>
.timeline { position: relative; display: grid; grid-template-columns: repeat(4, minmax(0, 1fr)); gap: 0.6rem; margin-bottom: 1rem; }
.tl-line { position: absolute !important; left: 0; right: 0; top: 0.75rem; height: 3px; background: var(--asc-border); }
.tl-year { position: relative; display: inline-block; padding: 0.05rem 0.6rem; border-radius: 999px; background: var(--asc-night); color: var(--asc-paper); font-weight: 700; font-size: 0.8rem; margin-bottom: 0.35rem; }
.tl-card { padding: 0.5rem 0.65rem; border: 2px solid var(--asc-border); border-radius: var(--asc-radius-md); background: var(--asc-surface); font-size: 0.8rem; line-height: 1.25; }
.tl-card b { font-family: var(--asc-font-serif); font-size: 0.9rem; }
.kind { display: block; width: fit-content; margin-bottom: 0.3rem; padding: 0.05rem 0.5rem; border-radius: 999px; font-size: 0.6rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.04em; color: #000; }
.kind.attack { background: var(--aalto-red); }
.kind.mistake { background: var(--aalto-orange); }
.kind.misuse { background: var(--aalto-darkyellow); }
.rules { display: flex; align-items: center; font-size: 1.15rem; }
</style>

<!--
CHECK BEFORE PRESENTING
- Li 2026 is a single-author preprint with manual verification.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini active="decision" /></div>

###### Move 1 of 4

# Decide per object, and write down why

<div>

- A study is many objects. Open or closed applies to **each one**, not to the study. For each object, record the **access level**, the **reason** and the **route** to access.
- FAIR does not mean open: access can require login and approval, while the description stays public. "On reasonable request" gives no reason and no route.

</div>

<table class="bp-matrix compact objects">
  <thead>
    <tr><th>Object <span class="rc-tag">running case: 80 interviews</span></th><th>Level</th><th>Reason</th><th>Route</th></tr>
  </thead>
  <tbody>
    <tr><td>Protocol, interview guide</td><td class="bp-green">Public</td><td></td><td>Repository with DOI</td></tr>
    <tr><td>Codebook, data dictionary</td><td class="bp-green">Public</td><td>Check example quotes first</td><td>Repository</td></tr>
    <tr><td>Analysis code</td><td class="bp-green">Public</td><td>Check for embedded data first</td><td>Repository</td></tr>
    <tr><td>Summary tables</td><td class="bp-green">Public</td><td>Merge very small groups</td><td>Article</td></tr>
    <tr><td>AI workflow description</td><td class="bp-green">Public</td><td></td><td>Supplement</td></tr>
    <tr><td>AI prompts and logs</td><td class="bp-orange">Controlled</td><td>Contain interview text</td><td>Audit request</td></tr>
    <tr><td>Transcripts</td><td class="bp-orange">Controlled</td><td>Participants could be recognised</td><td>Data access committee, agreement, secure environment</td></tr>
    <tr><td>Key linking codes to names</td><td class="bp-grey">Not shared</td><td>Identifies everyone</td><td>None</td></tr>
  </tbody>
</table>

<div class="ref-bottom"><a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> (§2.5, §3.1) · <a href="https://eur-lex.europa.eu/eli/dir/2019/1024/oj">Open Data Directive</a> · <a href="https://rea.ec.europa.eu/open-science_en">Horizon Europe</a> · <a href="https://tsv.fi/fi/palvelut/linjauslouhi/index.php/Aineistot/en">FI policy 2026–2030</a> · <a href="https://doi.org/10.1038/sdata.2016.18">Wilkinson 2016</a> · <a href="https://journals.sagepub.com/doi/10.1177/25152459251336130">van Ravenzwaaij 2025</a></div>

<style>
.objects td:first-child { width: 28%; font-weight: 600; }
.objects td:nth-child(2) { width: 12%; text-align: center; font-weight: 600; }
.rc-tag { margin-left: 0.4rem; padding: 0 0.45rem; border-radius: 999px; background: var(--aalto-yellow); color: #000; font-size: 0.6rem; font-weight: 600; text-transform: uppercase; letter-spacing: 0.04em; }
</style>

<!--
The table is meant to be copied into a data management plan.
Running case (fictional): 80 interviews on workplace harassment.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini active="privacy" /></div>

###### Move 2 of 4

# Set the level by who could identify whom

<div>

- **Pseudonymised data is still personal data** for anyone who can use the key. "Synthetic" says how data were made, not that they are safe.
- **The same data can be personal for one party and not for another** (*EDPS v SRB*). Public release is the hard case: anyone, with any tool.
- **Three checks:** can someone be singled out, linked to other data, or have something inferred about them? <span class="badge draft">Draft</span>
- **Look at the most exposed person, not the average.** In medical AI, attacks looked close to guessing overall, yet were near-perfect for some patients.
- **Promise only what you can keep.** Do not write "anonymous" for a small interview study, and recheck as tools improve.

</div>

<div class="grid-3 viewers">
  <div class="card dark"><div class="vw-who">Key holder</div><div class="vw-verdict">Personal data</div></div>
  <div class="card yellow"><div class="vw-who">Recipient with no realistic means</div><div class="vw-verdict">Assess</div></div>
  <div class="card red"><div class="vw-who">Public download</div><div class="vw-verdict">Assume anyone</div></div>
</div>

<div class="running-case"><strong>Running case</strong> The realistic threat is a colleague who recognises a story.</div>

<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> (Art 4(5), Recital 26) · <a href="https://www.fieldfisher.com/en-be/locations/belgium/insights/edps-v-srb-cjeu%e2%80%99s-contextual-approach-to-pseudonym">EDPS v SRB</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026 (draft)</a> · <a href="https://doi.org/10.1038/s41586-026-10688-0">Knolle 2026</a></div>

<style>
.viewers { margin: 0.5rem 0; }
.viewers .card { padding: 0.5rem 0.8rem; }
.vw-who { font-size: 0.72rem; text-transform: uppercase; letter-spacing: 0.05em; opacity: 0.8; }
.vw-verdict { font-family: var(--asc-font-serif); font-weight: 700; font-size: 1.2rem; }
</style>

<!--
CHECK BEFORE PRESENTING
- Draft Guidelines 02/2026 were read through law-firm summaries, and Knolle 2026 through its abstract and press release. Check both against the originals.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini :active="['ai', 'cyber']" /></div>

###### Move 3 of 4

# Match the tool to the data

<div class="grid-2-3">
<div>

- **Ask where it runs, not which brand:** who receives the data, where they are stored, how long they are kept, whether they train the model, who can look.
- **Keep the full AI log restricted.** Publish a clean workflow: tool and version, task, input type, what you accepted, who checked.
- **Never give one AI agent** private data, untrusted content and a way to send data out. Remove one, for example the internet connection.

</div>
<div>
  <div class="ladder">
    <div class="ld-row" style="--c: var(--aalto-green)"><span class="ld-class">Public</span><span class="ld-arrow">→</span><span class="ld-tool">Any tool</span></div>
    <div class="ld-row" style="--c: var(--aalto-darkyellow)"><span class="ld-class">Internal</span><span class="ld-arrow">→</span><span class="ld-tool">Approved tools</span></div>
    <div class="ld-row" style="--c: var(--aalto-orange)"><span class="ld-class">Confidential</span><span class="ld-arrow">→</span><span class="ld-tool">Contractual guarantees or local models</span></div>
    <div class="ld-row" style="--c: var(--aalto-red)"><span class="ld-class">Secret</span><span class="ld-arrow">→</span><span class="ld-tool">Local tools inside a secure environment</span></div>
  </div>
  <div class="logstrip">
    <span class="ls-box ls-full">Full AI log <em>restricted</em></span><span class="ls-arrow">→</span><span class="ls-filter">filter</span><span class="ls-arrow">→</span><span class="ls-box ls-pub">Public workflow <em>with the paper</em></span>
  </div>
  <div class="running-case"><strong>Running case</strong> Pseudonymised transcripts do not go into a consumer chatbot.</div>
</div>
</div>

<div class="ref-bottom"><a href="https://www.aalto.fi/en/research-art/best-practices-for-ai-use-in-research-work">Aalto best practices</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Guidelines v4</a> · <a href="https://tenk.fi/sites/default/files/2026-06/Artificial%20Intelligence%20in%20Research.%20TENK%27s%20Recommendation%202026.pdf">TENK 2026</a> · <a href="https://doi.org/10.1186/s41073-026-00245-8">Cwik 2026</a> · <a href="https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/">Willison 2025</a></div>

<style>
.ladder { display: flex; flex-direction: column; gap: 0.3rem; }
.ld-row { display: grid; grid-template-columns: 7.5rem auto 1fr; align-items: center; gap: 0.6rem; padding: 0.4rem 0.8rem; border-left: 8px solid var(--c); border-radius: var(--asc-radius-sm); background: color-mix(in srgb, var(--c) 30%, transparent); font-size: 0.9rem; }
.ld-class { font-family: var(--asc-font-serif); font-weight: 700; }
.ld-arrow { color: var(--asc-muted); }
.logstrip { display: flex; align-items: center; gap: 0.4rem; margin: 0.7rem 0; font-size: 0.78rem; }
.ls-box { flex: 1; padding: 0.35rem 0.6rem; border-radius: var(--asc-radius-md); border: 2px solid; font-weight: 600; }
.ls-box em { display: block; font-weight: 400; font-size: 0.65rem; opacity: 0.8; }
.ls-full { border-color: var(--aalto-red); background: color-mix(in srgb, var(--aalto-red) 18%, transparent); }
.ls-pub { border-color: var(--aalto-green); background: color-mix(in srgb, var(--aalto-green) 18%, transparent); }
.ls-filter { padding: 0.2rem 0.5rem; border-radius: 999px; background: var(--asc-night); color: var(--asc-paper); font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.05em; }
.ls-arrow { color: var(--asc-muted); }
</style>

<!--
CHECK BEFORE PRESENTING
- The four classes come from the public aalto.fi page; the adaptation of the Finnish classification model is still in progress.
- Cwik 2026: only the bibliographic record was confirmed.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini active="integrity" /></div>

###### Move 4 of 4

# Keep closed work checkable

<div class="verify">
  <div class="flow">
    <div class="step v-pub"><b>Public code + software setup</b></div>
    <div class="arrow">→</div>
    <div class="step v-sec"><b>Secure environment</b>fixed data version</div>
    <div class="arrow">→</div>
    <div class="step v-sec"><b>Run</b></div>
    <div class="arrow">→</div>
    <div class="step v-check"><b>Output check</b></div>
    <div class="arrow">→</div>
    <div class="step v-pub"><b>Public result</b></div>
  </div>
  <div class="v-second"><span>↳ second path: a <strong>qualified verifier</strong> reruns the same code on the same data version inside the secure environment</span></div>
</div>

<div>

- **Sharing code is not enough.** One team ran the same scripts unchanged in a second secure environment and still hit problems with how the data had been prepared.
- **Publish what you can:** code, data dictionary, data version, software setup, access route.
- **Say who can verify the work and how**, for example a qualified person rerunning it inside the secure environment.
- **Plan for time.** Controlled clinical trial data took 270 days on average to access, open data 8.
- **This is the EU direction.** From 2029, under the European Health Data Space: permit, secure environment, only non-personal outputs leave, results public within 18 months.

</div>

<div class="ref-bottom"><a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12273930/">Williams 2025</a> · <a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC12647387/">Rodriguez 2025</a> · <a href="https://eur-lex.europa.eu/eli/reg/2025/327/oj">EHDS</a> (<a href="https://streamlex.eu/articles/ehds-en-art-61/">Art 61</a>) · <a href="https://findata.fi/en/permits/data-permits/">Findata</a></div>

<style>
.verify { margin-bottom: 0.5rem; }
.slidev-layout .verify .step { font-size: 0.72rem; text-align: center; display: flex; flex-direction: column; justify-content: center; }
.slidev-layout .verify .step b { font-size: 0.85rem; }
.slidev-layout .verify .v-pub { border-color: var(--aalto-green); }
.slidev-layout .verify .v-sec { background: var(--asc-night); border-color: var(--asc-night); color: var(--asc-paper); }
.slidev-layout .verify .v-check { border-color: var(--aalto-orange); background: color-mix(in srgb, var(--aalto-orange) 25%, transparent); }
.v-second { margin: 0.3rem 0 0 18%; font-size: 0.75rem; color: var(--asc-muted); }
</style>

---
layout: end
---

# Four questions before you open, close or upload

<div class="close-grid">
<svg class="door4" viewBox="-10 0 250 192" role="img" aria-label="A fourth door, ajar: a reason written on the door, a route to enter, and a lock that works">
  <!-- light through the gap -->
  <polygon points="70,20 130,20 130,170 70,170" class="d4-gap" />
  <!-- path on the floor -->
  <polygon points="80,170 120,170 150,188 50,188" class="d4-path" />
  <rect x="65" y="15" width="70" height="157" rx="4" class="d4-frame" />
  <!-- door leaf, slightly open -->
  <polygon points="70,20 112,28 112,162 70,170" class="d4-leaf" />
  <!-- sign with the reason -->
  <rect x="76" y="58" width="30" height="20" rx="2" class="d4-sign" />
  <line x1="80" y1="64" x2="102" y2="65" class="d4-text" /><line x1="80" y1="70" x2="98" y2="71" class="d4-text" />
  <!-- working lock on the frame -->
  <rect x="122" y="88" width="16" height="13" rx="2" class="d4-lock" />
  <path d="M125.5 88 v-5 a4.5 4.5 0 0 1 9 0 v5" class="d4-shackle" />
  <!-- labels -->
  <text x="40" y="70" class="d4-lab" text-anchor="end">reason</text>
  <line x1="44" y1="67" x2="74" y2="67" class="d4-lead" />
  <text x="160" y="96" class="d4-lab" text-anchor="start">lock</text>
  <text x="160" y="110" class="d4-lab" text-anchor="start">that works</text>
  <text x="100" y="186" class="d4-lab d4-route">route</text>
</svg>
<ol class="q4">
  <li>Which object is this, and why is it closed?</li>
  <li>Who could identify whom, with what means today?</li>
  <li>Where does it run, and who else can see it?</li>
  <li>How can someone still check it?</li>
</ol>
</div>

Institutions owe researchers the **infrastructure that makes this the easy route**.

<div class="ai-disclosure">AI use: generative AI tools were used substantially for the literature review behind this deck (substantial use under EC Guidelines v4) and for drafting the slide code. Legal and factual claims were checked on 4 November 2026; claims read only through summaries are listed in the source plan.</div>

<style>
.slidev-layout.end h1 { font-size: 2.2rem !important; margin-bottom: 0.6rem; }
.close-grid { display: grid; grid-template-columns: 250px minmax(0, 1fr); gap: 1.5rem; align-items: center; text-align: left; max-width: 46rem; margin: 0 auto 0.8rem; }
.door4 { width: 250px; height: 192px; }
.d4-gap { fill: #fff6c8; }
.d4-path { fill: color-mix(in srgb, var(--aalto-yellow) 45%, transparent); }
.d4-frame { fill: none; stroke: var(--asc-text); stroke-width: 3; }
.d4-leaf { fill: #b98a52; stroke: var(--asc-text); stroke-width: 2; }
.d4-sign { fill: var(--aalto-blue); }
.d4-text { stroke: #000; stroke-width: 1.5; }
.d4-lock { fill: var(--aalto-green); stroke: var(--asc-text); stroke-width: 1.5; }
.d4-shackle { fill: none; stroke: var(--asc-text); stroke-width: 2; }
.d4-lab { font-size: 13px; font-weight: 600; fill: var(--asc-text); }
.d4-route { text-anchor: middle; fill: #000; }
.d4-lead { stroke: var(--asc-muted); stroke-width: 1; }
.slidev-layout .q4 { margin: 0; padding-left: 1.5rem; }
.slidev-layout .q4 li { font-size: 1.1rem; line-height: 1.3; margin: 0.45rem 0; color: var(--asc-text); }
.slidev-layout.end p { font-size: 1.1rem; }
.slidev-layout.end strong { color: var(--asc-text); }
.ai-disclosure { margin: 0.6rem auto 0; font-size: 0.6rem; color: var(--asc-muted); max-width: 46rem; }
</style>

<!--
The fourth door, ajar, answers the three doors on slide 2: a reason on the door, a route to enter, and a lock that works.

The AI-use disclosure wording is a draft: adjust it to what was actually done.
-->

---
layout: default
---

###### Backup

# Techniques move risk, they do not remove it

<table class="bp-matrix pet">
  <thead>
    <tr><th>Technique</th><th>Gives you</th><th></th><th>Risk moves to</th></tr>
  </thead>
  <tbody>
    <tr><td><strong>Pseudonymisation</strong></td><td>No names in working files</td><td class="pet-arrow">→</td><td class="bp-orange">Anyone who can link; stories still identify</td></tr>
    <tr><td><strong>Synthetic data</strong></td><td>Teaching, software tests, previews</td><td class="pet-arrow">→</td><td class="bp-orange">Lost patterns, leftover disclosure risk</td></tr>
    <tr><td><strong>Differential privacy</strong></td><td>A formal limit on one person's influence</td><td class="pet-arrow">→</td><td class="bp-orange">Accuracy, especially for small groups</td></tr>
    <tr><td><strong>Federated learning</strong></td><td>Raw data stay at each site</td><td class="pet-arrow">→</td><td class="bp-orange">Updates can leak; site differences cost accuracy</td></tr>
    <tr><td><strong>Secure environment</strong></td><td>Control of who, where and what leaves</td><td class="pet-arrow">→</td><td class="bp-orange">Cost, usability, reproducibility</td></tr>
  </tbody>
</table>

<div class="ref-bottom"><a href="https://pubmed.ncbi.nlm.nih.gov/40343279/">Adams 2025</a> · <a href="https://pubmed.ncbi.nlm.nih.gov/41032725/">Demuth 2025</a> · <a href="https://www.sciencedirect.com/science/article/pii/S2773186325002257">Federated learning review 2025</a> · <a href="https://lumi-ai-factory.eu/articles/international-data-protection-day/">Honkela interview 2026</a></div>

<style>
.pet td:first-child { width: 22%; }
.pet .pet-arrow { width: 2.5rem; text-align: center; font-size: 1.3rem; color: var(--aalto-orange); }
</style>

<!--
CHECK BEFORE PRESENTING
- Adams, Demuth and the federated learning review were taken from the report, not opened.
-->

---
layout: default
---

###### Backup

# Check the status before you cite the rule

<table class="bp-matrix compact rulebook">
  <thead>
    <tr><th>Binding now</th><th>Phasing in</th><th>Not law <span class="badge draft">Draft</span> <span class="badge proposal">Proposal</span></th></tr>
  </thead>
  <tbody>
    <tr>
      <td><ul>
        <li>GDPR</li>
        <li>Open Data Directive, through national law</li>
        <li>AI Act: prohibitions, GPAI, Art 50</li>
        <li>Digital Omnibus on AI, Reg. (EU) 2026/1744, in force 27 Jul 2026</li>
        <li>Finnish Secondary Use Act</li>
      </ul></td>
      <td><ul>
        <li>CRA: reporting since 11 Sep 2026, full 11 Dec 2027</li>
        <li>AI Act high-risk: Annex III 2 Dec 2027, Annex I 2 Aug 2028</li>
        <li>EHDS: 26 Mar 2027; secondary use 26 Mar 2029; more categories 26 Mar 2031</li>
      </ul></td>
      <td><ul>
        <li>EDPB draft Guidelines 1/2026 (research)</li>
        <li>EDPB draft Guidelines 02/2026 (anonymisation)</li>
        <li>Digital Omnibus COM(2025)837: Council mandate 21 Oct 2026, Parliament committee vote expected early 2027</li>
      </ul></td>
    </tr>
  </tbody>
</table>

<div class="card dark scope">
<strong>Scope trap:</strong> the AI Act excludes research-only systems and pre-market research (Art 2(6), 2(8)). Deployment and real-world testing are not excluded.
</div>

<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng">AI Act</a> · <a href="https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng">AI Omnibus</a> · <a href="https://eur-lex.europa.eu/eli/reg/2025/327/oj">EHDS</a> · <a href="https://eur-lex.europa.eu/eli/reg/2024/2847/oj">CRA</a> · <a href="https://www.edpb.europa.eu/system/files/2026-04/edpb_guidelines_202601_scientificresearch_en.pdf">EDPB 1/2026</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026</a> · <a href="https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52025PC0837">COM(2025)837</a> · <a href="https://iapp.org/news/a/eu-member-states-finalize-digital-omnibus-negotiating-stance">Council mandate</a> · <a href="https://www.nicfab.eu/en/posts/digital-omnibus-council/">NicFab 2026</a></div>

<style>
.rulebook { margin-bottom: 0.8rem; }
.rulebook td { width: 33%; }
.slidev-layout .rulebook ul { margin: 0; padding-left: 0.9rem; }
.slidev-layout .rulebook li { font-size: 0.82rem; line-height: 1.25; margin: 0.2rem 0; }
.slidev-layout .rulebook li::before { left: -0.75rem; }
</style>

<!--
EU rulebook, November 2026.

CHECK BEFORE PRESENTING
- Reg. (EU) 2026/1744 was read through summaries, and the Digital Omnibus is moving fast.
-->

---
layout: default
---

###### The tension

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
    <p>"Available on request": of 1,792 authors asked, 123 shared their data (6.8%).</p>
  </div>
  <div class="card">
    <svg class="door" viewBox="0 0 120 90" aria-label="A wide open door, nobody watching">
      <rect x="35" y="8" width="50" height="78" rx="3" class="door-frame" />
      <rect x="40" y="13" width="40" height="73" class="door-gap" />
      <polygon points="40,13 18,4 18,95 40,86" class="door-leaf" />
    </svg>
    <h3>Open by accident</h3>
    <p>UK Biobank data ended up in public code repositories, inside code that journals often ask authors to publish.</p>
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
    <p>April 2026: data on about 500,000 volunteers listed for sale. No hack: approved institutions broke the rules.</p>
  </div>
</div>

<div class="ref-bottom"><a href="https://pubmed.ncbi.nlm.nih.gov/35654271">Gabelica 2022</a> · <a href="https://www.ukbiobank.ac.uk/?p=63092">UK Biobank statement 2026</a> · <a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UKB Oversight Committee 2026</a> · <a href="https://www.theregister.com/2026/04/23/500k_biobank_volunteers_data_listed/">The Register 2026</a></div>

<style>
.door { display: block; width: 130px; height: 98px; margin: 0.4rem auto 0.6rem; }
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

<!--
Each failure has a different owner: integrity, privacy, security. The fourth door, at the end, answers all three.
-->
