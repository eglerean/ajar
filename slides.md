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
layout: section
color: dark
hexText: "AI?"
class: title-middle
---

# What is AI?


---
layout: three-cols
---

::header::
# What is AI in research? Topic, method, tool

<div class="ref-line">Reference: <a href="https://www.aalto.fi/en/research-art/best-practices-for-ai-use-in-research-work">Best practices for AI use in research work (Aalto.fi)</a></div>

::left::

### AI as a **topic**

AI is what is being studied.

- A new ML model or architecture
- A new algorithm for training
- How people interact with AI chatbots

::center::

### AI as a **method**

AI is how the data are analysed.

- A deep neural network that classifies tissue in cancer imaging data
- A scikit-learn model in the analysis of a dataset

::right::

### AI as a **tool**

AI is something that helps with the work.

- Brainstorming with a chatbot
- A coding agent writing analysis scripts
- An AI assistant helping to fill in a data management plan

<p class="small">Invisible AI: in word processors, search engines, translation, transcription tools, automatic meeting note-takers.</p>



---
layout: default
---

# Generative AI and Research Integrity

<div class="ref-line">Figure adapted from Glerean (2025) <a href="https://www.edpb.europa.eu/our-work-tools/our-documents/support-pool-experts-projects/fundamentals-secure-ai-systems-personal_en">“Fundamentals of secure AI systems with personal data”</a>, European Data Protection Board</div>

<p>For simplicity we focus on <strong>generative AI systems</strong> that use <strong>General Purpose AI models</strong> such as <strong>Large Language Models</strong> that can be used in your research work,  including <strong>agentic AI</strong> systems.</p>

<div class="grid-2-3">
  <div class="card">
    <h3>Generating one modality from another</h3>
    <ul>
      <li>Text → Text</li>
      <li>Text → Code</li>
      <li>Speech → Text</li>
      <li>Text → Speech</li>
      <li>Text → Image</li>
      <li>Image → Text</li>
      <li>…</li>
    </ul>
  </div>
  <div class="card dark ai-sys-diagram">
    <div class="asd-io-wrap asd-in">
      <div class="asd-io"><div class="asd-label">Data &amp; Input</div></div>
      <div class="asd-sample small">“Translate this email from English to Finnish: Hi Annukka, the AI lecture of our…”</div>
    </div>
    <div class="asd-arrow asd-in">→</div>
    <div class="asd-system">
      <div class="asd-label">AI system</div>
      <div class="asd-sub">e.g. a chatbot</div>
      <div class="asd-model">
        <div class="asd-label">AI model</div>
        <div class="asd-sub">e.g. a Large Language Model</div>
      </div>
    </div>
    <div class="asd-io-wrap asd-out">
      <div class="asd-io"><div class="asd-label">Outputs</div></div>
      <div class="asd-sample small">“Hei Annukka, tutkimusetiikan kurssimme tekoälyluento on…”</div>
    </div>
    <div class="asd-arrow asd-out">←</div>
  </div>
</div>

<style>
/* Dark box: inputs (top) go into the AI system, which wraps the AI model; outputs (bottom) come back out on the same side.
   Same look as the agent diagram (Harness and Model boxes) */
.ai-sys-diagram { display: grid; grid-template-columns: minmax(0, 1fr) auto minmax(0, 1fr); grid-template-rows: 1fr 1fr; gap: 0.5rem 0.6rem; align-items: center; }
.ai-sys-diagram .asd-label { font-family: var(--asc-font-serif); font-weight: 600; font-size: 1.1rem; }
.ai-sys-diagram .asd-sub { font-size: 0.8rem; opacity: 0.8; }
.asd-in { grid-row: 1; }
.asd-out { grid-row: 2; }
/* Example prompt and output under the two boxes, in small monospace text */
.asd-io-wrap { grid-column: 1; }
.asd-sample { margin-top: 0.4rem; font-family: var(--asc-font-mono); opacity: 0.85; }
.asd-io { padding: 0.8rem 0.9rem; text-align: center; background: var(--asc-night-raised); border: 1px solid rgba(250, 249, 245, 0.3); border-radius: var(--asc-radius-md); }
.asd-arrow { grid-column: 2; font-size: 1.6rem; line-height: 1; color: var(--asc-clay); }
.asd-system { grid-column: 3; grid-row: 1 / span 2; align-self: stretch; display: flex; flex-direction: column; padding: 0.8rem 1rem 1rem; border: 2px solid var(--asc-clay); border-radius: var(--asc-radius-lg); }
.asd-system .asd-model { flex: 1; margin-top: 0.6rem; display: flex; flex-direction: column; justify-content: center; padding: 1rem 0.9rem; text-align: center; background: var(--asc-clay); color: var(--asc-ink); border-radius: var(--asc-radius-md); }
.asd-model .asd-sub { opacity: 0.85; }
</style>

---
layout: default
color: dark
---

# What is an AI agent?

<div class="grid-2-3">
<div>
The four elements of an AI agent: <strong>a) goal complexity, b) environmental complexity, c) adaptability, d) independent execution. </strong> (<a href="https://doi.org/10.1787/396cf758-en%20">OECD 2026</a>).

An AI agent pairs the model with more components so that it can **take real actions**.

- **The model**, the "intelligence box": the LLM itself.
- **The scaffolding**, between the two: system prompts, tool descriptions, and the rules for how context is assembled and formatted before it reaches the model.
- **The harness**, the "body": the code around the model that calls it, carries out whatever it asks for, and decides when the task is done.

</div>
<div>
<div class="agent-diagram">
  <div class="ad-harness">
    <div class="ad-label">Harness · the body</div>
    <div class="ad-sub">calls the model · runs its actions · decides when done</div>
    <div class="ad-scaffold">
      <div class="ad-label">Scaffolding</div>
      <div class="ad-sub">system prompt · tool descriptions · context assembly</div>
      <div class="ad-model">
        <div class="ad-label">Model</div>
        <div class="ad-sub">the LLM · the intelligence box</div>
      </div>
    </div>
  </div>
  <div class="ad-bottom">
    <div class="ad-arrows">⇅</div>
    <div></div>
    <div class="ad-arrows">⇅</div>
    <div class="ad-env">
      <div class="ad-label">Environment</div>
      <div class="ad-chips"><span>files</span><span>shell</span><span>Slurm</span><span>APIs</span><span>web</span><span>Git</span><span>databases</span><span>MCP</span><span>emails / chat</span></div>
    </div>
    <div class="ad-arrows ad-side">⇄</div>
    <div class="ad-subs">
      <div class="ad-subagent"><div class="ad-label">Sub-agent</div></div>
      <div class="ad-subagent"><div class="ad-label">Sub-agent</div></div>
    </div>
  </div>
</div>
<div class="ad-source">Adapted from Hugging Face, <a href="https://huggingface.co/blog/agent-glossary">"Harness, Scaffold, and the AI Agent Terms Worth Getting Right"</a>, 2026</div>
</div>
</div>

<style>
.agent-diagram { display: flex; flex-direction: column; align-items: stretch; gap: 0.4rem; font-size: 0.8rem; }
.agent-diagram .ad-label { font-family: var(--asc-font-serif); font-weight: 600; font-size: 1rem; }
.agent-diagram .ad-sub { opacity: 0.75; font-size: 0.72rem; margin-bottom: 0.5rem; }
.ad-harness { border: 2px solid var(--asc-clay); border-radius: var(--asc-radius-lg); padding: 0.8rem 1rem; }
.ad-scaffold { border: 1.5px dashed rgba(250, 249, 245, 0.45); border-radius: var(--asc-radius-md); padding: 0.7rem 0.9rem; background: var(--asc-night-raised); }
.ad-model { background: var(--asc-clay); color: var(--asc-ink); border-radius: var(--asc-radius-md); padding: 0.6rem 0.9rem; }
.ad-model .ad-sub { margin-bottom: 0; opacity: 0.85; }
.ad-arrows { text-align: center; font-size: 1.4rem; line-height: 1; color: var(--asc-clay); }
/* Bottom row: Environment (half the Harness width) ⇄ two sub-agents; row above holds the ⇅ to the Harness */
.ad-bottom { display: grid; grid-template-columns: 1fr auto 1fr; gap: 0.4rem 0.5rem; align-items: stretch; }
.ad-side { align-self: center; }
.ad-subs { display: flex; gap: 0.5rem; }
.ad-subagent { flex: 1; display: flex; align-items: center; justify-content: center; text-align: center; border: 2px solid var(--asc-clay); border-radius: var(--asc-radius-md); padding: 0.55rem 0.5rem; }
.ad-env { border: 1px solid rgba(250, 249, 245, 0.3); border-radius: var(--asc-radius-md); padding: 0.55rem 0.9rem; display: flex; flex-direction: column; align-items: flex-start; gap: 0.35rem; }
.ad-chips { display: flex; flex-wrap: wrap; gap: 0.35rem; }
.ad-chips span { background: rgba(250, 249, 245, 0.12); border-radius: 999px; padding: 0.1rem 0.6rem; font-size: 0.72rem; }
.ad-source { font-size: 0.65rem; opacity: 0.7; margin-top: 0.6rem; text-align: right; }
</style>



---
layout: section
color: dark
hexText: "OPEN?\nCLOSED?"
class: title-middle
---

# The tension
## Open science versus data privacy

---
layout: default
---

# One tension, many added risks

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

# Generative AI: the epistemic risks

<div class="grid-3-2">
<div>

- **The ideal misconduct machine?** Generative AI always produces text and leaves quality control to the user. Unchecked output can turn into **fabrication, falsification or plagiarism**, and **hiding AI use is itself an integrity violation**, listed next to them (ALLEA 2023 §3.1).
- **Errors get cheaper.** Papers citing references that do not exist: 1 in 2,828 in 2023, 1 in 277 in early 2026.
- **The same prompt can give different outputs**, so "we used ChatGPT" does not let anyone reconstruct the work.
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
</div>
</div>

<div class="ref-bottom"><a href="https://retractionwatch.com/2026/05/07/one-in-277-pubmed-indexed-papers-in-2026-shows-fabricated-references-says-analysis/">Topaz 2026</a> · <a href="https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en">EC Guidelines v4</a> · <a href="https://doi.org/10.48550/arXiv.2602.14349">Cui &amp; Alexander 2026</a> · <a href="https://doi.org/10.26356/ECOC">ALLEA 2023</a> · <a href="https://asia.nikkei.com/business/technology/artificial-intelligence/positive-review-only-researchers-hide-ai-prompts-in-papers">Nikkei 2025</a> · More cases: <a href="https://github.com/eglerean/genAI_researchintegrity">AI tools, Research Integrity and Ethics</a></div>

<style>
.slidev-layout .ai-flow .step { text-align: center; font-size: 0.72rem; }
.slidev-layout .ai-flow .ai-tool { background: var(--asc-night); border-color: var(--asc-night); color: var(--asc-paper); }
.ai-flow .qm { display: block; font-family: var(--asc-font-serif); font-size: 1.8rem; font-weight: 700; line-height: 1; color: var(--aalto-yellow); }
.ai-log { display: flex; gap: 0.5rem; align-items: center; margin: 0.4rem 20% 0.8rem; padding: 0.35rem 0.6rem; border: 2px dashed var(--aalto-orange); border-radius: var(--asc-radius-md); font-size: 0.72rem; line-height: 1.2; }
.ai-log b { display: block; font-family: var(--asc-font-serif); font-size: 0.82rem; }
.ai-log .warn { font-size: 1.4rem; color: var(--aalto-orange); }
</style>

<!--
CHECK BEFORE PRESENTING
- Topaz counts references to papers that do not exist. It does not prove AI caused each one, and 91% of affected papers had only one or two.

The first bullet reuses "Generative AI: the ideal misconduct machine?" from the genAI_researchintegrity deck.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini :active="['cyber', 'privacy']" /></div>

###### The added risks

# Generative AI: the governance risks

<div class="grid-gov">
<div class="gov-left">

- **Agents act, they do not just answer.** An AI agent can read files, run code and use your credentials. Whatever it can reach, anyone who takes control of it can reach too.
- **Hidden instructions hijack agents.** Text in a web page, email or document can tell an agent to send data elsewhere (prompt injection). There is no reliable fix yet.
- **Attacks get cheaper.** In 2025 one actor used an AI coding agent to steal data from at least 17 organizations in about a month, healthcare among them.
- **Re-identification gets cheaper.** 6 of 24 public interview transcripts were linked to publications, at under $0.50 each (preprint: <a href="https://arxiv.org/abs/2601.05918">Li 2026</a>).
- **Sovereignty is a security control.** A US provider can be compelled to hand over data even from EU data centres (CLOUD Act). **Sovereign AI**, open models on European infrastructure such as the LUMI AI Factory, keeps data under EU law.

</div>
<div>
<div class="breach-head">Closed data, breached</div>
<ul class="breaches">
  <li><span class="kind attack">Attack</span><b><a href="https://cyberscoop.com/finnish-psychotherapy-data-breach-vastaamo/">Vastaamo, 2020</a></b>: therapy records stolen, patients blackmailed.</li>
  <li><span class="kind attack">Attack</span><b><a href="https://www.govinfosecurity.com/trauma-terrorist-victim-data-breached-in-university-attack-a-22409">University of Manchester, 2023</a></b>: data on 1.1 million NHS patients.</li>
  <li><span class="kind mistake">Mistake</span><b><a href="https://wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers">Microsoft AI research, 2023</a></b>: a model-sharing link exposed 38 TB.</li>
  <li><span class="kind agent">AI agent</span><b><a href="https://www.anthropic.com/news/detecting-countering-misuse-aug-2025">Data extortion, 2025</a></b>: an AI coding agent broke in, stole data and wrote the ransom notes.</li>
  <li><span class="kind misuse">Misuse</span><b><a href="https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/">UK Biobank, 2026</a></b>: approved users broke the rules.</li>
</ul>
<div class="breach-head">Not only personal data</div>
<p class="breach-note">Drafts, code and ideas sent to remote AI tools are confidential too.</p>
<ul class="breaches">
  <li><span class="kind disputed">Disputed</span><b><a href="https://www.nature.com/articles/d41586-026-02910-w">Navier–Stokes, 2026</a></b>: mathematicians who checked unpublished work with Codex ask whether it fed OpenAI's result. OpenAI: unlikely, cannot rule it out.</li>
  <li><span class="kind disputed">Disputed</span><b><a href="https://theconversation.com/a-biologist-queries-whether-ai-borrowed-his-work-to-make-major-discovery-an-expert-explains-the-rules-293529">Claude's "new" enzyme, 2026</a></b>: a Copenhagen researcher who shared drafts with Claude had found the enzymes first. Anthropic: no access to his chats.</li>
</ul>
</div>
</div>

<div class="ref-bottom"><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">OWASP LLM01 2025</a> · <a href="https://www.anthropic.com/news/detecting-countering-misuse-aug-2025">Anthropic 2025</a> · <a href="https://arxiv.org/abs/2601.05918">Li 2026</a> · <a href="https://www.justice.gov/criminal/cloud-act-resources">CLOUD Act</a> · <a href="https://www.lumi-ai-factory.eu/">LUMI AI Factory</a> · More: <a href="https://eglerean.github.io/genAI_researchintegrity/">AI tools, Research Integrity and Ethics</a></div>

<style>
.breach-head { font-family: var(--asc-font-serif); font-weight: 700; font-size: 0.9rem; margin: -0.3rem 0 0.25rem; }
.slidev-layout ul.breaches { list-style: none; margin: 0 !important; padding: 0 !important; }
.slidev-layout ul.breaches li { padding: 0.25rem 0.55rem; margin: 0 0 0.25rem !important; border: 2px solid var(--asc-border); border-radius: var(--asc-radius-md); background: var(--asc-surface); font-size: 0.66rem !important; line-height: 1.22 !important; }
.slidev-layout ul.breaches li::before { display: none; }
.slidev-layout ul.breaches li b { font-family: var(--asc-font-serif); }
.slidev-layout ul.breaches li b a { color: inherit; border-bottom: none !important; text-decoration: underline; text-decoration-thickness: 1px; text-underline-offset: 2px; }
.slidev-layout .grid-gov { display: grid; grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr); gap: 1.2rem; }
.slidev-layout .gov-left li { font-size: 0.86rem !important; line-height: 1.3 !important; margin: 0.2rem 0 !important; }
.kind { display: inline-block; margin-right: 0.35rem; padding: 0.02rem 0.45rem; border-radius: 999px; font-size: 0.55rem; font-weight: 700; text-transform: uppercase; letter-spacing: 0.04em; color: #000; vertical-align: 0.1em; }
.kind.attack { background: var(--aalto-red); }
.kind.mistake { background: var(--aalto-orange); }
.kind.misuse { background: var(--aalto-darkyellow); }
.kind.agent { background: var(--asc-night); color: var(--asc-paper); }
.kind.disputed { background: transparent; border: 1.5px dashed var(--asc-text); }
.slidev-layout .breach-note { font-size: 0.68rem !important; line-height: 1.25 !important; margin: 0 0 0.3rem !important; }
.breaches + .breach-head { margin-top: 0.35rem; }
.slidev-layout .grid-gov ~ .ref-bottom { right: 49% !important; }
</style>

<!--
CHECK BEFORE PRESENTING
- Li 2026 is a single-author preprint with manual verification.
- Navier–Stokes and the enzyme case are disputes, not proven leaks. Neither researcher accuses the company of taking the work on purpose. Say "ask whether", not "was stolen".
- CLOUD Act: a US provider can be ordered to disclose data it controls wherever it is stored; providers can challenge orders that conflict with foreign law. EU-US Data Privacy Framework does not change this.
- Anthropic 2025 is the vendor's own threat report; victims are not named. "Demands sometimes above $500,000" are demands, not payments.
-->



---
layout: section
color: dark
hexText: "HOW\nTO\nSOLVE?"
class: title-middle
---

# What should researchers and research support do?

---
layout: default
---

<div class="corner-icon"><TugOfWar mini active="decision" /></div>

# 1. For each object pick a level of protection

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

# 2. PETs and who could identify whom

<div>

- Chose the right combination of **Privacy Enhancing Technologies** (PETs) to minimize personal data
- **Pseudonymised data is still personal data**. 
- **The same data can be personal for one party and not for another** (*EDPS v SRB*). Public release is the hard case: anyone, with any tool.
- **Is it anonymous? three checks:** can someone be singled out, linked to other data, or have something inferred about them? (see EDPB guidelines draft)
- **Promise only what you can keep.** Do not write "anonymous" for a small interview study, and recheck as tools improve.

</div>

<div class="spectrum">
  <div class="sp-row">
    <div class="sp-box" style="--c: var(--aalto-red)"><b>Personal data with direct identifiers</b></div>
    <div class="sp-box" style="--c: var(--aalto-orange)"><b>Pseudonymisation</b><i>Replacing strong identifiers: tokenization, hashing, encryption</i></div>
    <div class="sp-box" style="--c: var(--aalto-darkyellow)"><b>Masking</b><i>Suppression / removal of strong identifiers</i></div>
    <div class="sp-box" style="--c: color-mix(in srgb, var(--aalto-darkyellow) 45%, var(--aalto-green))"><b>Anonymisation</b><i>K-anonymity, l-diversity, t-closeness, perturbation, data swapping, differential privacy</i></div>
    <div class="sp-box" style="--c: var(--aalto-green)"><b>Anonymisation</b><i>Aggregation, data synthesis</i></div>
  </div>
  <div class="sp-arrow"><span class="sp-end sp-left">Personal data</span><span class="sp-end sp-right">Anonymous data</span></div>
  <div class="sp-row">
    <div class="sp-box sp-risk" style="--c: var(--aalto-red)">Easy to re-identify</div>
    <div class="sp-box sp-risk" style="--c: var(--aalto-orange)">Can be re-identified with the key</div>
    <div class="sp-box sp-risk" style="--c: var(--aalto-darkyellow)">The key is lost but other data (will) exist, and re-identification can be reasonably likely</div>
    <div class="sp-box sp-risk" style="--c: color-mix(in srgb, var(--aalto-darkyellow) 45%, var(--aalto-green))">Impossible to re-identify, but data are still data from individuals</div>
    <div class="sp-box sp-risk" style="--c: var(--aalto-green)">Impossible to re-identify, and data are not related to any individual</div>
  </div>
</div>


<div class="ref-bottom"><a href="https://eur-lex.europa.eu/eli/reg/2016/679/oj">GDPR</a> (Art 4(5), Recital 26) · <a href="https://www.fieldfisher.com/en-be/locations/belgium/insights/edps-v-srb-cjeu%e2%80%99s-contextual-approach-to-pseudonym">EDPS v SRB</a> · <a href="https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en">EDPB 02/2026 (draft)</a> · <a href="https://doi.org/10.1038/s41586-026-10688-0">Knolle 2026</a></div>

<style>
.spectrum { margin: 0.4rem 0 0; }
.sp-row { display: grid; grid-template-columns: repeat(5, minmax(0, 1fr)); gap: 0.5rem; }
.sp-box { padding: 0.3rem 0.45rem; border: 2px solid var(--c); border-radius: var(--asc-radius-md); background: color-mix(in srgb, var(--c) 22%, transparent); font-size: 0.62rem; line-height: 1.2; text-align: center; }
.sp-box b { display: block; font-family: var(--asc-font-serif); font-size: 0.74rem; line-height: 1.15; }
.sp-box i { display: block; margin-top: 0.15rem; }
.sp-risk { display: flex; align-items: center; justify-content: center; font-weight: 600; font-size: 0.68rem; }
.sp-arrow { position: relative; height: 0.5rem; margin: 1.15rem 0.9rem 0.45rem 0; border-radius: 999px 0 0 999px; background: linear-gradient(90deg, var(--aalto-red), var(--aalto-orange), var(--aalto-darkyellow), var(--aalto-green)); }
.sp-arrow::after { content: ""; position: absolute; right: -0.9rem; top: 50%; transform: translateY(-50%); border-left: 0.9rem solid var(--aalto-green); border-top: 0.6rem solid transparent; border-bottom: 0.6rem solid transparent; }
.sp-end { position: absolute; bottom: 0.6rem; font-size: 0.66rem; font-weight: 700; font-style: italic; }
.sp-left { left: 0; color: color-mix(in srgb, var(--aalto-red) 75%, var(--asc-text)); }
.sp-right { right: 0; color: color-mix(in srgb, var(--aalto-green) 45%, var(--asc-text)); }
</style>

<!--
CHECK BEFORE PRESENTING
- Draft Guidelines 02/2026 were read through law-firm summaries, and Knolle 2026 through its abstract and press release. Check both against the originals.
-->

---
layout: default
---

<div class="corner-icon"><TugOfWar mini :active="['ai', 'cyber']" /></div>


# 3. Match the tool to the data

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

# 4. Keep closed work checkable

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


<div class="ai-disclosure">AI use: generative AI tools were used to code the deck as HTML pages and retrieve some sources.</div>

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
layout: image-right
image: /pets-landscape.png
class: fit-image
---

###### Backup · Concepts

# Privacy Enhancing Technologies (PETs)

Broadly two families:

- Techniques that **transform the data**
- Techniques that **harden the computing environment**

Embedded in the security of all other components.

<p class="pets-caption">Figure 5.1 from <a href="https://www.edpb.europa.eu/system/files/2025-06/spe-training-on-ai-and-data-protection-technical_en.pdf">Glerean 2025</a>. The landscape of PETs solutions. Various techniques can be combined to ensure the privacy of the entire system by altering the data or by improving security of storage, communication, and computations. The image is an evolution of Garrido et al. (2022).</p>

<style>
.slidev-layout .pets-caption { position: absolute; left: 3.5rem; right: 2rem; bottom: 3.2rem; font-size: 0.66rem !important; line-height: 1.3 !important; opacity: 0.8; }
</style>

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
