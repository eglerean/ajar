# Slide plan: As open as possible, as closed as necessary

Research integrity, AI, privacy and cybersecurity through an open science lens

- **Format:** 20 slides, Slidev markdown, about 40 minutes
- **Assumed audience:** researchers and research support in the EU
- **Status date:** legal and factual claims checked on 4 November 2026

**Thesis.** "Open" and "closed" are decisions per research object. Integrity decides what must stay checkable, privacy decides who could be harmed, cybersecurity decides whether "closed" holds, and AI moves all three lines.

| Part | Slides | Job |
|---|---|---|
| A. The principle | 1–5 | Why this is a rule with a burden of proof, and how the four domains connect |
| B. As open as possible | 6–8 | What integrity needs open, and why protection serves validity |
| C. As closed as necessary | 9–12 | What "necessary" means, how to measure it, and what makes closure real |
| D. AI moves the line | 13–17 | New objects to govern, cheaper attacks, new attack surface |
| E. Closed, but verifiable | 18–20 | Infrastructure, legal status, and what to do on Monday |

**Running devices**

1. **Running case (fictional):** 80 interviews on workplace harassment. Appears on slides 6, 9, 13, 14 and 15.
2. **Evidence badges:** `Incident`, `Survey`, `Audit`, `Preprint`. The deck should keep documented harm, demonstrated vulnerability and plausible concern visibly apart.
3. **Status badges on legal items:** `Binding`, `Phasing in`, `Draft`, `Proposal`.
4. **Corner icon:** a mini version of the slide 4 grid with the active cell highlighted, same idea as the AI pyramid icon in the current deck.

---

## Part A. The principle

### 1. As open as possible, as closed as necessary

Cover. Subtitle: Research integrity, AI, privacy and cybersecurity through an open science lens. Presenter, date and CC BY line as in the current deck.

**Diagram:** `layout: cover`, `hexText: "OPEN\nCLOSED"`.

### 2. Three ways to fail the same principle

- **Closed by habit.** "Available on request": 1,792 authors asked, 123 shared data (6.8%). `Audit`
- **Open by accident.** UK Biobank data in public code repositories, first detected in 2022; 80 takedown notices to GitHub in July–December 2025. UK Biobank's explanation: researchers published code, which journals often require. `Incident`
- **Closed on paper.** April 2026: data on about 500,000 participants listed for sale. No hack: breaches of access policy by approved institutions. `Incident`
- Each failure has a different owner: integrity, privacy, security. Neither more openness nor more closure fixes all three.

**Diagram:** three doors. Locked with nobody holding the key. Wide open with nobody watching. "Do not enter" sign with no lock.

**Sources:** Gabelica 2022; UKB statement 2026; Guardian via Freevacy 2026; UKB Oversight 2026; Register 2026

### 3. "Closed" needs a reason

- ALLEA 2023 §2.5: access "as open as possible, as closed as necessary", with transparent routes to access. §3.1: withholding data or results without justification is a violation.
- Open Data Directive Art 10: publicly funded research data "open by default"; weigh IPR, personal data, confidentiality, security and legitimate commercial interests.
- Horizon Europe: the data management plan must explain any restriction.
- Finnish national policy 2026–2030: same principle; where limits are justified, describe the resources as transparently as possible.
- So every closure needs an object, a reason and an access route. "On reasonable request" has none of the three.

**Diagram:** the normative cascade from your RCR page (ethics → EU law → Finland/Aalto → researcher), with this principle's wording on each step. Beside it, chips for valid reasons to close: personal data, confidentiality, IPR, security and dual use, commercial interests.

**Sources:** ALLEA 2023; ODD; Horizon Europe; FI Policy 2026; Council Rec 2024; RCR page

### 4. Four domains, six intersections, one question

- Research integrity: can others check it and trust it?
- Privacy: who could be harmed, and how?
- Cybersecurity: what can get in, get out or be altered?
- AI: what changes with a model in the loop?
- Open science is not a fifth domain. It is the question asked in every cell: what can be open here?

**Diagram:** triangular 4×4 grid. Each cell has one example and links to its slide, so this also works as the agenda.

| | Privacy | Cybersecurity | AI |
|---|---|---|---|
| **Integrity** | Confidentiality promises shape the answers (8) | Tampering and provenance (5, 12) | Disclosure vs documentation (14) |
| **Privacy** | | "Closed" data that leaks (12) | Cheaper re-identification, leaky models (15, 16) |
| **Cybersecurity** | | | Agents and poisoned inputs (17) |

### 5. One triad, three communities

- **Confidentiality:** participants, privacy, research security.
- **Integrity:** data, code and models unaltered and traceable. A precondition for research integrity, not the same thing.
- **Availability:** open science. Outputs that exist, can be found and can still be reached years later.
- GDPR already uses these terms: Art 5(1)(f) and Art 32(1)(b).
- Access decisions trade C against A. I is the one you do not trade.

**Diagram:** triangle with community labels on each vertex. The C–A edge is a slider marked with access tiers; I stays fixed.

**Sources:** GDPR; CodeRefinery security page

---

## Part B. As open as possible

### 6. A study is a bundle of objects, each with its own access level

- Transparency of claims, of methods and of data are three separate decisions.
- Open by default: question, protocol, data dictionary, code, container recipe, aggregate results (check small cells).
- Gated by default: participant-level data, linkage keys.
- New rows: prompts, logs, model weights, synthetic data (slides 14, 16).

**Diagram:** heatmap. Rows are objects; columns are Public, Registered users, Controlled access, Secure environment only, Not shared. Filled in for the running case. Build it as an HTML table in the style of `.bp-matrix`.

**Sources:** Lvovs 2025

### 7. FAIR says how to reach data, not who gets it

- FAIR A1.2 allows authentication and authorisation where necessary. A2 keeps metadata reachable after the data are gone.
- Behavioural datasets became more reusable while keeping access restrictions (two worked examples).
- FAIR is uneven. Feasibility varies with discipline, infrastructure and resources; 79.4% of data users report difficulty finding relevant data (n=643, LMIC focus).
- Not every dataset earns the cost. Appraise at the planning stage.

**Diagram:** public metadata card on top, a door with access conditions below it, the dataset behind the door. Place F, A, I and R where each applies.

**Sources:** Wilkinson 2016; van Ravenzwaaij 2025; Hellstrand 2025; Waithira 2024; Glerean 2026 (Data Available on Unreasonable Request)

### 8. Protecting participants protects validity

- 17,729 secondary school students: 46.0% had a privacy, confidentiality or data-use concern; 29.2% of those said it affected the accuracy of their answers. `Survey`
- Those students skipped sensitive measures more often, and gender-diverse adolescents reported more concerns. The loss is not random.
- Parkinson's patients favoured openness, but lower visit burden dominated their choices (randomised pilot, hypothetical trials).
- ALLEA §2.5: tell participants how data are used, reused, accessed, stored and deleted. Name the sharing route. Do not promise "anonymous" for a small interview study.
- Ethics consent is not GDPR consent. Consent as the legal basis keeps the link to the person, and non-random withdrawal biases the cohort.

**Diagram:** causal chain. Weak promise → withheld or altered answers plus non-response → biased estimate. Mirror row with a credible promise. Mark it as association, self-reported.

**Sources:** Soneson 2025; Iskander 2025; ALLEA 2023; Glerean SciResGDPR 2026

---

## Part C. As closed as necessary

### 9. "Necessary" depends on who could identify whom, with what means

- Four words, not synonyms: de-identified (not a GDPR term), pseudonymised (Art 4(5)), anonymous (Recital 26), synthetic (a method, not a status).
- *EDPS v SRB* (C-413/23 P, 2025): identifiability depends on the means of the party concerned. The same data can be personal for one party and not for another. `Binding`
- EDPB draft Guidelines 02/2026: test record isolation, linkage and inference. Contracts supplement technical measures, they do not replace them. `Draft`
- Digital Omnibus: the Council mandate of 21 October 2026 keeps the Art 4(1) definition of personal data. `Proposal`
- Running case: the credible adversary is a colleague who recognises the story. Removing names does not stop that.

**Diagram:** one dataset, three viewers. Key holder: personal data. Recipient without means: assess. Public download: assume anyone, with any tool.

**Sources:** GDPR; EDPS v SRB; EDPB 02/2026 (draft); Council mandate 2026

### 10. Average risk hides the people at risk

- 70 clinical trial datasets (31 open, 39 controlled): 7 labelled anonymised still held direct identifiers such as date of birth or initials. The scores measure structure; nobody was re-identified. `Audit`
- "Anonymised" health data kept measurable membership risk, depending on the privacy model and how records were changed. `Audit`
- Medical AI, seven datasets: aggregate attacks look close to chance, yet are near-perfect for some patients. Underrepresented groups face disproportionate success, and high-risk patients increase with model capacity. `Audit`
- Report tails, subgroups and attack conditions, not one average.

**Diagram:** schematic strip plot of per-patient risk with a mean marker near chance, a long tail and one highlighted subgroup. Must be labelled "schematic, not data".

**Sources:** Rodriguez 2025; Meurers 2025; Knolle 2026

### 11. Privacy-enhancing technologies move risk, they do not remove it

| Technique | Gives you | Risk moves to |
|---|---|---|
| Pseudonymisation | No direct identifiers in working data | Anyone who can link; narrative text still identifies |
| Synthetic data | Teaching, software tests, previews | Fidelity and disclosure; membership inference was the hardest criterion (Demuth 2025) |
| Differential privacy | Formal bound on one record's influence | Correlations and small groups (Adams 2025); the budget is a value judgement |
| Federated learning | Raw data stay at each site | Updates can leak; site differences cost accuracy |
| Secure environment | Control of who, where and what leaves | Cost, usability, reproducibility (slide 18) |

- Use bundles. Report parameters, not labels.

**Diagram:** this table, with an arrow column for "risk moves to".

**Sources:** Adams 2025; Demuth 2025; Federated review 2025; Honkela interview 2026; EDPB Guidelines 01/2025

### 12. "Closed" is only as real as the security behind it

- 2020, Vastaamo: psychotherapy records stolen, patients extorted one by one. `Incident`
- 2023, University of Manchester: research data on about 1.1 million NHS patients affected, including trauma and terror-attack victims. `Incident`
- 2023, Microsoft AI research: a link in an open-model repository opened 38 TB with write access, so the models could have been overwritten. `Incident`
- 2026, UK Biobank: no hack. The response is no participant-level downloads, a data airlock and confirmed deletion. `Incident`
- Contracts state rules, controls enforce them: MFA, least privilege, logging, export limits, output checks.
- Art 32 GDPR binds you now. NIS2 and the Finnish Cybersecurity Act exclude universities from "research organisation", so do not assume a sector regime covers you.

**Diagram:** horizontal timeline 2020–2026. Each incident has a C, I or A tag and the missing control.

**Sources:** Vastaamo 2020; Manchester 2023; Wiz 2023; UKB Oversight 2026; GDPR; NIS2; NCSC-FI; FI Cybersecurity Act

---

## Part D. AI moves the line

### 13. Ask which environment, not which chatbot

- Two separate problems: epistemic (is the output right?) and information governance (who receives the input?).
- Uploading is disclosure to a processing system. Assess roles, location, retention, training use and admin access per product and contract.
- Rule by data class, not by brand: public → any tool; internal → approved tools; confidential → contractual guarantees or local models; secret → local tools inside a TRE.
- Keep the evidence straight. "Everything you type becomes public" is not established. "Treat non-approved tools as public" is still sound policy.
- Running case: pseudonymised transcripts do not go into a consumer chatbot.

**Diagram:** four-row ladder of data classes with the allowed tool type.

**Reuse:** "AI risks in research" cards from genAI_researchintegrity as a small inset; classification table from the aalto.fi best-practices page.

**Sources:** Aalto best practices; EC Guidelines v4; Jones 2025; Glerean 2026 (AI risks)

### 14. Disclosure is not documentation

- "We used ChatGPT" does not let anyone reconstruct the work: the same prompt can give different outputs.
- Keep: tool and version, task, input type, prompt logic, what was accepted or rejected, who verified it.
- ALLEA §3.1: hiding AI use is a violation. EC Guidelines v4: retain or share prompts, logs and versions when needed "to understand, reproduce or audit". TENK 2026: document AI like any other important method, including in metadata and the DMP.
- Full prompt logs can leak source text. Keep a restricted audit log and publish a sanitised workflow.

**Diagram:** one AI session splits into two lanes through a filter: restricted log and public supplement. Running case: interview quotes stay in the restricted lane.

**Sources:** Cwik 2026; Jones 2025; Cui & Alexander 2026; ALLEA 2023; EC Guidelines v4; TENK 2026

### 15. LLMs are cutting the cost of re-identification

- Published interviews: of 24 public Anthropic Interviewer transcripts mentioning published work, 6 were linked to publications, at under $0.50 and about 4 minutes each. `Preprint`
- Pseudonymous profiles: 226 of 338 Hacker News users identified at 90% precision, $1–4 each. `Preprint`
- Redaction: after named-entity masking, at least one attacker still succeeded on 85.3% of a sample of synthetic test transcripts. The signal sits in role, project and affiliation. `Preprint`
- The legal test already expects this. Recital 26 counts cost, time and technological developments. EDPB draft 02/2026: AI, especially agentic AI, lowers time and cost, so reassess periodically. `Draft`
- Demonstrated vulnerability, not documented harm: small samples, partly manual verification.

**Diagram:** pipeline from transcript to attributes, web search, candidates and confidence score, with cost and time tags and a "no names needed" marker. Running case: why redacted transcripts still stay controlled.

**Sources:** Li 2026; Lermen 2026; Wen & Li 2026; GDPR; EDPB 02/2026 (draft); UKB Oversight 2026

### 16. Sharing model weights can be sharing data

- Two different attacks: membership inference (was this person in training?) and extraction (what did the model memorise?). State which one, under which conditions.
- EDPB Opinion 28/2024: a model trained on personal data is not automatically anonymous. Draft 02/2026 treats inference through queries as in scope.
- Knolle 2026 recommends patient-level audits before release, access control and differential privacy.
- Weights cannot be recalled, and unlearning is largely theoretical without special training.
- Minimising vs measuring: AI Act Art 4a allows special-category data only where strictly necessary for bias detection and correction, under safeguards. It is not a training licence.

**Diagram:** release ladder: paper → code → gated weights → public weights, with a privacy audit gate at each step. Imaging example: qualified verifiers rerun the workflow inside secure environments.

**Sources:** EDPB Opinion 28/2024; EDPB 02/2026 (draft); Knolle 2026; Honkela interview 2026; AI Omnibus

### 17. Agents turn untrusted text into actions

- Lethal trifecta: private data, untrusted content and a way to send data out. In research: participant data, PDFs and web pages, network access.
- Prompt injection has reached peer review. Authors hid "positive review" prompts; ICML 2026 used hidden prompts to flag 506 reviewers and desk-rejected 497 papers. EC Guidelines v4 now names hidden prompts.
- Open inputs need checks too. Pickle model files run code on load; non-existent packages reached at least 5.2% for commercial models and 21.7% for open-source models.
- Validate, minimize, contain: cut one leg of the trifecta. No network, read-only data, disposable containers, pinned hashes, human check points.
- EC Guidelines v4: agents are never "a delegation of control or responsibility".

**Diagram:** triangle with the three legs, a research example on each, scissors on one leg.

**Reuse:** `/risk-domains.png` and the agent diagram from genAI_researchintegrity.

**Sources:** Willison 2025; Nikkei 2025; ICML 2026; EC Guidelines v4; nullifAI 2025; Spracklen 2025; CodeRefinery security page

---

## Part E. Closed, but verifiable

### 18. Secure environments are a reproducibility variable

- Same R scripts, two English secure settings: data preparation was the obstacle. "Even with perfect code sharing, data reproducibility remains a challenge."
- Closure has a price. Controlled trial datasets took 270 days on average to access, open ones 8. Two UK TREs differed on approval, accreditation, cost and linkage. Lower-resource institutions report more difficulty.
- EU direction: EHDS permits and secure processing environments; only non-personal outputs leave; results public within 18 months (Art 61). `Phasing in`
- Finland: since 1 May 2026 Findata can allow another environment for a special reason, with the recipient as independent controller. `Binding`
- Build for verification: approved containers, stable dataset versions, machine-executable workflows, public metadata, predictable output checks.

**Diagram:** "verify under closure" pipeline: public code and container → secure environment with versioned data → run → output check → public result. Second path for a qualified verifier.

**Sources:** Williams 2025; Rodriguez 2025; IJPDS TREs; Waithira 2024; EHDS; Findata

### 19. Check the status before you cite the rule

EU rulebook, November 2026.

| Binding now | Phasing in | Not law |
|---|---|---|
| GDPR | CRA: reporting since 11 Sep 2026, full 11 Dec 2027 | EDPB draft Guidelines 1/2026 (research) |
| Open Data Directive, through national law | AI Act high-risk: Annex III 2 Dec 2027, Annex I 2 Aug 2028 | EDPB draft Guidelines 02/2026 (anonymisation) |
| AI Act: prohibitions, GPAI, Art 50 | EHDS: 26 Mar 2027; secondary use 26 Mar 2029; more categories 26 Mar 2031 | Digital Omnibus COM(2025)837: Council mandate 21 Oct 2026, Parliament committee vote expected early 2027 |
| Digital Omnibus on AI, Reg. (EU) 2026/1744, in force 27 Jul 2026 (Art 4 softened, Art 4a added) | | |
| Finnish Secondary Use Act | | |

Scope traps:

- AI Act Art 2(6) and 2(8) exclude research-only systems and pre-market research. Deployment and real-world testing are not excluded.
- CRA: free, non-commercial open source is outside; public funding alone does not make it commercial (Commission guidance).
- NIS2: see slide 12.

**Diagram:** swimlane timeline 2018–2031 (privacy, AI, health, cyber) with a "you are here" marker at November 2026.

**Sources:** AI Act; AI Omnibus; EHDS; CRA; CRA guidance 2026; EDPB 1/2026 (draft); EDPB 02/2026 (draft); COM(2025)837; Council mandate 2026; NicFab 2026

### 20. Five questions before you open, close or upload

1. Which object is this?
2. Who could be harmed, by whom, with what means today?
3. What must stay checkable, and by whom?
4. Where does it run, and who else can see it?
5. Is the closure written down and technically enforced?

Closing line: not "how do we stop risky research?" but "what infrastructure lets people do ambitious work safely and reproducibly?"

Footer: AI-use disclosure for this deck (literature review counts as substantial use under EC Guidelines v4).

**Diagram:** `layout: end`, five honeycomb cells.

**Presenter notes:** three discussion prompts from the report: which parts must be open for real scrutiny; whether approved secure GenAI should be research infrastructure; who decides when privacy reduces accuracy for a small subgroup.

---

## Build notes for Claude Code

- New repo with the theme copied from genAI_researchintegrity (`slidev-theme-aalto-scicomp/`), Slidev pinned to `~0.47.5`, `palette: aalto-classic`, `titles: aalto`. Follow the theme README.
- No section-divider slides, to stay at 20. Use an eyebrow on each content slide: `###### Part C · As closed as necessary`.
- Copy `style.css` for `.ref-line`, `.ref-bottom`, `.corner-icon`, `.grid-3`, `.grid-2-3` and the coloured cards. `.bp-matrix` is defined in the "When should I use AI" slide of `slides.md`. Avoid `>` child selectors, which break per-slide styles in Slidev 0.47.
- Build diagrams as inline SVG or HTML/CSS, like the wheel and pyramid in the current deck.
- Add evidence and status badges as one small `.badge` class with variants.
- Slide 10: do not invent patient percentages. Sources give none.

## Check before presenting

- **Fast-moving:** Digital Omnibus (slides 9, 19) and the four preprints (slide 15).
- **Read through summaries only:** EDPB draft 02/2026 and the final text of Reg. (EU) 2026/1744. Check slides 9, 15, 16 and 19 against the primary texts.
- **Knolle 2026:** read through the abstract and press release, as the Nature page would not load.
- **Taken from the report, not opened:** van Ravenzwaaij, Hellstrand, Waithira, Iskander, Meurers, Adams, Demuth, Jones, Lvovs and the federated learning review. For Cwik only the bibliographic record was confirmed.
- **Slide 12:** confirm Aalto's actual NIS2 position with the CISO. A university could still be in scope through another role.
- **Slide 13:** the four classes come from the public aalto.fi page, while the adaptation of the Finnish classification model is still in progress.

## References

**Rules and guidance**

- [ALLEA 2023](https://doi.org/10.26356/ECOC): European Code of Conduct for Research Integrity, revised edition
- [ODD](https://eur-lex.europa.eu/eli/dir/2019/1024/oj): Open Data Directive (EU) 2019/1024, Art 10
- [Horizon Europe](https://rea.ec.europa.eu/open-science_en): open science obligations
- [FI Policy 2026](https://tsv.fi/fi/palvelut/linjauslouhi/index.php/Aineistot/en): Open research data and methods, national policy and executive plan 2026–2030
- [Council Rec 2024](https://eur-lex.europa.eu/eli/C/2024/3510/oj/eng/pdf): Council Recommendation on enhancing research security
- [GDPR](https://eur-lex.europa.eu/eli/reg/2016/679/oj): Regulation (EU) 2016/679
- [EDPS v SRB](https://www.fieldfisher.com/en-be/locations/belgium/insights/edps-v-srb-cjeu%e2%80%99s-contextual-approach-to-pseudonym): C-413/23 P, summary
- [EDPB Guidelines 01/2025](https://www.edpb.europa.eu/our-work-tools/documents/public-consultations/2025/guidelines-012025-pseudonymisation_en): pseudonymisation
- [EDPB 1/2026 (draft)](https://www.edpb.europa.eu/system/files/2026-04/edpb_guidelines_202601_scientificresearch_en.pdf): scientific research
- [EDPB 02/2026 (draft)](https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en): anonymisation; summaries from [Sidley](https://datamatters.sidley.com/2026/07/27/edpb-publishes-draft-guidelines-on-anonymisation/), [DLA Piper](https://privacymatters.dlapiper.com/2026/08/eu-edpb-publishes-draft-guidelines-on-anonymisation/) and [GamingTechLaw](https://www.gamingtechlaw.com/2026/07/edpb-anonymisation-guidelines-ai/)
- [EDPB Opinion 28/2024](https://www.edpb.europa.eu/our-work-tools/our-documents/opinion-board-art-64/opinion-282024-certain-data-protection-aspects_en): AI models
- [COM(2025)837](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52025PC0837): Digital Omnibus proposal
- [Council mandate 2026](https://iapp.org/news/a/eu-member-states-finalize-digital-omnibus-negotiating-stance): IAPP report; [NicFab 2026](https://www.nicfab.eu/en/posts/digital-omnibus-council/): procedural status
- [AI Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng): Regulation (EU) 2024/1689
- [AI Omnibus](https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng): Regulation (EU) 2026/1744; summaries from [Stephenson Harwood](https://www.stephensonharwood.com/media/x0gbn3zx/the-digital-omnibus-on-ai-ten-key-takeaways.pdf) and [euaiact.com](https://www.euaiact.com/digital-omnibus-ai)
- [EHDS](https://eur-lex.europa.eu/eli/reg/2025/327/oj): Regulation (EU) 2025/327; [Art 61 text](https://streamlex.eu/articles/ehds-en-art-61/)
- [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj): Regulation (EU) 2024/2847; [CRA guidance 2026](https://www.opensourceforu.com/2026/07/eu-clarifies-cra-rules-for-non-commercial-open-source/), news report
- [NIS2](https://eur-lex.europa.eu/eli/dir/2022/2555/oj): Directive (EU) 2022/2555
- [NCSC-FI](https://kyberturvallisuuskeskus.fi/en/our-activities/regulation-and-supervision/public-administration-and-research-organisations): public administration and research organisations
- [FI Cybersecurity Act](https://www.finlex.fi/api/media/statute/535367/mainPdf/main.pdf): 124/2025, Swedish text
- [Findata](https://findata.fi/en/permits/data-permits/): data permits
- [EC Guidelines v4](https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en): Living guidelines on generative AI in research, 15 October 2026
- [TENK 2026](https://tenk.fi/sites/default/files/2026-06/Artificial%20Intelligence%20in%20Research.%20TENK%27s%20Recommendation%202026.pdf): AI in research recommendation
- [Aalto best practices](https://www.aalto.fi/en/research-art/best-practices-for-ai-use-in-research-work)

**Research evidence**

- [Gabelica 2022](https://pubmed.ncbi.nlm.nih.gov/35654271): compliance with data sharing statements
- [Wilkinson 2016](https://doi.org/10.1038/sdata.2016.18): FAIR principles
- [van Ravenzwaaij 2025](https://journals.sagepub.com/doi/10.1177/25152459251336130): de-identification and FAIR, worked examples
- [Hellstrand 2025](https://journals.sagepub.com/doi/10.1177/20539517251349157): FAIR for whom?
- [Waithira 2024](https://pubmed.ncbi.nlm.nih.gov/39565766/): data sharing and reuse in clinical research
- [Lvovs 2025](https://doi.org/10.1016/j.xcrm.2025.102080): ethical data sharing and open science
- [Soneson 2025](https://doi.org/10.1016/j.jadohealth.2025.03.004): adolescents and sensitive data
- [Iskander 2025](https://doi.org/10.1177/15562646251384573): open science vs participation burden
- [Rodriguez 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12647387/): re-identification risk in trial datasets
- [Meurers 2025](https://pubmed.ncbi.nlm.nih.gov/40652760/): phantom anonymization
- [Knolle 2026](https://doi.org/10.1038/s41586-026-10688-0): disparate privacy risks from medical AI; [TUM release](https://www.tum.de/en/news-and-events/all-news/press-releases/details/study-reveals-privacy-risks-in-medical-ai)
- [Adams 2025](https://pubmed.ncbi.nlm.nih.gov/40343279/): fidelity, privacy and utility of synthetic patient data
- [Demuth 2025](https://pubmed.ncbi.nlm.nih.gov/41032725/): virtual clinical trials as open datasets
- [Federated review 2025](https://www.sciencedirect.com/science/article/pii/S2773186325002257): privacy-preserving federated learning in healthcare
- [Williams 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12273930/): the challenges of replication
- [IJPDS TREs](https://ijpds.org/article/view/3243): barriers across multiple TREs
- [Cwik 2026](https://doi.org/10.1186/s41073-026-00245-8): disclosure is not documentation
- [Jones 2025](https://journals.sagepub.com/doi/10.1177/16094069251404329): heuristic for disclosing AI use
- [Cui & Alexander 2026](https://doi.org/10.48550/arXiv.2602.14349): same prompt, different outcomes
- [Li 2026](https://arxiv.org/abs/2601.05918): re-identification in the Anthropic Interviewer dataset
- [Lermen 2026](https://arxiv.org/abs/2602.16800): large-scale online deanonymization
- [Wen & Li 2026](https://arxiv.org/abs/2610.05586): AgentDoxx
- [Spracklen 2025](https://arxiv.org/abs/2406.10279): package hallucinations, figures as on the CodeRefinery page

**Incidents and security**

- [UKB statement 2026](https://www.ukbiobank.ac.uk/?p=63092): response on data in code repositories
- [Guardian via Freevacy 2026](https://www.freevacy.com/news/the-guardian/confidential-uk-biobank-health-records-exposed-online/7214)
- [UKB Oversight 2026](https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/): Oversight Committee report
- [Register 2026](https://www.theregister.com/2026/04/23/500k_biobank_volunteers_data_listed/): sale listings
- [Vastaamo 2020](https://cyberscoop.com/finnish-psychotherapy-data-breach-vastaamo/)
- [Manchester 2023](https://www.govinfosecurity.com/trauma-terrorist-victim-data-breached-in-university-attack-a-22409)
- [Wiz 2023](https://wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers): Microsoft AI research exposure
- [nullifAI 2025](https://thehackernews.com/2025/02/malicious-ml-models-found-on-hugging.html)
- [Willison 2025](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/): lethal trifecta
- [ICML 2026](https://blog.icml.cc/2026/03/18/on-violations-of-llm-review-policies/): violations of LLM review policies
- [Nikkei 2025](https://asia.nikkei.com/business/technology/artificial-intelligence/positive-review-only-researchers-hide-ai-prompts-in-papers): hidden prompts in manuscripts

**Your own material**

- [genAI_researchintegrity](https://github.com/eglerean/genAI_researchintegrity): slides, theme, reusable diagrams
- [Glerean 2026 (AI risks)](https://eglerean.github.io/assets/docs/2026_05_06_AI_research_risks.pdf): AI risk framework
- [Glerean 2026 (Data Available on Unreasonable Request)](https://zenodo.org/records/18609058)
- [Glerean SciResGDPR 2026](https://eglerean.github.io/posts/sciresgdpr): consent, anonymisation and open science
- [RCR page](https://scicomp.aalto.fi/scicomp/rcr-scicomp/): normative cascade, classification
- [CodeRefinery security page](https://coderefinery.github.io/coding-with-ai/security/): risk domains, OWASP mapping, Validate. Minimize. Contain.
- [Honkela interview 2026](https://lumi-ai-factory.eu/articles/international-data-protection-day/): differential privacy, synthetic data, unlearning
