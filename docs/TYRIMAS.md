# Tyrimas: informacijos rinkimo–atrankos–sisteminimo moduliai ir mokslinis procesas

Data: 2026-07-15. Atliktas web-researchas apie esamus įrankius, mokslinius/epistemologinius karkasus, UX praktikas ir duomenų modelius. Santrauka lietuviškai, šaltiniai — originalūs.

---

## 1. Esami įrankiai: rinkimas → atranka → sintezė

| Įrankis | Stiprybė | Spraga |
|---|---|---|
| **Zotero** | Geriausias rinkimui: naršyklės kirpiklis, PDF + metaduomenys, citavimas | Silpnas sintezei — „biblioteka Zotero, mąstymas kitur" |
| **Obsidian (Zettelkasten)** | Lokalūs Markdown užrašai, dvikrypčiai ryšiai, grafas, Zotero integracija | Ryšys nesako, *kodėl* du užrašai susiję — nėra epistemikos |
| **Roam / Logseq** | Blokų lygmens nuorodos, dienoraštinis rinkimas be trinties | Chaotiška šaltinių medžiagai; Roam nyksta |
| **Notion** | Tikros duomenų bazės (savybės, view'ai, ryšiai) — gera atrankos matricoms | Silpnas PDF/anotacijos, jokios epistemikos |
| **Elicit.org** | DI literatūros apžvalga: klausimas → radinių matrica iš tūkst. straipsnių | Tik moksliniai straipsniai, nėra asmeninės bazės |
| **ResearchRabbit** | Vizuali citavimo tinklo paieška („Spotify straipsniams") | Tik atradimas, be atrankos/sintezės |
| **Readwise / Reader** | Highlight'ų rinkimas iš visur + kartojimas intervalais (Daily Review) | Priminimai be mąstymo sluoksnio — highlight'ai nevirsta teiginiais |
| **Heptabase** | Vizualus kortelių sisteminimas lentoje, anotacijos | Erdvinis dėliojimas netipizuotas epistemiškai |

Šaltiniai: pdf.ai/resources/knowledge-base-software-comparison, atlasworkspace.ai/blog/pkm-apps-for-researchers, thesoftwarescout.com (Obsidian vs Logseq 2026; Notion vs Logseq 2026), stilllater.com/productivity/notion-vs-obsidian-vs-roam, aitoolranked.com/blog/elicit-review-best-ai-literature-review-tools, effortlessacademic.com (Litmaps vs ResearchRabbit), readwise.io, wiki.heptabase.com.

**Bendra visų spraga:** nė vienas neseka įsitikinimų būsenos — nėra hipotezių, pasitikėjimo, prieštaravimų fiksavimo, išvadų revizijos ciklo. Čia Laulife gali skirtis.

## 2. Moksliniai / epistemologiniai karkasai, pritaikomi appse

- **Įrodymų hierarchijos / GRADE** — įrodymai rikiuojami pagal tyrimo dizainą (sisteminės apžvalgos ir RCT viršuje → anekdotai apačioje); GRADE prideda skaidrų tikrumo kėlimą/žeminimą. Tiesiogiai virsta šaltinio kokybės lauku su 4–5 lygiais. (en.wikipedia.org/wiki/Hierarchy_of_evidence; ncbi.nlm.nih.gov/pmc/articles/PMC2981887)
- **Claim–Evidence–Reasoning / discourse graphs** — žinios modeliuojamos kaip Klausimai → Teiginiai → Įrodymai → Šaltiniai su tipizuotais ryšiais (palaiko/prieštarauja/informuoja). Referencinė realizacija — Joel Chan „Discourse Graph" (Roam/Obsidian pluginai). (discoursegraphs.com; arxiv.org/abs/2407.20666)
- **Analysis of Competing Hypotheses (ACH)** — CŽV analitikų metodas: matrica hipotezės × įrodymai, kiekvienas langelis „suderinama/nesuderinama"; prioritetas **diagnostiniams** įrodymams ir bandymui **paneigti**, o ne patvirtinti. Labai gerai verčiasi į UI. (en.wikipedia.org/wiki/Analysis_of_competing_hypotheses)
- **Bajeso atnaujinimas / kalibracija** — laikyti tikimybę prie kiekvieno teiginio, žurnaluoti kiekvieną pakeitimą su jį sukėlusiu įrodymu, ilgainiui matuoti kalibraciją (Metaculus stilius). (metaculus.com/help/prediction-resources; lesswrong.com „Building an epistemic status tracker")
- **Argumentų žemėlapiai (Kialo)** — už/prieš medis po teze, kiekvienas teiginys susietas su šaltiniais ir paaiškinimu *kaip* šaltinis jį palaiko. Įrodyta, kad lavina kritinį mąstymą. (en.wikipedia.org/wiki/Kialo; kialo-edu.com/research)
- **PRISMA sisteminės apžvalgos srautas** — identifikuoti → atrinkti → tinkamumas → ištraukti → sintezuoti, su diagramą ir **užfiksuotomis atmetimo priežastimis**. Lengva „asmeninė PRISMA" piltuvėlio versija — stiprus šablonas. (libguides.mq.edu.au/systematic_reviews/prisma_screen)
- **Šaltinių vertinimas — SIFT ir CRAAP** — SIFT (Stop, Investigate, Find better coverage, Trace to original) su „lateral reading" pranoksta paprastus checklistus; CRAAP (Currency, Relevance, Authority, Accuracy, Purpose) tinka kaip balų kriterijai. Appse — 30 sek. vedlys atrankos metu. (library.lapc.edu/evaluating-online-sources/sift-method; merritt.libguides.com)

## 3. UX praktikos rinkimui ir atrankai

- **Universali dėžutė → triage eilė**: vienas mažos trinties įmetimo taškas (share sheet, kirpiklis); atskiras Linear-tipo „Triage" vaizdas, kur viskas peržiūrima, nukreipiama arba atmetama. Principas — „rink neapsispręsdamas, kur padėti". (linear.app/docs/triage)
- **CODE konvejeris (Forte)**: Capture → Organize → Distill → Express; tvarkyti pagal veiksmingumą (PARA), ne pagal temų taksonomiją. (fortelabs.com)
- **Progresyvi santrauka**: distiliuoti sluoksniais (highlight → bold → mini-santrauka) tik tiek, kiek elementas nusipelno, tuo metu, kai jį lieti. (fortelabs.com/blog/progressive-summarization…)
- **Kartojimas intervalais**: Readwise Daily Review kasdien iškelia kelis senus highlight'us — natūralus kablys klausimui „ar šis įrodymas vis dar palaiko tavo teiginį?" (readwise.io)
- **Kasdienis apdorojimo ritualas + inbox zero**; nauja banga — DI *siūlo* paskirtį su priežastimi, žmogus tvirtina.

## 4. Duomenų modelio idėjos

- **Esybės** (iš discourse-graph / nanopublication praktikos): `Šaltinis`, `Ištrauka`, `Įrodymas`, `Teiginys`, `Klausimas`, `Hipotezė` (su tikimybe), `Išvada`, `Žyma`. (discoursegraphs.com; arxiv.org/pdf/1305.3506)
- **Tipizuoti ryšiai, ne pliki linkai**: `palaiko`, `prieštarauja`, `informuoja`, `atsako`, `kildinama-iš`, `cituoja`.
- **Provenance kaip pirmos klasės duomuo** (nanopublikacijų šablonas): kiekvienas tvirtinimas saugo kas/kada/iš-kur. (arxiv.org/pdf/2203.01608)
- **Balai**: šaltiniui — GRADE-tipo lygis + SIFT/CRAAP būsena; įrodymui — aktualumas + patikimumas + diagnostiškumas (ACH); hipotezei — tikimybė + atnaujinimų žurnalas; išvadai — pasitikėjimas + „peržiūrėti iki" data.
- **ACH matrica kaip išvestinis vaizdas** — skaičiuojama iš grafo, atskiro saugojimo nereikia.
- **Gyvavimo ciklai**: elemento (`inbox → triaged → vetted → distilled → integrated`) ir hipotezės (`proposed → active → supported → refuted → superseded`).

## 5. Galimybės / Laulife skirtukai

1. **Įsitikinimų sekimas kaip stuburas** — pasitikėjimas prie kiekvieno teiginio su įrodymais susieta atnaujinimų istorija; niekas mainstream'e to nedaro.
2. **Asmeninis PRISMA piltuvėlis** — matomas identifikuoti→atrinkti→įtraukti srautas su suskaičiuotais atmetimais kasdieniam researchui, ne tik akademiniam.
3. **Vedlio tipo šaltinio patikra atrankoje** — SIFT/CRAAP per 30 sek., balas paveldimas visų to šaltinio įrodymų.
4. **Prieštaravimų išryškinimas** — aktyviai rodyti, kai naujas įrodymas prieštarauja esamai išvadai (ACH „pirmenybė paneigimui"); dabartiniai įrankiai tik kaupia patvirtinimus.
5. **Kartojamas *per-vertinimas*, ne per-skaitymas** — „pasitikėjimas H3 = 70 % ir nekito 60 d.; atėjo 2 prieštaraujantys įrodymai — peržiūrėti?"
6. **Viena apimtis: web + užrašai + dokumentai** — Elicit apsiriboja straipsniais, PKM įrankiai be mokslo; Laulife gali sukti vieną mokslinį ciklą per visus asmeninius šaltinius.
7. **DI siūlo, žmogus teisėjauja** — DI siūlo teiginių ištraukimą, ryšių tipus, paskirtį su priežastimi; tvirtina vartotojas — epistemologinė atsakomybė lieka žmogui.
