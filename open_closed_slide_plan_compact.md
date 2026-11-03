# Compact slide plan: As open as possible, as closed as necessary

Open science with personal data: what researchers can do

- **Format:** 10 slides plus 2 backup slides, Slidev markdown, about 20 minutes
- **Audience:** non-technical researchers who work with personal data and publish articles
- **Status date:** legal and factual claims checked on 4 November 2026

**Message.** Integrity pulls research towards open. Privacy pulls it towards closed. AI adds risk on the first side and cybersecurity on the second. You resolve the tension with four moves, made object by object.

| Part | Slides | Job |
|---|---|---|
| The tension | 1–3 | Show the failures and the one picture that explains them |
| The added risks | 4–5 | AI on the integrity side, cybersecurity on the privacy side |
| Four moves | 6–9 | What a researcher can do |
| Close | 10 | Four questions to take away |

**Running case (fictional):** 80 interviews on workplace harassment, used on slides 6–9.

**Badges:** only where status changes how much weight a claim can bear: `Preprint`, `Draft`, `Proposal`.

---

## The tension

### 1. As open as possible, as closed as necessary

Cover. Subtitle: Open science with personal data: what researchers can do.

**Diagram:** `layout: cover`, `hexText: "OPEN\nCLOSED"`.

### 2. Three ways to fail the same principle

- **Closed by habit.** "Available on request": of 1,792 authors asked, 123 shared their data (6.8%).
- **Open by accident.** UK Biobank data ended up in public code repositories, inside code that journals often ask authors to publish.
- **Closed on paper.** April 2026: data on about 500,000 volunteers listed for sale. No hack: approved institutions broke the rules.

**Diagram:** three doors. Locked with nobody holding the key. Wide open with nobody watching. "Do not enter" sign with no lock.

**Sources:** Gabelica 2022; UKB statement 2026; UKB Oversight 2026; Register 2026

### 3. One tension, two added risks

- Integrity pulls towards open: others must be able to check your work.
- Privacy pulls towards closed: nobody should be harmed by taking part.
- AI adds risk on the integrity side. Cybersecurity adds risk on the privacy side.
- The two sides need each other. Of 17,729 students surveyed, 46.0% had a privacy or data-use concern, and 29.2% of those said it affected the accuracy of their answers.

**Diagram:** tug of war. Integrity pulls left, privacy pulls right, with a marker in the middle labelled "your decision". AI stands behind integrity, cybersecurity behind privacy. This picture returns as the corner icon.

**Sources:** Soneson 2025

---

## The added risks

### 4. AI makes research harder to check

- Errors get cheaper. Papers citing references that do not exist: 1 in 2,828 in 2023, 1 in 277 in early 2026.
- The same prompt can give different outputs, so "we used ChatGPT" does not let anyone reconstruct the work.
- Hiding AI use is an integrity violation (ALLEA 2023 §3.1).
- Peer review is exposed too: authors have hidden instructions in manuscripts to steer AI reviewers.
- The catch: prompts and logs make AI use checkable, but they can contain confidential text. That is the tension again.

**Diagram:** input → AI tool → output, with question marks on the tool and a warning on the log.

**Reuse:** "Generative AI: the ideal misconduct machine?" from genAI_researchintegrity.

**Sources:** Topaz 2026; EC Guidelines v4; Cui & Alexander 2026; ALLEA 2023; Nikkei 2025

### 5. Closed data is only as safe as its security

- **Attack.** Vastaamo 2020: therapy records stolen, patients blackmailed. Manchester 2023: research data on about 1.1 million NHS patients affected.
- **Mistake.** Microsoft AI research 2023: a link for sharing AI models also opened 38 TB of other data.
- **Misuse.** UK Biobank 2026: no hack, approved institutions broke the rules.
- **AI helps the attacker.** 6 of 24 public interview transcripts were linked to publications, at under $0.50 each. Participants had agreed to release, so this shows a capability, not documented harm. `Preprint`
- A contract states the rule. Only a technical control enforces it.

**Diagram:** timeline 2020–2026 with each case tagged attack, mistake or misuse.

**Sources:** Vastaamo 2020; Manchester 2023; Wiz 2023; UKB Oversight 2026; Li 2026

---

## Four moves

### 6. Move 1: Decide per object, and write down why

- A study is many objects. Open or closed applies to each one, not to the study.
- For each object, record the access level, the reason and the route to access.
- FAIR does not mean open: access can require login and approval, while the description stays public.
- "On reasonable request" gives no reason and no route.

**Diagram:** this table, filled in for the running case. Researchers can copy it into a data management plan.

| Object | Level | Reason | Route |
|---|---|---|---|
| Protocol, interview guide | Public | | Repository with DOI |
| Codebook, data dictionary | Public | Check example quotes first | Repository |
| Analysis code | Public | Check for embedded data first | Repository |
| Summary tables | Public | Merge very small groups | Article |
| AI workflow description | Public | | Supplement |
| AI prompts and logs | Controlled | Contain interview text | Audit request |
| Transcripts | Controlled | Participants could be recognised | Data access committee, agreement, secure environment |
| Key linking codes to names | Not shared | Identifies everyone | None |

**Sources:** ALLEA 2023 (§2.5, §3.1); ODD; Horizon Europe; FI Policy 2026; Wilkinson 2016; van Ravenzwaaij 2025

### 7. Move 2: Set the level by who could identify whom

- Pseudonymised data is still personal data for anyone who can use the key. "Synthetic" says how data were made, not that they are safe.
- The same data can be personal for one party and not for another (*EDPS v SRB*). Public release is the hard case: anyone, with any tool.
- Three checks: can someone be singled out, linked to other data, or have something inferred about them? `Draft`
- Look at the most exposed person, not the average. In medical AI, attacks looked close to guessing overall, yet were near-perfect for some patients.
- Promise only what you can keep. Do not write "anonymous" for a small interview study, and recheck as tools improve.

**Diagram:** one dataset, three viewers. Key holder: personal data. Recipient with no realistic means: assess. Public download: assume anyone. Running case: the realistic threat is a colleague who recognises a story.

**Sources:** GDPR (Art 4(5), Recital 26); EDPS v SRB; EDPB 02/2026 (draft); Knolle 2026

### 8. Move 3: Match the tool to the data

- Ask where it runs, not which brand: who receives the data, where they are stored, how long they are kept, whether they train the model, who can look.
- Public data: any tool. Internal: approved tools. Confidential: contractual guarantees or local models. Secret: local tools inside a secure environment.
- Keep the full AI log restricted. Publish a clean workflow: tool and version, task, input type, what you accepted, who checked.
- Never give one AI agent private data, untrusted content and a way to send data out. Remove one, for example the internet connection.

**Diagram:** four-row ladder of data classes with the allowed tool type, and a side strip showing full log → filter → public workflow. Running case: pseudonymised transcripts do not go into a consumer chatbot.

**Sources:** Aalto best practices; EC Guidelines v4; TENK 2026; Cwik 2026; Willison 2025

### 9. Move 4: Keep closed work checkable

- Sharing code is not enough. One team ran the same scripts unchanged in a second secure environment and still hit problems with how the data had been prepared.
- Publish what you can: code, data dictionary, data version, software setup, access route.
- Say who can verify the work and how, for example a qualified person rerunning it inside the secure environment.
- Plan for time. Controlled clinical trial data took 270 days on average to access, open data 8.
- This is the EU direction. From 2029, under the European Health Data Space: permit, secure environment, only non-personal outputs leave, results public within 18 months.

**Diagram:** pipeline: public code and software setup → secure environment with a fixed data version → run → output check → public result. Second path for a qualified verifier.

**Sources:** Williams 2025; Rodriguez 2025; EHDS; Findata

---

## Close

### 10. Four questions before you open, close or upload

1. Which object is this, and why is it closed?
2. Who could identify whom, with what means today?
3. Where does it run, and who else can see it?
4. How can someone still check it?

Closing line: institutions owe researchers the infrastructure that makes this the easy route.

Footer: AI-use disclosure for this deck (literature review counts as substantial use under EC Guidelines v4).

**Diagram:** `layout: end`. A fourth door, ajar: reason on the door, a route to enter, a lock that works. It answers the three doors on slide 2.

---

## Backup slides

### B1. Techniques move risk, they do not remove it

| Technique | Gives you | Risk moves to |
|---|---|---|
| Pseudonymisation | No names in working files | Anyone who can link; stories still identify |
| Synthetic data | Teaching, software tests, previews | Lost patterns, leftover disclosure risk |
| Differential privacy | A formal limit on one person's influence | Accuracy, especially for small groups |
| Federated learning | Raw data stay at each site | Updates can leak; site differences cost accuracy |
| Secure environment | Control of who, where and what leaves | Cost, usability, reproducibility |

**Sources:** Adams 2025; Demuth 2025; Federated review 2025; Honkela interview 2026

### B2. Check the status before you cite the rule

| Binding now | Phasing in | Not law |
|---|---|---|
| GDPR | CRA: reporting since 11 Sep 2026, full 11 Dec 2027 | EDPB draft Guidelines 1/2026 (research) |
| Open Data Directive, through national law | AI Act high-risk: Annex III 2 Dec 2027, Annex I 2 Aug 2028 | EDPB draft Guidelines 02/2026 (anonymisation) |
| AI Act: prohibitions, GPAI, Art 50 | EHDS: 26 Mar 2027; secondary use 26 Mar 2029; more categories 26 Mar 2031 | Digital Omnibus COM(2025)837: Council mandate 21 Oct 2026, Parliament committee vote expected early 2027 |
| Digital Omnibus on AI, Reg. (EU) 2026/1744, in force 27 Jul 2026 | | |
| Finnish Secondary Use Act | | |

Scope trap: the AI Act excludes research-only systems and pre-market research (Art 2(6), 2(8)). Deployment and real-world testing are not excluded.

**Sources:** AI Act; AI Omnibus; EHDS; CRA; EDPB 1/2026 (draft); EDPB 02/2026 (draft); COM(2025)837; Council mandate 2026; NicFab 2026

---

## Build notes for Claude Code

- New repo with the theme copied from genAI_researchintegrity (`slidev-theme-aalto-scicomp/`), Slidev pinned to `~0.47.5`, `palette: aalto-classic`, `titles: aalto`. Follow the theme README.
- No section-divider slides. Use an eyebrow: `###### Move 2 of 4`.
- Corner icon: a mini version of the slide 3 tug of war, with the active side highlighted.
- Copy `style.css` for `.ref-line`, `.ref-bottom`, `.corner-icon`, `.grid-3`, `.grid-2-3` and the coloured cards. `.bp-matrix` is defined in the "When should I use AI" slide of `slides.md`. Avoid `>` child selectors, which break per-slide styles in Slidev 0.47.
- Build diagrams as inline SVG or HTML/CSS, like the wheel and pyramid in the current deck.
- Backup slides go after the end slide.

## Check before presenting

- **Slide 4:** Topaz counts references to papers that do not exist. It does not prove AI caused each one, and 91% of affected papers had only one or two.
- **Slide 5:** Li 2026 is a single-author preprint with manual verification.
- **Slide 7:** I read draft Guidelines 02/2026 through law-firm summaries and Knolle 2026 through its abstract and press release. Check both against the originals.
- **Slide 8:** the four classes come from the public aalto.fi page, while the adaptation of the Finnish classification model is still in progress.
- **B2:** I read Reg. (EU) 2026/1744 through summaries, and the Digital Omnibus is moving fast.
- **Taken from the report, not opened:** van Ravenzwaaij, Adams, Demuth and the federated learning review. For Cwik only the bibliographic record was confirmed.

## References

**Rules and guidance**

- [ALLEA 2023](https://doi.org/10.26356/ECOC): European Code of Conduct for Research Integrity, revised edition
- [ODD](https://eur-lex.europa.eu/eli/dir/2019/1024/oj): Open Data Directive (EU) 2019/1024, Art 10
- [Horizon Europe](https://rea.ec.europa.eu/open-science_en): open science obligations
- [FI Policy 2026](https://tsv.fi/fi/palvelut/linjauslouhi/index.php/Aineistot/en): Open research data and methods, national policy 2026–2030
- [GDPR](https://eur-lex.europa.eu/eli/reg/2016/679/oj): Regulation (EU) 2016/679
- [EDPS v SRB](https://www.fieldfisher.com/en-be/locations/belgium/insights/edps-v-srb-cjeu%e2%80%99s-contextual-approach-to-pseudonym): C-413/23 P, summary
- [EDPB 1/2026 (draft)](https://www.edpb.europa.eu/system/files/2026-04/edpb_guidelines_202601_scientificresearch_en.pdf): scientific research
- [EDPB 02/2026 (draft)](https://www.edpb.europa.eu/public-consultations/guidelines-022026-on-anonymisation_en): anonymisation; summary from [DLA Piper](https://privacymatters.dlapiper.com/2026/08/eu-edpb-publishes-draft-guidelines-on-anonymisation/)
- [COM(2025)837](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52025PC0837): Digital Omnibus proposal
- [Council mandate 2026](https://iapp.org/news/a/eu-member-states-finalize-digital-omnibus-negotiating-stance): IAPP report; [NicFab 2026](https://www.nicfab.eu/en/posts/digital-omnibus-council/): procedural status
- [AI Act](https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng): Regulation (EU) 2024/1689
- [AI Omnibus](https://eur-lex.europa.eu/eli/reg/2026/1744/oj/eng): Regulation (EU) 2026/1744; summary from [Stephenson Harwood](https://www.stephensonharwood.com/media/x0gbn3zx/the-digital-omnibus-on-ai-ten-key-takeaways.pdf)
- [EHDS](https://eur-lex.europa.eu/eli/reg/2025/327/oj): Regulation (EU) 2025/327; [Art 61 text](https://streamlex.eu/articles/ehds-en-art-61/)
- [CRA](https://eur-lex.europa.eu/eli/reg/2024/2847/oj): Regulation (EU) 2024/2847
- [Findata](https://findata.fi/en/permits/data-permits/): data permits
- [EC Guidelines v4](https://research-and-innovation.ec.europa.eu/document/2b6cf7e5-36ac-41cb-aab5-0d32050143dc_en): Living guidelines on generative AI in research, 15 October 2026
- [TENK 2026](https://tenk.fi/sites/default/files/2026-06/Artificial%20Intelligence%20in%20Research.%20TENK%27s%20Recommendation%202026.pdf): AI in research recommendation
- [Aalto best practices](https://www.aalto.fi/en/research-art/best-practices-for-ai-use-in-research-work)

**Research evidence**

- [Gabelica 2022](https://pubmed.ncbi.nlm.nih.gov/35654271): compliance with data sharing statements
- [Wilkinson 2016](https://doi.org/10.1038/sdata.2016.18): FAIR principles
- [van Ravenzwaaij 2025](https://journals.sagepub.com/doi/10.1177/25152459251336130): de-identification and FAIR, worked examples
- [Soneson 2025](https://doi.org/10.1016/j.jadohealth.2025.03.004): adolescents and sensitive data
- [Topaz 2026](https://retractionwatch.com/2026/05/07/one-in-277-pubmed-indexed-papers-in-2026-shows-fabricated-references-says-analysis/): fabricated references, Retraction Watch report on the Lancet letter
- [Cui & Alexander 2026](https://doi.org/10.48550/arXiv.2602.14349): same prompt, different outcomes
- [Cwik 2026](https://doi.org/10.1186/s41073-026-00245-8): disclosure is not documentation
- [Li 2026](https://arxiv.org/abs/2601.05918): re-identification in the Anthropic Interviewer dataset
- [Knolle 2026](https://doi.org/10.1038/s41586-026-10688-0): disparate privacy risks from medical AI; [TUM release](https://www.tum.de/en/news-and-events/all-news/press-releases/details/study-reveals-privacy-risks-in-medical-ai)
- [Rodriguez 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12647387/): re-identification risk in trial datasets
- [Williams 2025](https://pmc.ncbi.nlm.nih.gov/articles/PMC12273930/): the challenges of replication
- [Adams 2025](https://pubmed.ncbi.nlm.nih.gov/40343279/): fidelity, privacy and utility of synthetic patient data
- [Demuth 2025](https://pubmed.ncbi.nlm.nih.gov/41032725/): virtual clinical trials as open datasets
- [Federated review 2025](https://www.sciencedirect.com/science/article/pii/S2773186325002257): privacy-preserving federated learning in healthcare
- [Honkela interview 2026](https://lumi-ai-factory.eu/articles/international-data-protection-day/): differential privacy, synthetic data, unlearning

**Incidents and security**

- [UKB statement 2026](https://www.ukbiobank.ac.uk/?p=63092): response on data in code repositories
- [UKB Oversight 2026](https://www.ukbiobank.ac.uk/news/report-into-data-security-at-uk-biobank-published/): Oversight Committee report
- [Register 2026](https://www.theregister.com/2026/04/23/500k_biobank_volunteers_data_listed/): sale listings
- [Vastaamo 2020](https://cyberscoop.com/finnish-psychotherapy-data-breach-vastaamo/)
- [Manchester 2023](https://www.govinfosecurity.com/trauma-terrorist-victim-data-breached-in-university-attack-a-22409)
- [Wiz 2023](https://wiz.io/blog/38-terabytes-of-private-data-accidentally-exposed-by-microsoft-ai-researchers): Microsoft AI research exposure
- [Willison 2025](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/): lethal trifecta
- [Nikkei 2025](https://asia.nikkei.com/business/technology/artificial-intelligence/positive-review-only-researchers-hide-ai-prompts-in-papers): hidden prompts in manuscripts
